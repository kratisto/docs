---
title: "Guide post-migration vers Managed VCD"
excerpt: "Découvrez comment mettre à jour votre configuration réseau après la migration de votre environnement PCC vers Managed VCD."
updated: 2025-02-17
---

## Objectif  

Ce guide explique les étapes nécessaires pour configurer votre environnement après la migration de `Managed vSphere` vers `VMware Cloud Director (VCD)`.  

Ces ajustements sont essentiels pour assurer le bon fonctionnement de vos `machines virtuelles (VMs)` et de vos réseaux.  

## Prérequis  

- Accès à `VMware Cloud Director`.  
- Vous devez avoir accès au [Control Panel OVHcloud](/links/manager) et être administrateur technique du `Managed VMware vSphere` sur l’infrastructure OVHcloud.  

## En pratique  

### Étape 1 : Mettre à jour la configuration réseau des machines virtuelles  

Après la migration, vous devez ajuster la configuration réseau de vos `machines virtuelles (VMs)` en sélectionnant **une seule** des options suivantes :  

- **Option 1 : Passer la configuration réseau en `DHCP`** *(Recommandé)*  
   - Accédez aux paramètres réseau de chaque `VM`.  
   - Modifiez le mode d’attribution des IP et sélectionnez `DHCP`{.action}.  

   ![Paramètre DHCP](images/01-VCD-post-migration.png){.thumbnail}

   - Assurez-vous que `"Guest customization settings"`{.action} est défini sur `Disabled` avant de modifier les paramètres de l’interface réseau (NIC).  

   ![Paramètre Désactivé](images/02-VCD-post-migration.png){.thumbnail}

- **Option 2 : Mettre à jour le `Gateway CIDR` pour chaque réseau**  
   - Mettez à jour le `Gateway CIDR` pour qu’il corresponde au sous-réseau réellement utilisé sur chaque réseau.  
   - Cette étape est essentielle pour assurer la connectivité et éviter les conflits de configuration.  

   ![CIDR de la passerelle](images/03-VCD-post-migration.png){.thumbnail}

### Étape 2 : Gérer le problème d’adressage IP dans `VCD`  

Lors de la migration, les `VLANs` sont pré-créés avec des **`Gateway CIDRs` temporaires**, car les sous-réseaux exacts des VMs ne sont pas connus à l’avance.  

Cela peut entraîner des erreurs d’attribution d’IP si les paramètres ne sont pas ajustés après la migration.  

#### **Problème détecté**  
- Si une adresse IP statique est attribuée manuellement à une `VM` et qu’elle ne correspond pas au `Gateway CIDR` préconfiguré, l’attribution échoue.  
- Il est impossible de créer ou de modifier une `VM` avec une adresse IP manuelle hors du `Gateway CIDR` défini initialement.  

#### **Solutions possibles**  

1. **Utiliser le mode `DHCP`** *(Recommandé)*  
   - L’activation du mode `DHCP` permet d’attribuer une adresse automatiquement, même si l’OS de la `VM` est configuré en statique.  
   - Cette solution fonctionne aussi bien pour les **`réseaux isolés`** que pour les **`VM Networks`**.  

   ![Mode DHCP](images/04-VCD-post-migration.png){.thumbnail}

2. **Mettre à jour manuellement le sous-réseau en `mode statique`**  
   - Identifier et configurer manuellement le bon sous-réseau pour chaque réseau.  
   - Il n’existe pas de méthode automatique pour récupérer ces informations.  

3. **Créer un nouveau `segment`**  
   - Les clients peuvent créer un nouveau `network segment` avec le sous-réseau correct.  
   - Cette solution est applicable uniquement si le client possède **un seul** bloc d’adresses IP publiques. 

## Aller plus loin  

Si vous avez des questions ou besoin d’assistance, plusieurs options sont à votre disposition :  

- **Votre `Account Manager` ou `Technical Account Manager` assigné**  
- **Notre équipe `OVHcloud Professional Services`** : [https://www.ovhcloud.com/fr/professional-services/](https://www.ovhcloud.com/fr/professional-services/)  

Échangez avec notre [communauté d’utilisateurs](/links/community).