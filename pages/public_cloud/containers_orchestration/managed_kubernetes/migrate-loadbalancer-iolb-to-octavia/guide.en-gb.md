---
title: How to migrate from LoadBalancer for MKS (IOLB) to Public Cloud LoadBalancer (Octavia)
excerpt: "How do I migrate from a LoadBalancer for MKS (IOLB) to a LoadBalancer for the Public Cloud (Octavia)"
updated: 2025-01-17
---

## Objective

The purpose of this guide is to help OVHcloud Managed Kubernetes Service (MKS) to migrate from an existing [Loadbalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) to a [Public Cloud Load Balancer](/links/public-cloud/load-balancer).

[Loadbalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) is the default Load Balancer for MKS clusters using Kubernetes versions >1.30.

[Loadbalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) is deprecated for MKS clusters using Kubernetes versions >1.31.

It explains the steps required to make this transition safely, minimising service interruptions. Finally, it provides recommendations on DNS management, in particular reducing the TTL, to optimise the propagation of changes and ensure a smooth migration.

> [!warning]
>
> As Loadbalancer for Kubernetes and Public Cloud LoadBalancer do not use the same solution for Public IP allocation, it is not possible to keep the existing public IP of your Loadbalancer for Kubernetes. Changing the LoadBalancer class of your Service will lead to the creation of a new Loadbalancer and the allocation of a new Public IP (Floating IP).

## Comparison

When selecting a load balancing solution, it's important to compare the features and limitations of each option. Below is a comparison between Load Balancer for Kubernetes and Public Cloud Load Balancer, highlighting their key differences and capabilities.

|                                     | Load Balancer for Kubernetes | Public Cloud Load Balancer |
| ----------------------------------- | ---------------------------- | -------------------------- |
| Maximum number of connections       | 10 000                       | up to 20 000               |
| Maximum number of HTTP  requests    | 2000                         | Up to 80 000               |
| Bandwith                            | 200 Mbit/s                   | up to 4 Gbit/s (up/down)   |
| Supported protocol                  | TCP                          | TCP/UCP                    |
| Supported load balancing layers     | L4                           | L4/L7                      |
| Capacity to export metrics and logs | No                           | Yes                        |
| Private to private scenario         | No                           | Yes                        |
| Floating IP                         | No                           | Yes                        |

## Migration of your LoadBalancer

> [!warning]
>  
> Starting from MKS cluster using Kubernetes version **1.32**, any cluster upgrade attempt will be blocked if an service [Loadbalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) (IOLB) is still present in the cluster.
>  
> Action required**: Before upgrading, you must **migrate your services to the Public Cloud LoadBalancer (Octavia)** by following the steps described in this guide.  
>  
> If you attempt to upgrade without first migrating, an error will be returned, preventing the upgrade.
>
> The old LoadBalancer and IP will be deleted, making services unreachable. Perform the DNS switch immediately with the new IP.
> You can reserve a public IP (floating IP) in advance and specify it during service/load balancer creation.

In order to migrate from an existing [LoadBalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) to a [Public Cloud LoadBalancer](/links/public-cloud/load-balancer) you will have to modify an existing Service and change its LoadBalancer class.

Your existing LoadBalancer Service using [LoadBalancer for Kubernetes](/links/public-cloud/load-balancer-kubernetes) should have the following annotation:

```yaml
annotations:
  loadbalancer.ovhcloud.com/class: "iolb"
```

##### Step 1 - Edit your Service to change the LoadBalancer class to 'octavia'

```yaml
annotations:
  loadbalancer.ovhcloud.com/class: "octavia" // not required for clusters running kubernetes versions >= 1.31, you can just remove the annotation.
```

##### Step 2 - Apply the change

```yaml
kubectl apply -f your-service-manifest.yaml
```

## Perform a DNS switch

### Check the current TTL

By default, DNS servers cache the IP address of a domain for a period defined by the TTL (Time-To-Live).

A TTL that is too long can slow down the transition by forcing some users to wait several hours before accessing the new Load Balancer. To avoid this, we recommend temporarily reducing the TTL before updating the IP.

Before changing the TTL, it is important to know its current value. To do this, run the following command in a terminal:

```bash
dig yourdomain.com +noall +answer

yourdomain.com.             600     IN      A       17*.***.**.*4
```

Here, 600 corresponds to the TTL in seconds (i.e. approximately 10 minutes). This means that the DNS servers keep this IP in cache for this length of time before checking for an update.

### Lower the TTL before migration

To lower the TTL, follow these steps:

- Access your DNS management console.
- Find the A record (or CNAME) associated with your domain.
- Change the TTL of your A or CNAME record by reducing it to 300 seconds (5 min).
- Wait 24 to 48 hours for this new TTL to propagate.

> [!info]
>
> Why wait? Because DNS servers must first clear their caches before adopting the new TTL.

### Update the Load Balancer IP

Once the TTL reduction has been propagated :

- Replace the old IP with the one of the new Load Balancer in your DNS record.
- Thanks to the low TTL, users will quickly see the update.
- Check that the change is effective using the same **dig** command you used recently. You should see the new IP displayed.

### Restore TTL after migration

Once the transition has been validated and the old Load Balancer disconnected, reset the TTL to a higher value.

## Other resources

- [Exposing applications using services of LoadBalancer type](https://github.com/kubernetes/cloud-provider-openstack/blob/master/docs/openstack-cloud-controller-manager/expose-applications-using-loadbalancer-type-service.md)
- [Using Octavia Ingress Controller](https://github.com/kubernetes/cloud-provider-openstack/blob/master/docs/octavia-ingress-controller/using-octavia-ingress-controller.md)
- [OVHcloud Load Balancer concepts](/pages/public_cloud/public_cloud_network_services/concepts-03-loadbalancer)
- [How to monitor your Public Cloud Load Balancer with Prometheus](/pages/public_cloud/public_cloud_network_services/technical-resources-02-octavia-monitoring-prometheus)

## Go further

Visit the [Github examples repository](https://github.com/ovh/public-cloud-databases-examples/).

Visit our dedicated Discord channel: <https://discord.gg/ovhcloud>. Ask questions, provide feedback and interact directly with the team that builds our Container and Orchestration services.

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](/links/professional-services) to get a quote and ask our Professional Services experts for a custom analysis of your project.

Join our community of users on <https://community.ovh.com/en/>.
