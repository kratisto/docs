---
title: MKS Premium Plan Beta
excerpt: 'Features and limitations of the MKS Premium Plan in Beta version'
updated: 2025-04-29
---

<style>
 pre {
     font-size: 14px;
 }
 pre.console {
   background-color: #300A24;
   color: #ccc;
   font-family: monospace;
   padding: 5px;
   margin-bottom: 5px;
 }
 pre.console code {
   b   font-family: monospace !important;
   font-size: 0.75em;
   color: #ccc;
 }
 .small {
     font-size: 0.75em;
 }
</style>

> [!primary]
> This document describes the features and 'how-to' for the Managed Kubernetes Service Premium Plan currently in beta version. For additional details on the Managed Kubernetes Service Standard plan, refer to the [following documentation](/pages/public_cloud/containers_orchestration/managed_kubernetes/known-limits).

## Standard vs Premium comparison

| Plan                  | Standard                                            | Premium                                   |
| --------------------- | --------------------------------------------------- | ----------------------------------------- |
| ControlPlane          | Managed                                             | Managed & Cross-AZ resilient              |
| Availability          | 99,5% SLO                                           | 99,99 SLA (at General Availability stage) |
| etcd                  | Shared, up to 400MB                                 | Dedicated, up to 8GB                      |
| Max cluster size      | Up to 100 nodes                                     | Up to 500 nodes                           |
| Regional availability | Single-zone regions (3-AZ regions planned for 2025) | 3-AZ region for now                       |

## Limitations / Upcoming features

In order to help you make the best use of our new Managed Kubernetes Service (MKS) Premium Plan, we have listed some limitations and guidelines related to specific features.

This list is subject to change as new features will be introduced during the Beta period, planned for the end of summer 2025.

### Cluster upgrade

Upgrading an existing cluster is not supported at the moment, we'll deliver this functionality once we support the next Kubernetes release (1.33).

### Cluster rename

Renaming an existing cluster is not supported at the moment.

### Logs Data Platform integration

Audit logs forwarding to the [Logs Data Platform](/pages/public_cloud/containers_orchestration/managed_kubernetes/forwarding-audit-logs-to-logs-data-platform) is not supported at the moment.

### ETCD Quota

Real-time monitoring of the etcd storage usage is not supported at the moment, current etcd quota is 8GB per cluster.

### API server admission plugins configuration

The configuration of the [API server admission plugins](/pages/public_cloud/containers_orchestration/managed_kubernetes/apiserver-flags-configuration) is not available at the moment.

### API Server IP restrictions

To enable IP filtering on the API server, the IP of the gateway in the cluster's OpenStack subnet should be specified.
This allows worker nodes to communicate with the API server.

Retrieve the gateway IP of your cluster's gateway in the Manager, or by using the following command:

```bash
openstack router show ROUTER_ID -c external_gateway_info
```

### Security Policies

Changing the Security Policy after the cluster creation is not supported yet.

### Anti-affinity

This feature allows worker nodes to be deployed on different hypervisors (physical servers), guaranteeing better fault tolerance. It is currently supported on the MKS Premium Plan (EU-WEST-PAR).

We recommend using multiple Availability Zones (AZs) instead by using node pool to spread worker nodes between AZ.

### Ports

The OpenStack security group for worker nodes is the `default` one. It allows all egress and ingress traffic by default on your private network.

```bash
openstack security group rule list default
+--------------------------------------+-------------+-----------+-----------+------------+-----------+-----------------------+----------------------+
| ID                                   | IP Protocol | Ethertype | IP Range  | Port Range | Direction | Remote Security Group | Remote Address Group |
+--------------------------------------+-------------+-----------+-----------+------------+-----------+-----------------------+----------------------+
| 0b31c652-b463-4be2-b7e9-9ebb25d619f8 | None        | IPv4      | 0.0.0.0/0 |            | egress    | None                  | None                 |
| 25628717-0339-4caa-bd23-b07376383dba | None        | IPv6      | ::/0      |            | ingress   | None                  | None                 |
| 4b0b0ed2-ed16-4834-a5be-828906ce4f06 | None        | IPv4      | 0.0.0.0/0 |            | ingress   | None                  | None                 |
| 9ac372e3-6a9f-4015-83df-998eec33b790 | None        | IPv6      | ::/0      |            | egress    | None                  | None                 |
+--------------------------------------+-------------+-----------+-----------+------------+-----------+-----------------------+----------------------+
```

For now it is recommended to leave these security rules in their "default" configuration or the nodes could be disconnected from the cluster.

### Reserved IP ranges

The following ranges are used by the cluster, and should not be used elsewhere on the private network attached to the cluster.

```text
10.240.0.0/13 # Subnet used by pods
10.3.0.0/16 # Subnet used by services
```

## Getting started

The following methods are supported to create an MKS Premium cluster:

### Using Terraform

Refer to the [dedicated documentation](/pages/public_cloud/containers_orchestration/managed_kubernetes/creating-a-cluster-through-terraform) to create a Managed Kubernetes cluster.

Here is a sample Terraform file that creates an MKS Premium cluster and three nodepools on three different availability zones in the `EU-WEST-PAR` region.

```
terraform {
  required_providers {
    ovh = {
      source  = "ovh/ovh"
    }
  }
}

provider "ovh" {
  endpoint           = "ovh-eu"
  application_key    = "<your_access_key>"
  application_secret = "<your_application_secret>"
  consumer_key       = "<your_consumer_key>"
}

resource "ovh_cloud_project_kube" "my_kube_cluster" {
  service_name = var.service_name
  name         = "lgr-terraform-test-3az"
  region       = "EU-WEST-PAR"
  version      = "1.31"
  private_network_id = "<OpenStack Network Id>"
  nodes_subnet_id = "<Openstack Subnet Id>"
}
resource "ovh_cloud_project_kube_nodepool" "node_pool_a" {
  service_name  = var.service_name
  kube_id       = ovh_cloud_project_kube.my_kube_cluster.id
  name          = "my-pool-a-1"
  flavor_name   = "b3-8"
  availability_zones = ["eu-west-par-a"]
  desired_nodes = 1
}
resource "ovh_cloud_project_kube_nodepool" "node_pool_b" {
  service_name  = var.service_name
  kube_id       = ovh_cloud_project_kube.my_kube_cluster.id
  name          = "my-pool-b-1"
  flavor_name   = "b3-8"
  availability_zones = ["eu-west-par-b"]
  desired_nodes = 1
}
resource "ovh_cloud_project_kube_nodepool" "node_pool_c" {
  service_name  = var.service_name
  kube_id       = ovh_cloud_project_kube.my_kube_cluster.id
  name          = "my-pool-c-1"
  flavor_name   = "b3-8"
  availability_zones = ["eu-west-par-c"]
  desired_nodes = 1
}
output "kubeconfig_file" {
  value     = ovh_cloud_project_kube.my_kube_cluster.kubeconfig
  sensitive = true
}

```

## Go further

- If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](/links/professional-services) to get a quote and ask our Professional Services experts for assisting you on your specific use case of your project.

- Join our [community of users on Discord](https://discord.com/channels/850031577277792286/1366761790150541402)!
