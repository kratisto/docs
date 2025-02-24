---
title: "Managed VCD - Limitations"
excerpt: "Learn about the limitations of Managed VCD, including resource caps and configuration constraints."
updated: 2025-02-24
---

## Objective

**This guide explains the limitations of Managed VCD, including resource constraints and configuration restrictions.**

> [!warning]
> Before creating a network or a VM, ensure you check the limitations by consulting the official documentation:
>
>- [Creating a VM on VMware Cloud Director](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/hosted_private_cloud_powered_by_vmware/vcd-first-vm-creation/guide.en-gb.md)
>- [Creating network components via VCD](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd_network_creation/guide.en-gb.md)

## Requirements

Before getting started, review the following guides to better understand VMware Cloud Director:

- [VMware Cloud Director - Fundamental Concepts](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd-get-concepts/guide.en-ie.md)
- [VMware Cloud Director - Network Concepts](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd_network_concepts/guide.en-ie.md)

## Instructions

### General limitations

| Resource | Standard | Advanced | Premium | Comments |
|----------|---------|----------|---------|----------|
| vCPU (per VM) | 32 | 32 | 32 | Number of available vCPUs per VM. |
| vCPU (cores per socket) | 1 | 1 | 1 | - |
| Number of sockets (per VM) | 1 | 1 | 1 | - |
| RAM (per VM) | 128 GB | 128 GB | 128 GB | Maximum RAM per VM (min. 0.5 GB). |
| Network Cards (per VM) | 5 | 10 | 10 | Maximum number of network adapters per VM. |
| Edge Gateway (per organization) | N/A | 42 | 42 | Maximum number of Edge Gateways per organization. |
| Public IPs (per vDC) | N/A | 2 | 2 | Number of available public IPs per vDC. |
| Storage (per VM) | 1.5 TB | 1.5 TB | 1.5 TB | Storage limit on NFS/vSAN. |
| Snapshots (per VM) | 3 | 3 | 3 | Maximum of 3 snapshots per VM. |
| VMs (per vApp) | 128 | 128 | 128 | Maximum number of VMs allowed per vApp. |
| VMs (per organization) | 2000 | 4000 | 4000 | Maximum number of VMs per organization. |
| vApps (per organization) | 10,000 | 10,000 | 10,000 | Maximum number of vApps per organization. |

### Hardware limitations

| Resource | Standard | Advanced | Premium | Comments |
|----------|---------|----------|---------|----------|
| vCPU Frequency Min | 1 GHz | 1 GHz | 1 GHz | Depends on Baremetal hardware. |
| vCPU Frequency Max | 3 GHz | 3 GHz | 3 GHz | Depends on Baremetal hardware. |
| Storage per VM (VMDK) | 1.5 TB | 1.5 TB | 1.5 TB | Storage limit on VMDK. |
| Maximum Number of Storage Policies | - | To be validated | To be validated | Need confirmation if a limit exists. |

## Go further

If you require training or technical support to implement our solutions, please contact your sales representative or click [this link](/links/professional-services) to get a quote and request a custom analysis of your project from our Professional Services team experts.

Ask questions, give your feedback and interact directly with the team building our Hosted Private Cloud services on the dedicated channel [Discord](https://discord.gg/ovhcloud).

Join our [community of users](/links/community).