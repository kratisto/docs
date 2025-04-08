---
title: Restauration Bare Metal avec Veeam Backup Agent
excerpt: Restaurez votre système complet avec un ISO de récupération et des sauvegardes Veeam hébergées sur OVHcloud, en cloud ou sur site.
updated: 2025-04-08
---

## Objectif

**Ce guide explique comment restaurer l’intégralité de votre système à l’aide de la fonctionnalité de restauration Bare Metal de Veeam, en utilisant les sauvegardes stockées sur le service Cloud Connect d’OVHcloud.**

Vous apprendrez à :
    - Créer un ISO de récupération (un fichier permettant de démarrer votre machine si elle ne démarre plus)
    - L’utiliser pour accéder à votre dernière sauvegarde et la restaurer depuis l’infrastructure OVHcloud

Ce guide s’adresse à tous les clients OVHcloud utilisant la solution de sauvegarde Veeam, que votre infrastructure soit hébergée chez OVHcloud ou sur vos propres équipements.

Il est adapté si vous utilisez :
    - Un VPS sous Windows
    - Une instance Public Cloud Compute sous Windows
    - Un serveur Bare Metal avec Veeam Agent
    - Une machine virtuelle Hosted Private Cloud (PCC) sous Windows
    - Une machine physique ou virtuelle sur site, sous Windows ou Linux

> [!warning]
> Ce guide est basé sur le Veeam Agent pour Windows. Si vous utilisez le Veeam Agent pour Linux, la procédure est similaire, bien que l’interface soit en mode texte.

## Prérequis

Avant de commencer, assurez-vous de disposer des éléments suivants :

- Une [solution Veeam Enterprise](/links/hosted-private-cloud/veeam-enterprise) configurée avec OVHcloud 
- Un tenant provisionné avec l’Alpha Backup Agent
- Une machine sur laquelle le Veeam Backup Agent est installé et a déjà envoyé au moins une sauvegarde vers le dépôt Cloud Connect
- Un système d’exploitation pris en charge :
    - Windows Server 2012 ou version ultérieure, ou
    - Une distribution Linux compatible avec le Veeam Agent pour Linux
- Un accès administrateur à la machine
- Un moyen de démarrer à partir de l’ISO de récupération :
    - Utilisez une clé USB ou un disque externe si vous restaurez une machine physique
    - Utilisez un lecteur CD/DVD virtuel si vous restaurez une machine virtuelle

## En pratique

### Étape 1 : Créer l’ISO de récupération

Si votre ordinateur ne démarre plus, vous aurez besoin d’un ISO de récupération pour le relancer.

Voici comment le créer :

1. Ouvrez l’outil **Create Recovery Media** sur votre machine (il est inclus avec le Veeam Backup Agent).

    ![Launch the Create Recovery Media tool](images/baremetal_recovery_01.png){.thumbnail}

2. Veeam vous demandera si vous souhaitez inclure des pilotes supplémentaires.

    > **Conseil :** Si vous utilisez du matériel spécifique (comme un contrôleur RAID ou une clé Wi-Fi), sélectionnez les pilotes nécessaires. Sinon, les options par défaut conviennent généralement.

    ![Select drivers for boot image](images/baremetal_recovery_02.png){.thumbnail}

3. Choisissez l’emplacement d’enregistrement de l’ISO et donnez-lui un nom.

    ![Set ISO location and name](images/baremetal_recovery_03.png){.thumbnail}

4. Laissez l’outil terminer. Le fichier ISO sera généré.

    ![Recovery ISO creation complete](images/baremetal_recovery_04.png){.thumbnail}

    ![Recovery file](images/baremetal_recovery_05.png){.thumbnail}

Vous pouvez maintenant utiliser cet ISO pour créer une clé USB bootable à l’aide d’un outil comme Rufus — ou, si vous restaurez une VM, montez l’ISO directement depuis la console de gestion de la machine virtuelle.

### Étape 2 : Démarrer la machine à partir de l’ISO de récupération

Si votre système ne démarre plus et que vous devez le restaurer :

1. Branchez la clé USB ou montez l’ISO dans la console de votre VM, puis démarrez la machine à partir de celui-ci.

    > **Vous ne savez pas comment démarrer depuis une clé USB ?** Redémarrez votre machine physique et appuyez sur la touche indiquée (généralement F2, F12, ESC ou DEL) pour accéder au menu de démarrage.  
    > **Pour les machines virtuelles**, utilisez l’interface de votre hyperviseur (par exemple OpenStack, vSphere, Proxmox) pour monter l’ISO et démarrer dessus.

2. Une fois le système lancé, l’assistant de restauration Veeam s’ouvrira. Cliquez sur `Bare Metal Recovery`{.action}.

![Launch Bare Metal Recovery](images/step2_01.png){.thumbnail}

3. Sélectionnez `Network Storage`{.action} pour accéder à vos sauvegardes en ligne.

> [!warning]
> Si le réseau n’est pas détecté, vous devrez peut-être le configurer manuellement. Cliquez sur `Configure network settings`{.action} et chargez les pilotes manquants.

![Select Network Storage](images/step2_02.png){.thumbnail}

4. Sélectionnez `Veeam Cloud Connect repository`{.action}.

![Choose Cloud Connect Repository](images/step2_03.png){.thumbnail}

5. Saisissez l’adresse suivante lorsqu’il vous est demandé de renseigner le fournisseur de service :

```bash
backup.private.ovhcloud.dev
```

![Enter DNS](images/step2_04.png){.thumbnail}

6. Saisissez votre nom d’utilisateur et votre mot de passe pour vous connecter.

![Enter credentials](images/step2_05.png){.thumbnail}

7. Sélectionnez le `serveur`{.action} que vous souhaitez restaurer.

![Select server](images/step2_06.png){.thumbnail}

8. Choisissez le `point de restauration (date/heure)`{.action} auquel vous souhaitez revenir.

Nous vous recommandons d’utiliser la dernière sauvegarde réussie, sauf si vous avez une raison particulière de revenir à une version antérieure.

![Choose restore point](images/step2_07.png){.thumbnail}

9. Choisissez le `mode de restauration`{.action} adapté à votre situation (généralement **Entire computer**).

![Recovery mode](images/step2_08.png){.thumbnail}

10. Vérifiez le résumé, puis lancez la `restauration`{.action}.

![Launch restore - confirmation](images/step2_09.png){.thumbnail}

![Launch restore - progress](images/step2_10.png){.thumbnail}

> [!warning]
> Le processus de restauration peut prendre un certain temps selon la taille de votre sauvegarde et la vitesse de votre connexion Internet. Une fois terminé, votre système redémarrera avec l’état correspondant au point de restauration sélectionné.

## Aller plus loin

Si vous avez besoin de formation ou d’une assistance technique pour mettre en œuvre nos solutions, contactez votre Technical Account Manager ou cliquez sur [ce lien](/links/professional-services) pour demander un devis auprès de notre équipe Professional Services.

Posez vos questions, donnez votre avis et échangez directement avec l’équipe en charge du Hosted Private Cloud sur notre salon [Discord dédié](https://discord.gg/ovhcloud).

Échangez avec notre [communauté d’utilisateurs](/links/community).
