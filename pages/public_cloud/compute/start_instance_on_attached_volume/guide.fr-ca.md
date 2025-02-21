---
title: 'Comment démarrer une instance de Cloud public sur un volume amorçable'
excerpt: 'Découvrez comment démarrer une instance sur un volume amorçable'
updated: 2025-02-20
---

## Objectif

Les instances Public Cloud sont livrées avec un disque d’origine copié à partir d’une image système (Debian 12, Windows Server, etc.). Il est également possible d’utiliser des volumes supplémentaires, il s’agit de disques persistants qui permettront de stocker des données.

Vous pouvez également déployer un système d'exploitation depuis et vers un volume. L'instance Public Cloud démarrera alors sur ce volume à la place du disque d'origine.

**Ce guide vous explique comment démarrer une instance sur un volume attaché.**

![public-cloud](images/3704.png){.thumbnail}

> [!success]
>
> OpenStack vous permet nativement de démarrer à partir d'un volume.
> Il s'agit de rendre le volume amorçable et de démarrer l'instance à partir de ce volume.
> Les modifications entraîneront la disparition du disque d'origine au fur et à mesure que le nouveau volume prendra le relais.
> Les fonctionnalités décrites dans ce guide éliminent la nécessité d’accéder au disque d’origine et tirent donc parti du volume.

> [!warning]
>
> Concernant la version actuelle d'OpenStack, avec un volume amorçable, le mode rescue-pro n'est pas disponible sur une instance sauvegardée en volume.
>

## Prérequis

- [Accès à l’interface Horizon](/pages/public_cloud/compute/loading_presentation_horizon)
- [Charger les variables d'environnement OpenStack](/pages/public_cloud/compute/loading_openstack_environment_variables)


## Instructions

### Création d’un volume de démarrage à partir d’une image.

> [!tabs]
> **Horizon**
>> Connectez-vous à l'[interface Horizon](https://horizon.cloud.ovh.net/auth/login/).
>>
>> Sélectionnez la région appropriée dans le menu déroulant en haut à gauche.
>>
>> Dans l'onglet Projet, ouvrez l'onglet `Volumes`{.action} et cliquez sur la catégorie `Volumes`{.action}.
>>
>> Cliquez sur `Create Volume`{.action}.
>>
>> ![public-cloud](images/create-a-volume-2.png){.thumbnail width="800"}
>>
>> Dans la boîte de dialogue qui s'affiche, entrez ou sélectionnez les valeurs suivantes :
>>
>> | Information | Description |
>> | --- | --- |
>> |  Volume Name | Spécifiez un nom pour le volume |
>> | Description | Facultatif, fournir une brève description du volume |
>> | Volume Source | Choisissez l'option `Image`.<br><br> ![public-cloud](images/create-a-volume-3.png){.thumbnail} |
>> | Use image as a source | Vous pouvez sélectionner l'image dans la liste.<br><br> ![public-cloud](images/create-a-volume-4.png){.thumbnail} |
>> | Type | Dépend du type de volume que vous souhaitez utiliser |
>> | Size (GB) | Taille du volume en gigaoctets (Gio) |
>> | Availability Zone | nova <br><br> ![public-cloud](images/create-a-volume-5.png){.thumbnail} |
>>
>> Cliquez sur `Create Volume`{.action}.
>>
>> Le volume sera dans l'état *`creating`* puis dans l'état *`downloading`* avant d'être disponible.
>>
>> ![public-cloud](images/create-a-volume-8.png){.thumbnail width="800"}
>>
>> Comme vous pouvez le voir sur l'image ci-dessous ou si vous cliquez sur le nom du volume, il est défini comme amorçable (*bootable*).
>>
>> ![public-cloud](images/create-a-volume-9.png){.thumbnail width="800"}
>>
> **Client OpenStack**
>> Vous pouvez créer un volume de démarrage à partir d'une image, d'un volume ou d'un instantané existant. Cette procédure vous montre comment créer un volume à partir d'une image et utiliser le volume pour démarrer une instance.
>>
>> ```console
>> $ openstack image list
>> ```
>>
>> > [!primary]
>> >
>> > Notez l'ID ou le nom de l'image que vous souhaitez utiliser.
>>
>> Créez un volume amorçable de 10 Go à haute vitesse nommé **volume_ubuntu** à partir d'une image Ubuntu 24.04 :
>>
>> Vous pouvez installer une image sur un volume en utilisant l'argument `--image` :
>>
>> ```console
>> $ openstack volume create --type high-speed --image 2c2e28dc-9124-49c3-b92d-7f00bd83ac86 --size 10 volume_ubuntu
>> +---------------------+--------------------------------------+
>> | Field | Value |
>> +---------------------+--------------------------------------+
>> | attachments | [] |
>> | availability_zone | nova |
>> | bootable | false |
>> | consistencygroup_id | None |
>> | created_at | 2025-02-06T17:04:34.000000 |
>> | description | None |
>> | encrypted | False |
>> | id | d7611318-fd7b-4b6a-8a7a-8d368049f747 |
>> | multiattach | False |
>> | name | volume_ubuntu |
>> | properties | |
>> | replication_status | None |
>> | size | 20 |
>> | snapshot_id | None |
>> | source_volid | None |
>> | status | creating |
>> | type | high-speed |
>> | updated_at | None |
>> | user_id | 1a67934f87ef481d9cb617a913bfa8bb |
>> +---------------------+--------------------------------------+
>> ```
>>
>> Dans cette commande, **2c2e28dc-9124-49c3-b92d-7f00bd83ac86** est l'ID d'image Ubuntu 24.04.
>>
>> > [!primary]
>> >
>> > Cinder rend un volume amorçable lorsque le paramètre `--image` est passé.
>>

### Démarrer une instance en utilisant un volume amorçable

> [!tabs]
> **Horizon**
>> Connectez-vous à l'[interface Horizon](https://horizon.cloud.ovh.net/auth/login/).
>>
>> Sélectionnez la région appropriée dans le menu déroulant en haut à gauche.
>>
>> Dans l'onglet Projet, ouvrez l'onglet `Compute`{.action} et cliquez sur `Instances`{.action} catégorie.
>>
>> Cliquez sur `Launch Instance`{.action}.
>>
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-1.png){.thumbnail width="800"}
>>
>> Dans la boîte de dialogue `Launch Instance`, dans l'onglet Source, choisissez « Volume » dans le champ `Select Boot Source`.
>>
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-3.png){.thumbnail}
>>
>> Un nouveau champ de sélection de volume s'affiche. Vous pouvez sélectionner le volume précédemment créé dans la liste.
>>
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-4.png){.thumbnail}
>>
>> Cliquez sur `Launch Instance`{.action}.
>>
>> L'instance sera dans l'état `build` puis dans l'état `Block Device Mapping` avant d'être disponible.
>>
>> L'instance finira par avoir le volume attaché.
>>
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-9.png){.thumbnail width="800"}
>>
> Créez une instance, en spécifiant le volume amorçable **volume_ubuntu** comme périphérique d'amorçage.
>>
>> ```console
>> openstack server create --volume volume_ubuntu --flavor d2-2 --key-name publickey --nic net-id=Ext-Net InstanceTest
>> ```
>>
>> Lister les volumes pour s'assurer que le statut a changé en in-use et que le volume rapporte correctement l'attachement :
>>
>> ```console
>> $ openstack volume list
>> +--------------------------------------+---------------+--------+------+--------------------------------------+
>> | ID | Name | Status | Size | Attached to |
>> +--------------------------------------+---------------+--------+------+--------------------------------------+
>> | d7611318-fd7b-4b6a-8a7a-8d368049f747 | volume_ubuntu | in-use | 10 | Attached to InstanceTest on /dev/sda |
>> +--------------------------------------+---------------+--------+------+--------------------------------------+
>> ```
>>
>> Lister les volumes attachés à l'instance **InstanceTest** :
>>
>> ```console
>> $ openstack server volume list InstanceTest
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | ID | Device | Server ID | Volume ID | Tag |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | d7611318-fd7b-4b6a-8a7a-8d368049f747 | /dev/sda | 5d97c190-f2e3-4af4-a010-6fa7bffbf88b | d7611318-fd7b-4b6a-8a7a-8d368049f747 | None |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> ```
>>
>> > [!primary]
>> >
>> > Vous pouvez également créer une instance, en utilisant l'image choisie et en demandant le comportement « boot from volume ».
>> 
>> ```console
>> $ openstack server create --flavor d2-2 --key-name publickey --nic net-id=Ext-Net --image b680f0aa-8eb8-4ac8-b008-2a90bb71af4f --boot-from-volume 10 InstanceTest2
>> +-----------------------------+---------------------------------------------+
>> | Field | Value |
>> +-----------------------------+---------------------------------------------+
>> | OS-DCF:diskConfig | MANUAL |
>> | OS-EXT-AZ:availability_zone | |
>> | OS-EXT-STS:power_state | NOSTATE |
>> | OS-EXT-STS:task_state | scheduling |
>> | OS-EXT-STS:vm_state | building |
>> | OS-SRV-USG:launched_at | None |
>> | OS-SRV-USG:terminated_at | None |
>> | accessIPv4 | |
>> | accessIPv6 | |
>> | addresses | |
>> | adminPass | dP4e4iY3eWWC |
>> | config_drive | |
>> | created | 2025-02-06T17:20:06Z |
>> | flavor | d2-2 (dc3fe9e7-e374-4ad8-b200-fa3bdf45069f) |
>> | hostId | |
>> | id | a4632249-e1b4-4047-be1c-87f8b0328f7c |
>> | image | N/A (booted from volume) |
>> | key_name | publickey |
>> | name | InstanceTest2 |
>> | progress | 0 |
>> | project_id | d7fb756ae2c24b1cb8630ec7f56ee4a8 |
>> | properties | |
>> | security_groups | name='default' |
>> | status | BUILD |
>> | updated | 2025-02-06T17:20:06Z |
>> | user_id | 1a67934f87ef481d9cb617a913bfa8bb |
>> | volumes_attached | |
>> +-----------------------------+---------------------------------------------+
>> ```
>>
>> Dans la commande ci-dessus, `b680f0aa-8eb8-4ac8-b008-2a90bb71af4f` est l'ID image Debian 12.
>>
>> - Lister les volumes :
>> 
>> Lister les volumes pour s'assurer que l'état est passé à *in-use* et que le volume signale correctement le rattachement.
>> ```console
>> $ openstack volume list
>> +--------------------------------------+---------------+--------+------+----------------------------------------+
>> | ID | Name | Status | Size | Attached to |
>> +--------------------------------------+---------------+--------+------+----------------------------------------+
>> | 27f8332d-8bfd-4515-b0a8-18667ae50ff8 | | in-use | 10 | Attached to InstanceTest2 on /dev/sda |
>> | d7611318-fd7b-4b6a-8a7a-8d368049f747 | volume_ubuntu | in-use | 10 | Attached to InstanceTest on /dev/sda |
>> +--------------------------------------+---------------+--------+------+----------------------------------------+
>> ```
>>
>> Listez le volume sur le serveur pour vous assurer qu'il est correctement rattaché.
>> ```console
>> $ openstack server volume list InstanceTest
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | ID | Device | Server ID | Volume ID | Tag |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | d7611318-fd7b-4b6a-8a7a-8d368049f747 | /dev/sda | 5d97c190-f2e3-4af4-a010-6fa7bffbf88b | d7611318-fd7b-4b6a-8a7a-8d368049f747 | None |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> ```

## Aller plus loin

Échangez avec notre [communauté d'utilisateurs](/links/community).