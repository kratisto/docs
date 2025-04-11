---
title: 'Cómo iniciar una instancia de Public Cloud en un volumen de arranque'
excerpt: 'Cómo iniciar una instancia en un volumen de arranque'
updated: 2025-02-26
---

## Objetivo

Las instancias de Public Cloud se entregan con un disco original copiado de una imagen de sistema (Debian 12, Windows Server, etc.). También es posible utilizar volúmenes adicionales, que son discos persistentes que permitirán almacenar datos.

También puede implementar un sistema operativo desde y hacia un volumen. La instancia de Public Cloud se iniciará en ese volumen en lugar del disco original.

**Esta guía explica cómo iniciar una instancia en un volumen asociado.**

![public-cloud](images/img_3704.jpg){.thumbnail}

> [!success]
>
> OpenStack permite arrancar de forma nativa desde un volumen.
> Consiste en hacer que el volumen sea iniciable y arrancar la instancia desde ese volumen.
> Los cambios harán que desaparezca el disco original a medida que el nuevo volumen tome el relevo.
> Las funcionalidades descritas en esta guía eliminan la necesidad de acceder al disco original y, por lo tanto, aprovechan el volumen.

> [!warning]
>
> Con la versión actual de OpenStack, el modo rescue-pro no está disponible en una instancia iniciada a través de un volumen de arranque.
>

## Requisitos

- [Acceso a Horizon](/pages/public_cloud/public_cloud_cross_functional/introducing_horizon)
- [Cargar variables de entorno OpenStack](/pages/public_cloud/public_cloud_cross_functional/loading_openstack_environment_variables)

## Instrucciones

### Creación de un volumen de arranque a partir de una imagen.

> [!tabs]
> **Horizon**
>> Conéctese al [interface Horizon](https://horizon.cloud.ovh.net/auth/login/).
>>
>> Seleccione la región adecuada en el menú desplegable de la parte superior izquierda.
>>
>> En la pestaña Proyecto, abra la pestaña `Volumes`{.action} y haga clic en la categoría `Volumes`{.action}.
>>
>> Haga clic en `Crear volumen`{.action}.
>>
>> ![public-cloud](images/create-a-volume-2.png){.thumbnail width="800"}
>>
>> En el cuadro de diálogo que aparece, introduzca o seleccione los siguientes valores:
>>
>> | Información | Descripción |
>> | --- | --- |
>> | Volume Name | Especifique un nombre para el volumen |
>> | Description | Opcional, proporcionar una breve descripción del volumen |
>> | Volumen De Origen | Elija la opción `Image`.<br><br> ![public-cloud](images/create-a-volume-3.png){.thumbnail} |
>> | Use image as a source | Puede seleccionar la imagen de la lista.<br><br> ![public-cloud](images/create-a-volume-4.png){.thumbnail} |
>> | Type | Depende del tipo de volumen que desee utilizar |
>> | Size (GB) | Tamaño del volumen en gigabytes (GiB) |
>> | Availability Zone | nova <br><br> ![public-cloud](images/create-a-volume-5.png){.thumbnail} |
>>
>> Haga clic en `Create Volume`{.action}.
>>
>> El volumen tendrá el estado *`creating`* y el estado *`downloading`* antes de estar disponible.
>>
>> ![public-cloud](images/create-a-volume-8.png){.thumbnail width="800"}
>>
>> Como puede ver en la siguiente imagen o si hace clic en el nombre del volumen, se define como volumen de arranque (*bootable*).
>>
>> ![public-cloud](images/create-a-volume-9.png){.thumbnail width="800"}
>>
> **Cliente OpenStack**
>> Puede crear un volumen de arranque a partir de una imagen, un volumen o un snapshot de un volumen existente. Este procedimiento muestra cómo crear un volumen a partir de una imagen y cómo utilizar el volumen para iniciar una instancia.
>>
>> ```console
>> $ openstack image list
>> ```
>>
>> > [!primary]
>> >
>> > Anote el ID o el nombre de la imagen que desea utilizar.
>>
>> Cree un volumen de arranque de 10 GB a alta velocidad denominado **volume_ubuntu** a partir de una imagen Ubuntu 24.04:
>>
>> Puede instalar una imagen en un volumen utilizando el argumento `--image`:
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
>> 
>> En este comando, **2c2e28dc-9124-49c3-b92d-7f00bd83ac86** es el ID de imagen Ubuntu 24.04.
>> 
>> > [!primary]
>> >
>> > Cinder convierte un volumen de arranque cuando se pasa el parámetro `--image`.
>> 

### Iniciar una instancia utilizando un volumen de arranque

> [!tabs]
> **Horizon**
>> Conéctese al [interface Horizon](https://horizon.cloud.ovh.net/auth/login/).
>> 
>> Seleccione la región adecuada en el menú desplegable de la parte superior izquierda.
>> 
>> En la pestaña Proyecto, abra la pestaña `Compute`{.action} y haga clic en `Instances`{.action} categoría.
>> 
>> Pulse `Launch Instance`{.action}.
>> 
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-1.png){.thumbnail width="800"}
>> 
>> En el cuadro de diálogo `Launch Instance`, complete la información solicitada. Para más información, consulte la guía [Crear una instancia desde Horizon](/pages/public_cloud/compute/create_instance_in_horizon).
>>
>> En la pestaña Source, seleccione "Volume" en el campo `Select Boot Source`.
>> 
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-3.png){.thumbnail}
>> 
>> Aparecerá un nuevo campo de selección de volumen. Puede seleccionar el volumen creado anteriormente de la lista.
>> 
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-4.png){.thumbnail}
>> 
>> Haga clic en `Launch Instance`{.action}.
>> 
>> La instancia tendrá el estado `build` y el estado `Block Device Mapping` antes de estar disponible.
>> 
>> La instancia terminará teniendo el volumen asociado.
>> 
>> ![public-cloud](images/create-an-instance-with-a-bootable-volume-9.png){.thumbnail width="800"}
>> 
> **Cliente OpenStack**
>> Cree una instancia, especificando el volumen de arranque **volume_ubuntu** como dispositivo de arranque.
>> 
>> ```console
>> openstack server create --volume volume_ubuntu --flavor d2-2 --key-name publickey --nic net-id=Ext-Net InstanceTest
>> ```
>> 
>> Mostrar los volúmenes para asegurarse de que el estado ha cambiado en uso y que el volumen informa correctamente de la asociación:
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
>> Enumerar los volúmenes asociados a la instancia **InstanceTest** :
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
>> > También puede crear una instancia utilizando la imagen seleccionada y solicitando el comportamiento "boot from volume".
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
>> En el comando anterior, `b680f0aa-8eb8-4ac8-b008-2a90bb71af4f` es el ID de imagen Debian 12.
>> 
>> - Mostrar los volúmenes:
>> 
>> Mostrar los volúmenes para asegurarse de que el estado se ha cambiado a *in-use* y de que el volumen indica correctamente la asociación.
>> 
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
>> Enumere el volumen en el servidor para asegurarse de que esté correctamente conectado.
>> 
>> ```console
>> $ openstack server volume list InstanceTest2
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | ID | Device | Server ID | Volume ID | Tag |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> | d7611318-fd7b-4b6a-8a7a-8d368049f747 | /dev/sda | 5d97c190-f2e3-4af4-a010-6fa7bffbf88b | d7611318-fd7b-4b6a-8a7a-8d368049f747 | None |
>> +--------------------------------------+----------+--------------------------------------+--------------------------------------+------+
>> ```

## Más información

Interactúe con nuestra [comunidad de usuarios](/links/community).