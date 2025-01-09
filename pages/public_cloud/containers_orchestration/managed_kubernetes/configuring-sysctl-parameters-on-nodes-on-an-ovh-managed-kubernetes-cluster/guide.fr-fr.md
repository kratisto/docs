---
title: Adapt your Inotify parameters for your deployments
excerpt: 'Adapt your Inotify parameters for your deployments which needs to have specific Inotify parameters'
updated: 2025-01-09
---

## Objective

The OVHcloud Managed Kubernetes service gives you access to Kubernetes clusters, without the hassle of installing or operating them.
But for some specific usecases, you may have to customize nodes parameters.

This guide will cover the modification of the Sysctl parameters which takes in charge the Inotify part and allows you to open more files simultaneously.

## Requirements

- A [Public Cloud project](https://www.ovhcloud.com/fr/public-cloud/) in your OVHcloud account
- Access to the [OVHcloud Control Panel](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/fr/&ovhSubsidiary=fr)
- An OVHcloud Managed Kubernetes cluster
- Access to your OVHcloud Managed Kubernetes cluster through the Kubeconfig file
- You must have the [`kubectl`](https://kubernetes.io/docs/reference/kubectl/overview/){.external} command-line tool installed
- Your Kubeconfig is exported into your terminal following this guide : [Configuring Kubectl](/pages/public_cloud/containers_orchestration/managed_kubernetes/configuring-kubectl-on-an-ovh-managed-kubernetes-cluster)

## Instructions

### Step 1: Create a privileged DaemonSet and define the value to modify

Create a YAML named ```sysctl-tuner-daemonset.yaml``` with the content below:

```yaml
apiVersion: apps/v1
kind: DaemonSet
metadata:
    name: sysctl-tuner
spec:
    selector:
        matchLabels:
            name: sysctl-tuner
    template:
        metadata:
            labels:
                name: sysctl-tuner
        spec:
            containers:
                - name: sysctl
                  image: busybox
                  securityContext:
                      privileged: true
                  command:
                      - sh
                      - -c
                      - "sysctl -w fs.inotify.max_user_watches=<value>" # Define the value you need
            hostNetwork: true
            hostPID: true
            tolerations:
                - operator: "Exists" # Allow running on all nodes, including tainted ones
```

And define the value of the sysctl key ```fs.inotify.max_user_watches``` based on your applications' needs.

The DaemonSet will set the sysctl parameter "fs.inotify.max_user_watches" with the value you provided in the DaemonSet configuration on all nodes deployed into your Kubernetes Cluster.

## Step 2: Test if the changes were applied correctly

In order to check if the Inotify value has been changed properly, you can escalate a shell into a pod : 

```bash 
$ kubectl exec -it <pod> -- cat /proc/sys/fs/inotify/max_user_watches
```

The output should be the same as the value you defined in the DaemonSet YAML defined above.

Congratulations ! You've successfully modified the maximum Inotify "max_user_watches" value on Managed Kubernetes Service.

## Go further

To deploy your first application on your Kubernetes cluster, we suggest you refer to our guide to [Deploying an application](/pages/public_cloud/containers_orchestration/managed_kubernetes/deploying-an-application).

- If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](https://www.ovhcloud.com/fr/professional-services/) to get a quote and ask our Professional Services experts for assisting you on your specific use case of your project.

- Join our [community of users](https://community.ovh.com/en/).


