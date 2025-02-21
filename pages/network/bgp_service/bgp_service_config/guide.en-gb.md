---
title: BGP Service Configuration
excerpt: By leveraging BGP, you gain full control over your routing policies and network resilience. Follow this guide to set up and optimize your BGP session seamlessly.
updated: 2025-02-21
---

## Introduction

The Border Gateway Protocol (BGP) allows you to build highly available infrastructures by running standard BGP routing protocol straight from your OVHcloud hosts. It can be used with OVHcloud Additional IP or with your own IP addresses, by using BYOIP.

## Requirements

- At least one Bare Metal [dedicated server](/links/bare-metal/bare-metal) from the following range : High Grade, Scale, Advance Gen3. All servers that will participate in the BGP peering must be in the same 1-AZ Region.
- Access to the [OVHcloud Control Panel](/links/manager)
- If you use [Bring Your Own IP (BYOIP)](/links/network/byoip) : IP prefixes that you own and can announce
- A [vRack private network](/links/network/vrack)
- Knowledge in IP networks and BGP routing protocol
- Knowledge in Linux networking

## Instructions

### Step 1: Join the Alpha

First you need to request to join the beta on the following [page](labs.ovh.com). After we receive your application, we will contact you via email.

Important : BGP Service is currently in alpha. This product is not intended to be used in production environment.

### Step 2: Prepare your IP addresses

You need to either buy Additional IP from OVHcloud our use your own IPs with BYOIP.

If you buy Additional IP from us, you MUST NOT associate them to any service (e.g. Baremetal).

If you need to import your IPs, you need to use our BYOIP service. Please follow [this documentation](/pages/network/bring_your_own_ip/bring-your-own-IP/) to import your IPs to OVHcloud.

### Step 3: Configure your vRack

You need to have created a vRack, which is the private network where the peering between your servers and the BGP service will take place.

The vRack must contain the servers that will participate in the BGP peering.

Important : the vRack must contain only servers in one specific availability zone (AZ). For regions with 1-AZ, an AZ is equivalent to a region. Only 1-AZ regions are available in the alpha.

### Step 4: Provide configuration parameters of your BGP Service

You need to provide us the following parameters so that we can configure the BGP service on OVHcloud side :

| Parameter	| Value (example) | Netmask | Description | Comment |
| :--- | :--- | :--- | :--- | :--- |
| Location	| RBX | | The location on which to deliver the service | |
| vRack ID | 937 | | vRack ID on which the BGP sessions will run | |
| BYOIP | Y | | IP block coming from the customer ?	| |
| IP block | 17.13.2.0 | 24 | The IP block to be announced | Allowed range size : <br>&bull; OVHcloud IP (/24 to /30) <br>&bull; BYOIP imported rang (/19 to /24) <br>&bull; IPv6 (/56) |
| Private Subnet | 10.0.0.0 | 28 | Reserved subnet for BGP peer IPs <br> 4 last addresses will be used by OVHcloud for OVHcloud side BGP peers | |
| Peering IP 1 | 10.0.0.1 | | Customer IP should be explictely specificed by customer (for OVH-side monitoring) | |
| Peering IP 2 | 10.0.0.2 | | Customer IP should be explictely specificed by customer (for OVH-side monitoring) | |
| Peering IP 3 | 10.0.0.3 | | Customer IP should be explictely specificed by customer (for OVH-side monitoring) | |
| Peering IP 4 | 10.0.0.4 | | Customer IP should be explictely specificed by customer (for OVH-side monitoring) | |

### Step 5: BGP Service delivery

After a approximatively 2 weeks, your service will be delivered. We will contact you back to notify you that the service is ready to use and give you the following needed parameters on your side :

&bull; OVHcloud peer IPs (4 IPs) <br>&bull; Customer AS and OVH AS to use for the BGP peering sessions
<br>&bull; BFD parameters

### Step 6: Customer-side setup

You now are able to setup the BGP sessions on your side. Below is a guide that walks you through a typical setup for simple load balancing using BGP ECMP.

## Use case : Load Balancing using BGP ECMP

Here is a simple architecture that allows you to perform load balancing of your traffic on 3 hosts :

![BGP LB Architecture](images/BGP_LB_archi_2025.png){.thumbnail}

To achieve this setup, you need to install a BGP daemon, like FRR, on each hosts.

### Configuring a BGP Daemon (FRR) <span style="color:red">TODO</span>

To establish a BGP session using FRR, follow these steps :

### Step 1: Install FRR

On a Debian-based system, install BIRD with:

```bash
sudo apt update && sudo apt install frr frr-pythontools
```

### Step 2: Configure FRR

Edit the FRR configuration file, typically located at /etc/frr/frr.conf:

```bash
router bgp YOUR_ASN
 bgp router-id YOUR_ROUTER_IP
 neighbor YOUR_PEER_IP remote-as PEER_ASN
 neighbor YOUR_PEER_IP ebgp-multihop 5
 address-family ipv4 unicast
  redistribute connected
 exit-address-family
!
```

### Step 3: Restart FRR

After editing the configuration, restart FRR to apply changes:

```bash
sudo systemctl restart frr
```

### Step 4: Verify BGP Session

Check the status of your BGP session with:

```bash
TBD show protocols all
```

### Step 5: Verify Ingress and Egress Connectivity

To ensure your BGP session is functioning correctly, test both inbound and outbound traffic:

**Check Ingress Traffic (Incoming)**
Use a remote server to ping or traceroute to your advertised IP prefix:

```bash
ping YOUR_ADVERTISED_IP
traceroute YOUR_ADVERTISED_IP
```

Verify that traffic reaches your network via the expected BGP paths.

**Check Egress Traffic (Outgoing)**

From your server, check the routing table and ensure your BGP routes are in use:

```bash
ip route show
vtysh -c 'show ip route bgp'
```

Confirm that outbound traffic is following the correct BGP paths.

### Step 6: Verify connectivity with OVHcloud team

When your setup is done and after conducting basic tests, you should notify us via email at this address: <bgp_alpha@ovh.net>.

We'll make sure the BGP connectivity and IP announcements are OK from our side.

## Limitations

The number of peers on OVHcloud side is limited to 4. If you need more than 4 peers, you will need to install a route reflector on your infrastructure in order to redistribute routes to your hosts.

&bull; BGP sessions : 4 BGP sessions per client (4IPv4 + 4IPv6) <br>&bull; prefixes : up to 32 IPv4 prefixes and 32 IPv6 prefixes per client <br>&bull; hosts : 10 hosts per client

## Available Regions

The product is available in the following regions:

| Region Location | Region Name | Region Type |
| :--- | :--- | :--- |
| Europe (France - Paris) (will be available only in beta) | eu-west-par | 3-AZ |
| Europe (France - Gravelines) | eu-west-gra | 1-AZ |
| Europe (France - Roubaix) | eu-west-rbx | 1-AZ |
| Europe (France - Strasbourg) | eu-west-sbg | 1-AZ |
| Europe (Germany - Limburg) | eu-west-lim | 1-AZ |
| Europe (Poland - Warsaw) | eu-central-waw | 1-AZ |
| Europe (UK - Erith) | eu-west-eri | 1-AZ |
| North America (Canada - East - Beauharnois) | ca-east-bhs | 1-AZ |
| North America (Canada - East - Toronto) | ca-east-tor | 1-AZ |
| Asia-Pacific (Singapore - Singapore) | ap-southeast-sgp | 1-AZ |
| Asia-Pacific (Australia - Sydney) | ap-southeast-syd | 1-AZ |
| Asia-Pacific (India - Mumbai) | ap-south-mum | 1-AZ |

## Troubleshooting

If you encounter issues with your BGP session:

&bull; Verify that your ASN and IP prefixes are correctly configured. <br>&bull; Check for any conflicting announcements. <br>&bull; Ensure your firewall and network policies allow BGP traffic. <br>&bull; Contact our team for further assistance via email : <bgp_alpha@ovh.net>

## Go further

Join our [community of users](/links/community)