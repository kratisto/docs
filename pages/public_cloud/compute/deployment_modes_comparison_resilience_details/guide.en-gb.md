---
title: "Comparison and resilience of S3 Deployment Modes - Understanding 3-AZ / 1-AZ / Local Zones"
excerpt: "Explore OVHcloud's deployment modes"
updated: 2024-12-18
---

<style>
details>summary {
    color:rgb(33, 153, 232) !important;
    cursor: pointer;
}
details>summary::before {
    content:'\25B6';
    padding-right:1ch;
}
details[open]>summary::before {
    content:'\25BC';
}
</style>

## Objective

OVHcloud offers several deployment modes for its service, like with les [Compute instances](/links/public-cloud/compute), [S3 Object Storage](/links/public-cloud/object-storage), [Containers & Orchestration](/links/public-cloud/kubernetes), each tailored to specific needs regarding resilience, availability, performance, and latency. This document provides a detailed explanation of the characteristics of the characteristics of each deployment mode (1-AZ, 3-AZ, Local Zones), explaining the benefits and limitations of each.

By offering a clear and detailed comparison, this guide will enable users to make an informed decision based on their specific priorities, whether it's ensuring high availability for critical applications, minimizing costs while providing fault tolerance, or meeting local compliance and ultra-low latency requirements.

Additionally, we will highlight the real-world challenges users may face, such as impacts on business continuity, scalability of services, and cost management in each deployment mode. This guide is particularly useful for cloud architects, IT managers, and developers looking to optimize their infrastructure based on specific business and technical needs.

## Concepts

OVHcloud provides a robust and adaptable infrastructure, designed to meet a wide variety of use cases through deployment modes that balance cost-efficiency, redundancy, and fault tolerance. This flexibility extends across OVHcloud's entire portfolio of services, enabling customers to customize solutions to meet their specific requirements.

1. **1-AZ Region**: Ideal for general workloads such as storage, backup, or applications where cost optimization is the priority. These regions provide a solid foundation of resilience with single-zone deployment, balancing reliability and performance.
2. **3-AZ Region**: Designed for business-critical applications requiring high availability and data durability. With replication across three availability zones, this mode minimizes downtime risks and ensures continuity even in the event of major disruptions.
3. **Local Zones**: Perfect for use cases demanding low latency and geographical compliance. By hosting infrastructure closer to end-users, Local Zones enable seamless performance for edge computing, gaming, and content delivery.

The principles of resilience and fault tolerance seen in these deployment models extend across OVHcloud's services, including:

- **Compute instances**: Offering failover and scaling options in single or multi-zone configurations to match the redundancy levels required by your workload.
- **Databases**: Supporting high availability with distributed setups across regions or zones for critical applications.
- **Network**: Ensuring connectivity through diverse routes and disaster recovery mechanisms for uninterrupted access.
- **Containers and Orchestrations**: Providing cluster resilience with multi-zone deployments, guaranteeing consistent performance and fault isolation.

## Deployment modes

> [!primary]
>
> OVHcloud offers multiple region deployment modes, each tailored to meet diverse business requirements by providing varying levels of redundancy, fault tolerance, and geographical distribution. These deployment modes ensure flexibility, scalability, and resilience across all OVHcloud services, empowering customers to align their infrastructure with their operational priorities:

### 1-AZ Region

#### Infrastructure and Redundancy

A 1-AZ Region consists of a **single availability zone that spans multiple data centers within the same region**, utilizing a 2N+1 redundancy design. This setup ensures resilience against server rack and disk failures, but it is vulnerable to a complete data center outage. While services and data are protected against local hardware failures (e.g., server or disk issues), a complete data center failure could impact service availability, even if other data centers within the same availability zone remain operational.

#### Characteristics

- **Erasure Coding:** Implements mechanisms such as replication or erasure coding (depending on the service) to ensure continuity in case of hardware failures. Data is distributed across multiple servers and storage units within the availability zone to mitigate the impact of localized issues.
- **Cost-Effectiveness:** This deployment model is cost-efficient, ideal for general-purpose workloads, development environments, and backups. It prioritizes affordability over enhanced fault tolerance provided by multi-AZ configurations.

#### Limitations

- **Outage Risk:** If a data center experiences an outage, data or services may become unavailable, especially if the affected data center hosts critical services. However, redundancy is maintained within the availability zone for hardware failures.

> [!success]
>
>  To improve resilience for critical applications in a 1-AZ Region, consider using asynchronous replication for added protection. This can help reinforce both application and data resiliency. Another option to mitigate this risk is using a [**3-AZ deployment mode**](#3azregion).

#### Redundancy Specifications for 1-AZ

| Specification         | Description                                                               |
|-------------------|---------------------------------------------------------------------------|
| **Redundancy Type**   | 2N+1 across multiple data centers                                         |
| **Fault Tolerance**   | Protects against server and disk failures; data center outages may impact services.           |
| **Use Case Examples** | Suitable for general-purpose applications, testing, development, and backups.                                    |


#### Scaling

In a 1-AZ Region, scaling options are somewhat limited due to the single availability zone. Here's how scaling works in this setup:

- **Limited to a single zone:** Horizontal scaling (adding instances across other zones) is not possible since there is only one availability zone. Vertical scaling (increasing the capacity of an instance or service) is feasible but does not provide fault tolerance across regions.
- **Typical use case:** Suitable for development environments, applications with low availability requirements, and scenarios where resilience is not a priority, but internal redundancy is still needed to handle hardware failures.

#### Architecture example

/// details | Internal management application

> [!primary]
>
> **Scenario:**
>
> An organization utilizes the 1-AZ Region mode for its internal management application and backup services. This setup is ideal for applications that do not require high availability 24/7, but still need redundancy to protect against hardware failures.

Architecture:
- **Single Availability Zone (AZ):** Hosted in one availability zone with multiple data centers, ensuring basic fault tolerance within the zone.
- **Internal replication:** Data is replicated internally to protect against disk or server failures within the zone.
- **Backup Integration:** The application uses S3 storage for regular backups, ensuring data can be restored if needed.
- **Compute Instances:** Basic application tasks are handled by compute instances in the same AZ, with auto-scaling for resource management.

///

### 3-AZ Region

#### Infrastructure and Redundancy

3-AZ Regions consist of **three independent availability zones**, each with isolated power, cooling, and network systems, providing true fault isolation. This setup ensures service availability even in the event of an entire availability zone failure. The architecture enables the replication of data and services across zones, ensuring that if one zone goes down, the others can continue to serve traffic and maintain application performance.

#### Characteristics

- **High Availability:** Data remains available for both read and write operations, even in the event of a zone failure. This architecture is ideal for applications requiring fault tolerance, as the data is replicated across all three availability zones. Even in the event of a disruption in one zone, service continuity is maintained.
- **Fault isolation:** Each availability zone is independent in terms of power, networking, and cooling, which means issues in one zone won’t directly impact the others. This leads to a higher level of redundancy and ensures that service interruptions are minimized.

#### Ideal Use Cases

3-AZ Regions are perfect for mission-critical and availability-sensitive applications where data governance requires continuous data availability, such as e-commerce, healthcare platforms, financial services, or live-streaming applications.

> [!success]
>
> While this setup provides strong protection, it may not be completely resilient in the case of an unlikely regional outage. For even greater data availability and resilience, solutions like multi-region asynchronous replication can be implemented.

#### Performance Specifications for 3-AZ

| Specification         | Description                                                               |
|-------------------|---------------------------------------------------------------------------|
| **Connectivity**      | Low latency between availability zones, ensuring fast and reliable communication.                                    |
| **High Availability** | Services remain accessible even during an availability zone failure, ensuring minimal disruption.                      |
| **Use Case Examples** | Suitable for mission-critical applications, streaming, e-commerce, healthcare, and other high-availability workloads. |

#### Scaling

In a 3-AZ Region, scaling is more flexible, offering the ability to scale horizontally across multiple availability zones. Here’s what you can expect:

- **Optimized horizontal scaling:** With replication and distribution of services across three independent zones, horizontal scaling becomes more seamless, ensuring high availability, optimal performance, and efficient resource distribution.
- **Optimized load balancing:** With multiple availability zones, load balancing and traffic distribution are optimized, ensuring better performance and resilience.
- **Typical use case:** Ideal for critical applications that require high availability, such as e-commerce platforms or financial services, which demand both consistent performance and resilience against zone failures.

#### Architecture example

/// details | E-commerce platform

> [!primary]
>
> **Scenario:**
>
> An e-commerce platform that demands high availability and performance. This deployment mode ensures service continuity even in the event of a failure in one entire availability zone.

Architecture:
- **Three availability zones** (AZs) distributed geographically, providing true fault isolation and redundancy.
- **Real-time data replication** between zones ensures continuous access to application data, even during a failure in one of the zones.
- **Redundant compute instances** deployed across multiple zones to provide failover capabilities and guarantee consistent performance.
- **Load balancers** to efficiently distribute traffic between availability zones, maintaining smooth user experience despite potential disruptions.

///

### Local Zones

#### Design and Flexibility

Local Zones are designed to bring OVHcloud services closer to end-users, reducing latency and helping meet local compliance requirements. These zones are ideal for applications that demand low-latency performance and real-time processing, such as edge computing and content delivery.

#### Benefits for Compliance and Cost

- **Reduced Network Costs:** Local Zones help minimize data travel distance, lowering network costs and improving performance.
- **Localized Storage:** Supports compliance with regional data localization requirements, making it ideal for applications subject to specific regulatory frameworks.

#### Limitations

- **Single Zone Limitation:** Local Zones are limited to a single availability zone and do not provide cross-zone redundancy, which limits data recovery options in the event of a disaster.

#### Use Case Specifications for Local Zones

| Advantage        | Description                                           |
|------------------|-------------------------------------------------------|
| **Performance**      | Ultra-low latency, ensuring optimal performance for real-time applications.             |
| **Data Compliance**  | Facilitates compliance with regional data localization and regulatory requirements. |
| **Use Case Examples**| Ideal for online gaming, video conferencing, edge computing, and other latency-sensitive applications. |

#### Scaling

In Local Zones, scaling is designed to meet the demands of low-latency applications while being restricted to a single availability zone. Here’s how scaling is structured:

- **Latency reduction, but with constraints:** Scaling in a Local Zone is primarily aimed at minimizing latency for real-time applications. However, since it is limited to a single availability zone, scaling must be carefully planned to maximize performance while avoiding local failure risks.
- **Typical use case:** Perfect for ultra-low-latency applications like online gaming, augmented reality, or live video streaming, where every millisecond counts, and low latency is crucial for user experience.

#### Architecture example

/// details | Online gaming platform or video streaming service

> [!primary]
>
> **Scenario:**
>
> A real-time online gaming platform or a video streaming service that requires ultra-low latency and high performance for users within a specific geographic region.

Architecture:
- **Local Zones:** located near the user base, significantly reducing latency and improving overall performance.
- **Processing Servers and Storage:** Deployed within the Local Zones for fast data access and responsiveness.
- **Regulated Data:** Stored within the Local Zones for compliance with data localization laws, reducing bandwidth costs.
- **Load Balancers:** Redirect traffic to another Local Zone or availability zone during a failure, ensuring minimal downtime and continuous service.

///

### Comprehensive Comparison Table

| Characteristics        | 1-AZ Region                         | 3-AZ Region                     | Local Zones                              |
|------------------------|-------------------------------------|---------------------------------|------------------------------------------|
| **Deployment Structure**   | Single availability zone            | Three independent availability zones | Single availability zone                |
| **Redundancy**             | 2N+1 internal                       | Cross-zone redundancy            | Local triple replication                |
| **Data Availability**      | Limited during data center outages, protected against server/disk failures | Maintained across zones, resilient to zone outages | Limited during data center outages, protected against server/disk failures |
| **Latency**                | Low for close end-users                            | Low for close end-users and ultra low between availability zones   | Low for close end-users |
| **Ideal Use Cases**        | Development, staging environments, cost-sensitive applications, non-critical services | High-availability applications, critical business services, disaster recovery, and mission-critical workloads | Real-time applications, edge computing, gaming, video streaming, regulatory-compliant services |
| **Cost**                   | Lower                               | Higher due to increased redundancy | Dependent on the specific Local Zones and required latency performance |

## Go Further

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](/links/professional-services) to get a quote and ask our Professional Services experts for assisting you on your specific use case.

Join our [community of users](/links/community) and visit our [Discord channel](https://discord.gg/ovhcloud).
