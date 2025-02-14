---
title: "Guide post-migration vers Managed VCD"
excerpt: "Découvrez comment adapter votre configuration réseau après la migration de votre environnement PCC vers Managed VCD."
updated: 2025-02-13
---

## Objectif

Découvrez les étapes essentielles pour configurer votre environnement après la migration de votre infrastructure PCC vers VMware Cloud Director (VCD). 

Ces ajustements sont nécessaires pour assurer le bon fonctionnement de vos machines virtuelles et de vos réseaux.

## Prérequis

- Accès à **VMware Cloud Director**.  
- Droits administratifs pour modifier les paramètres des machines virtuelles et des réseaux.

## En pratique

### Étape 1 : Mettre à jour la configuration réseau des machines virtuelles  

Après la migration, il est impératif de modifier la configuration réseau de vos machines virtuelles en choisissant une des options suivante :

- Option 1 : **Passer la configuration réseau en mode DHCP**  
   - Accédez aux paramètres réseau de chaque VM. 

   - Modifiez le mode d’attribution des IP et sélectionnez **DHCP**. 

   ![DHCP setting](images/01-VCD-post-migration.png){.thumbnail}
 
   - Assurez-vous que l’option **"Guest customization settings"** est définie sur **Désactivé** avant de modifier les paramètres de l’interface réseau (NIC).  

   ![Disabled setting](images/02-VCD-post-migration.png){.thumbnail}

- Option 2 : **Mettre à jour les CIDR des passerelles**  
   - Adaptez les CIDR des passerelles aux sous-réseaux réellement utilisés sur chaque réseau.  
   - Cette étape est essentielle pour éviter tout conflit de configuration et assurer la connectivité des VMs.  

   ![Gateway CIDR](images/03-VCD-post-migration.png){.thumbnail}

### Étape 2 : Gérer le problème d’adressage IP dans VCD  

Lors de la migration, les VLANs sont pré-créés avec des **CIDR de passerelles temporaires**, car les sous-réseaux exacts des VMs ne sont pas connus à l’avance. 

Cela peut entraîner des erreurs d’attribution d’IP si les paramètres ne sont pas ajustés après la migration.

#### **Problème détecté**  
- Si une adresse IP statique est attribuée manuellement à une VM et qu’elle ne correspond pas au CIDR de la passerelle préconfigurée, l’attribution échoue.  
- Il est impossible de créer ou de modifier une VM avec une adresse IP manuelle hors du CIDR de la passerelle définie initialement.  

#### **Solutions possibles**  

1. **Utiliser le mode DHCP** *(Recommandé)*  
   - L’activation du mode DHCP permet d’attribuer une adresse automatiquement, même si l’OS de la VM est configuré en statique.  
   - Cette solution fonctionne aussi bien pour les **réseaux isolés** que pour les **VM Networks**.  

2. **Passer en mode manuel et définir le bon sous-réseau**  
   - Identifier et configurer manuellement le bon CIDR sur chaque réseau.  
   - Il n’existe pas de méthode automatique pour récupérer ces informations.  

      ![DHCP mode](images/04-VCD-post-migration.png){.thumbnail}

3. **Créer un nouveau segment réseau**  
   - Un nouveau segment peut être créé avec le sous-réseau correct.  
   - Cette solution est applicable uniquement si le client possède **un seul** bloc d’adresses IP publiques.  

## Aller plus loin  

Si vous avez des questions ou besoin d’assistance, plusieurs options sont à votre disposition :  

- **Votre Account Manager ou Technical Account Manager assigné**  
- **Notre équipe Professional Services OVHcloud** : [https://www.ovhcloud.com/fr/professional-services/](https://www.ovhcloud.com/fr/professional-services/)  

Nous vous recommandons vivement de lire attentivement cette documentation et d’adapter votre environnement en conséquence pour assurer une transition optimale vers Managed VCD.  

Échangez avec notre [communauté d’utilisateurs](/links/community).
