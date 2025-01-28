---
title: "Move2Cloud: Migrating VMware Workloads to OVHcloud HPC with Veeam Replication"
excerpt: "Learn how to migrate your on-prem VMware workloads to an OVHcloud Hosted Private Cloud environment using Veeam Replication."
updated: 2025-01-28
---

## Objective

This guide explains how to migrate your on-premises VMware workloads to an OVHcloud Hosted Private Cloud (HPC) using Veeam Replication. The steps are straightforward and designed to minimize downtime.

## Requirements

Before getting started, you’ll need:
- A complete list of VMs with FQDNs, IP addresses, and dependencies.
- Correctly sized target resources (e.g., hosts, datastores, vSAN clusters).
- A valid Veeam Backup & Replication (B&R) license.
- Access to vCenter and pre-configured DNS, NTP, and authentication services in HPC.
- A secure network connection (VPN or OVHcloud Connect).
- Relevant OVHcloud and Veeam guides for setup details.

## Instructions

### 1. Inventory source VMs and network configuration
- List all VMs with their FQDNs, IP addresses, operating systems, and dependencies.
- Group VMs by application to reduce service interruptions during migration.
- Document subnets and VLAN IDs for replication planning.

### 2. Size target resources
- Calculate your needs for cores, RAM, and storage.
- Decide on storage types (NFS or vSAN) based on performance requirements.
- Plan VLAN routing and network segregation with NSX-T if needed.

### 3. Whitelist IPs for vCenter access
- Allow required IPs to access the vCenter through the OVHcloud Secure SSL Gateway.
- Follow the [guide to whitelist IPs](https://help.ovhcloud.com/csm/en-gb-vmware-authorise-ip-addresses-vcenter?id=kb_article_view&sysparm_article=KB0045321).

### 4. Set up roles and permissions
- Mirror roles and permissions from your current environment in HPC.
- Use OVHcloud IAM or integrate your existing IAM (e.g., Active Directory, Okta).
- Enable SSO via ADFS using [this guide](https://help.ovhcloud.com/csm/en-gb-connect-saml-sso-adfs?id=kb_article_view&sysparm_article=KB0043008).

### 5. Build your target network
- Set up VLANs, routing, and traffic flow matrices in NSX-T.
- Configure dVS and NSX-T gateways for network segregation and filtering.
- Check the [NSX first steps guide](https://help.ovhcloud.com/csm/en-gb-vmware-nsx-first-steps?id=kb_article_view&sysparm_article=KB0056831).

### 6. Deploy core services in HPC
- Deploy services like NTP, DNS, and authentication to reduce cross-traffic.
- Use `ntp.ovh.net` for time synchronization.
- Set up DNS services, such as an AD Domain Controller.

### 7. Install Veeam B&R server
- Install Veeam Backup & Replication on your OVHcloud HPC.
- Activate the license using [this guide](https://help.ovhcloud.com/csm/en-gb-public-cloud-storage-veeam-backup-replication?id=kb_article_view&sysparm_article=KB0046503).

### 8. Configure a VPN tunnel
- Create an IPsec tunnel between your on-prem infrastructure and OVHcloud.
- Use NSX, Stormshield, or OpnSense for the configuration:
  - [NSX VPN setup](https://help.ovhcloud.com/csm/en-gb-vmware-nsx-configure-ipsec?id=kb_article_view&sysparm_article=KB0058696)
  - [Stormshield VPN setup](https://documentation.stormshield.eu/SNS/v4/en/Content/User_Configuration_Manual_SNS_v4/IPSec_VPN/IPSEC_VPN.htm)
  - [OpnSense VPN setup](https://docs.opnsense.org/manual/how-tos/ipsec-s2s.html)
- Or use [OVHcloud Connect](https://www.ovhcloud.com/fr/network/ovhcloud-connect/) for low-latency and high bandwidth.

### 9. Deploy Veeam proxy server

Deploying a Veeam proxy server is essential for optimizing data transfer during replication. 

Here’s how to set it up:
  1. Open the Veeam Console and go to the **Backup Infrastructure**{.action} section.
  2. In the inventory pane, click **Managed Servers**{.action}.
  3. Add your on-prem proxy server (Windows or Linux) by selecting **Add Server**{.action} and following the wizard.
  4. Once added, configure the server as a proxy by navigating to **Backup Proxies**{.action} and clicking **Add Proxy**{.action}.
  5. Assign the necessary resources and settings (transport mode, maximum concurrent tasks, etc.).

After configuring, verify the proxy server’s connectivity with the Veeam B&R server in your Hosted Private Cloud. 

For a detailed walkthrough, check the [proxy setup guide](https://helpcenter.veeam.com/docs/backup/vsphere/add_vmware_proxy.html?ver=120).

### 10. Create replication jobs

To create a replication job in Veeam Backup & Replication:

  1. Open the Veeam Console and navigate to the **Home** view.
  2. In the inventory pane, click on **Replication Jobs**{.action}.
  3. Select **Create Replication Job**{.action} from the menu.
  4. Follow the wizard to:
     - Add the VMs you want to replicate.
     - Choose the target destination (your OVHcloud HPC).
     - Configure settings like compression, throttling, or application-aware processing if needed.
  5. Specify the schedule for the replication job.

After completing the setup, save the job and run it to start replicating your VMs. 

For detailed steps, check the [replication job setup guide](https://helpcenter.veeam.com/docs/backup/vsphere/replica_job.html?ver=120).

### 11. Start and test replication jobs

Once your replication jobs are set up, start them from the Veeam Console:
  1. Open the **Home** view and navigate to **Replication Jobs**{.action}.
  2. Select the job you created and click **Start**{.action} to begin replication.
  3. Monitor the progress to ensure there are no errors.

To test replication, use the **Failover Now** feature:
  1. Open the **Replicas**{.action} section in the Veeam Console.
  2. Right-click the replicated VM and select **Failover Now**{.action}.
  3. Confirm the action to activate the replica without impacting the source VM.

After testing, undo the failover:
  1. Go back to the same replicated VM in the **Replicas** section.
  2. Right-click and select **Undo Failover**{.action} to revert to the original state and resume replication.

Testing ensures that your replicas are functional and ready for production use without affecting your on-prem environment. 

For more details, refer to the [Failover process](https://helpcenter.veeam.com/docs/backup/vsphere/failover.html?ver=120) and [Undo failover process](https://helpcenter.veeam.com/docs/backup/vsphere/undo_failover.html?ver=120).
### 12. Migrate workloads

Use the **Planned Failover** process to migrate your workloads without losing data or disrupting services:
  1. Open the Veeam Console and go to the **Home** view.
  2. Navigate to the **Replicas** section and locate the VM replica you want to migrate.
  3. Right-click the replica and select **Planned Failover**{.action}.
  4. Confirm the action. Veeam will:
     - Synchronize any final changes from the source VM to the replica.
     - Power off the source VM automatically.
     - Power on the replica in the target environment.

Once the process completes, validate that the replica is active and functional in the Hosted Private Cloud. 

For more details, refer to the [Planned Failover guide](https://helpcenter.veeam.com/docs/backup/vsphere/planned_failover.html?ver=120).


### 13. Validate applications and services
- Confirm VMs boot without issues.
- Test connectivity to services like AD, DNS, and internet-facing apps.
- Verify that all applications are working correctly.

### 14. Confirm permanent failover

- To make the replica VM your new production VM, open the Veeam Console and navigate to the **Home** view.
- Click on **Replicas**{.action} in the inventory pane and find the replica VM you want to finalize.
- Right-click the VM and select **Permanent Failover**{.action} from the menu.
- Confirm the action when prompted.

Once done, Veeam will remove the original VM from replication jobs and adjust the settings so the replica VM becomes the primary one. 

For more details, check the [Permanent Failover guide](https://helpcenter.veeam.com/docs/backup/vsphere/permanent_failover.html?ver=120).

### 15. Optimize and secure your environment
- Move VMs to the desired storage (e.g., vSAN or NFS datastores) using [Storage vMotion](https://help.ovhcloud.com/csm/fr-vmware-storage-vmotion?id=kb_article_view&sysparm_article=KB0046287).
- Create backups for your workloads with OVHcloud S3 storage as described [here](https://help.ovhcloud.com/csm/fr-public-cloud-storage-s3-veeam?id=kb_article_view&sysparm_article=KB0047499).

## Go Further

For more details and advanced options:
- Check [OVHcloud Hosted Private Cloud documentation](https://www.ovhcloud.com/en/private-cloud/).
- Review [Veeam documentation](https://helpcenter.veeam.com/docs/backup/vsphere/index.html?ver=120).
- Contact OVHcloud support if you need additional help.
