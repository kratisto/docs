---
title: "Managed VCD - Limitations"
excerpt: "Découvrez les limitations de Managed VCD, y compris les restrictions de ressources et les contraintes de configuration."
updated: 2025-02-24
---

## Objectif

**Découvrez les limitations de Managed VCD, y compris les restrictions de ressources et les contraintes de configuration.**

> [!warning]
> Avant de créer un réseau ou une VM, assurez-vous de vérifier les limitations en consultant la documentation officielle :
>
> - [Création d'une VM sur VMware Cloud Director](/pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd-first-vm-creation/guide.fr-fr.md)
> - [Création de composants réseau via VCD](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd_network_creation/guide.fr-fr.md)

## Prérequis

Avant de commencer, consultez les guides suivants pour mieux comprendre VMware Cloud Director :

- [VMware Cloud Director - Concepts fondamentaux](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd-get-concepts/guide.fr-fr.md)
- [VMware Cloud Director - Concepts réseau](pages/hosted_private_cloud/hosted_private_cloud_powered_by_vmware/vcd_network_concepts/guide.fr-fr.md)

## En pratique

### Limitations générales

| Ressource | Standard | Advanced | Premium | Commentaires |
|-----------|---------|----------|---------|--------------|
| vCPU (par VM) | 32 | 32 | 32 | Nombre de vCPU disponibles par VM. |
| vCPU (cœurs par socket) | 1 | 1 | 1 | - |
| Nombre de sockets (par VM) | 1 | 1 | 1 | - |
| RAM (par VM) | 128 Go | 128 Go | 128 Go | Quantité maximale de RAM par VM (min. 0,5 Go). |
| Cartes réseau (par VM) | 5 | 10 | 10 | Nombre maximal d'adaptateurs réseau par VM. |
| Edge Gateway (par organisation) | N/A | 42 | 42 | Nombre maximal d'Edge Gateways par organisation. |
| IP publiques (par vDC) | N/A | 2 | 2 | Nombre d’IP publiques disponibles par vDC. |
| Stockage (par VM) | 1,5 To | 1,5 To | 1,5 To | Limite de stockage sur NFS/vSAN. |
| Snapshots (par VM) | 3 | 3 | 3 | Nombre maximal de snapshots par VM. |
| VMs (par vApp) | 128 | 128 | 128 | Nombre maximal de VMs autorisées par vApp. |
| VMs (par organisation) | 2000 | 4000 | 4000 | Nombre maximal de VMs par organisation. |
| vApps (par organisation) | 10 000 | 10 000 | 10 000 | Nombre maximal de vApps par organisation. |

### Limitations matérielles

| Ressource | Standard | Advanced | Premium | Commentaires |
|-----------|---------|----------|---------|--------------|
| Fréquence vCPU Min | 1 GHz | 1 GHz | 1 GHz | Dépend du matériel Baremetal. |
| Fréquence vCPU Max | 3 GHz | 3 GHz | 3 GHz | Dépend du matériel Baremetal. |
| Stockage par VM (VMDK) | 1,5 To | 1,5 To | 1,5 To | Limite de stockage sur VMDK. |
| Nombre maximal de Storage Policies | - | À valider | À valider | Besoin de confirmation sur l'existence d'une limite. |

## Aller plus loin

Si vous avez besoin d'une formation ou d'une assistance technique pour la mise en oeuvre de nos solutions, contactez votre commercial ou cliquez sur [ce lien](/links/professional-services) pour obtenir un devis et demander une analyse personnalisée de votre projet à nos experts de l’équipe Professional Services.

Posez des questions, donnez votre avis et interagissez directement avec l’équipe qui construit nos services Hosted Private Cloud sur la chaîne dédiée [Discord](https://discord.gg/ovhcloud).

Pour rejoindre et échanger avec notre [communauté d'utilisateurs](/links/community).