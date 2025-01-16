---
title: Block Storage security specification
excerpt: Block Storage security overview
updated: 2025-01-16
---

## Objective

In addition to [the responsibility model for Public Cloud Block Storage](/pages/block_storage/responsibility-model-block-storage), this security fact sheets aims at describing security features and 
functions associated to the service. It also describes best practices that customers can adopt to secure their Block Storage volumes based on OpenStack technology.

### 1. Certifications

- ISO/IEC 27001
- ISO/IEC 27701
- ISO/IEC 27017
- ISO/IEC 27018
- HDS
- SOC 1 type II
- SOC 2 type II
- CSA type II
- C5 type II

### 2. Recommendations once the service is delivered

Once you have subscribed to Instances service, you can add your Block storage volumes. You can manages users' rights through the Users & Roles section in the customer Control Panel by following 
this [guide](/pages/public_cloud/compute/create_and_delete_a_user).


### 3. Service Level Agreement (SLA)

The SLA varies between 99.999% and 99.5% and differs between offers and ranges. Please refer to the specific terms and conditions of service for more details.

### 4. Backups



#### 4.2 Customer data backups

You  must implement additional back-up device based on customer tools or options offered by OVH such as Second server, IP Fail Over, etc.

| **Option** | **Granularity** | **RPO** | **RTO** | **Documentation** |
| --- | --- | --- | --- | --- |
| Volume backup | The Block Storage volume | Depends on the date of the last backup and how long it takes to resolve the case | Depends on the volume size| [Creating a volume backup](/pages/public_cloud/compute/volume-backup)|


### 5. Logs

| **Source** | **Content** | **Documentation** |
| --- | --- | --- |
| Control Panel | Logs of interactions made by admin, technical or billing contacts in the Control Panel and services they have access to, using API calls. |- <https://api.ovh.com/console/#/me> (see `/me/api/logs`)<br>- [List of API calls done with your account](https://api.ovh.com/console/#/me/api/logs/self~GET)<br>- [List of API calls done on services you have access to](https://api.ovh.com/console/#/me/api/logs/services~GET)<br>- [Get your audit logs](https://api.ovh.com/console/#/me/logs/audit~GET) |

### 6. API

| **Name** | **Capacity** | **Documentation** |
| --- | --- | --- |
| Control Panel and service | Manage customer accounts and services on which each account has access rights. | [Managing volumes in the OpenStack API](/pages/public_cloud/compute/starting_with_managing_volumes_openstack_api)|

### 7. Accounts - User

#### 7.1 Control plane

Using your customer account on the OVHcloud Control Panel, you are able to manage your service using [three different contacts](/pages/account_and_service_management/account_information/managing_contacts).<br>
OVHcloud uses another account with an internal NIC to refer a customer having subscribed to several services.

To enforce security access to your account on the Control Panel, we recommend activating a [two-factor authentication mechanism](/pages/account_and_service_management/account_information/secure-ovhcloud-account-with-2fa) or [SSO (Single Sign-On) authentication](/pages/account_and_service_management/account_information/ovhcloud-account-connect-saml-adfs).


#### 7.2 Data plane

Once you get your credentials, you are autonomous to create user accounts on your OS and applications you've installed.

### 8. Features and options available at service delivery


#### 8.1 HDS option

The HDS option can be activated on the service.<br>
The subscription to the [Business support level](https://www.ovhcloud.com/en/support-levels/business/)is mandatory, at least to maintain necessary requirements.

### 9. Reversibility

To ensure reversibility on the service, you may follow the [specific reversibility policy](/pages/account_and_service_management/reversibility/03-public-cloud-reversibility-policy) to import and export your data in complete autonomy. 

#### 9.1 Erasure of customer data

Once you have destroyed your public Cloud project, in the OVHcloud control panel, all allocated resources are released.
