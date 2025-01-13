---
title: Tarification et gestion des NSX Edges OVHcloud
excerpt: Guide sur les options de tarification, configurations et personnalisation des NSX Edges pour VMware sur OVHcloud.
updated: 2025-01-13
---
# Informations concernant le mode de tarification et les configurations des NSX Edges
# Informations concernant le mode de tarification et les configurations des NSX Edges

## Objectif
Cette documentation a pour but d'expliquer les options de configuration des NSX Edges et les étapes pour les gérer dans un environnement VMware sur OVHcloud. Elle décrit également les limitations techniques et fournit des indications sur la manière d'adapter ces configurations aux besoins spécifiques.

---

## Prérequis
- **Accès à l’interface Manager OVHcloud** pour gérer vos NSX Edges.
- **Utilisation de VMware NSX 4.1.1** pour accéder aux options de personnalisation.
- Connaissance de base des concepts VMware et des fonctionnalités des NSX Edges.

---

## Principe général
### Configuration par défaut
Lors de la création d’un environnement VMware, OVHcloud fournit automatiquement :
- **2 NSX Edges Medium** :
  - 4 vCPU.
  - 8 Go RAM.

Cette configuration par défaut répond à la majorité des besoins standards en connectivité et en sécurité réseau.

### Personnalisation
Vous pouvez adapter votre infrastructure en fonction de vos besoins spécifiques :

1. **Taille des NSX Edges** :
   - Medium : 4 vCPU, 8 Go RAM.
   - Large : 8 vCPU, 32 Go RAM.
   - XL : 16 vCPU, 64 Go RAM.

2. **Nombre de NSX Edges** :
   - Minimum : 2 (configuration par défaut).
   - Maximum : Jusqu’à **10 NSX Edges par cluster**.

### Limitations
- **1 cluster NSX Edge par vDC**.
- **10 NSX Edges maximum par cluster** (limitation Broadcom/VMware).
- Les versions NSX 4.0.1 ne supportent pas :
  - La commande de nouveaux vDC sous NSX 4.1.1.
  - La modification ou l’ajout de NSX Edges.
---

## En pratique
### Étapes pour personnaliser les NSX Edges
1. **Commander de nouveaux NSX Edges** :
   - Connectez-vous à l’interface Manager OVHcloud.
   - Naviguez vers la section **Network** du dashboard Datacenter, puis accédez à **NSX Edges**.
   - Cliquez sur « Ajouter un Edge » et sélectionnez la taille souhaitée.
   > Toutes les Edges doivent être de la même taille : lorsqu’un Edge est ajouté, il sera automatiquement aligné sur la taille des autres Edges présents.

2. **Modifier la taille des NSX Edges existants** :
   - Accédez à la liste des NSX Edges dans le Manager.
   - Sélectionnez l’Edge à modifier.
   - Choisissez une nouvelle taille (Medium, Large ou XL) et appliquez les modifications.

3. **Supprimer des NSX Edges inutilisés** :
   - Identifiez l’Edge à supprimer dans l’interface Manager.
   - Cliquez sur « Supprimer » et confirmez l’action.
   
   **Note** : L’Edge doit être en mode résilience avant suppression pour garantir l’absence de trafic en cours.

---

## Aller plus loin
- Pour des informations détaillées sur les fonctionnalités des NSX Edges, consultez la [documentation technique VMware NSX](https://www.vmware.com/products/nsx.html).
- Les tarifs associés aux NSX Edges ne sont pas inclus dans cette documentation. Pour connaître les détails tarifaires ou obtenir une estimation, rendez-vous sur le site OVHcloud ou contactez le support via votre espace client.