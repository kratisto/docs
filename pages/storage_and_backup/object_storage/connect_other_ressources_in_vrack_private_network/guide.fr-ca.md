---
title: Object Storage - Comment connecter mon bucket Object Storage avec d'autres ressources dans un réseau privé vRack ?
excerpt: Découvrez comment utiliser l'Object Storage avec des ressources dans un réseau privé.
updated: 2025-04-10
---

## Objectif

Ce guide explique comment utiliser l'Object Storage avec d'autres ressources dans un réseau privé.

## Prérequis

Vous devez disposer des éléments suivants :

- Un [bucket Object Storage](/pages/storage_and_backup/object_storage/s3_getting_started_with_object_storage).
- Un [réseau privé vRack](/pages/public_cloud/public_cloud_network_services/getting-started-07-creating-vrack).
- Une [Gateway Public Cloud](/pages/public_cloud/public_cloud_network_services/getting-started-02-create-private-network-gateway).
- D'autres ressources (instances Public Cloud, Managed Kubernetes, Bare Metal servers, etc.).

## En pratique

### Contexte

Selon vos besoins, une connexion sécurisée entre un réseau privé et votre bucket Object Storage peut s'avérer nécessaire. Nos services **réseau privé vRack** et **Gateway Public Cloud** sont conçus pour répondre à vos besoins spécifiques en matière de sécurité et de performance.

Cela vous permet également d'interconnecter deux buckets Object Storage avec vos ressources rassemblées dans un réseau privé vRack (voir le diagramme d'architecture ci-dessous).

![vrack private network with buckets - diagram](images/object_storage_buckets_vrack_private.png){.thumbnail}

### Création d'un réseau privé vRack et d'une Gateway Public Cloud

Afin de créer et de configurer à la fois une Gateway Public Cloud et un réseau privé vRack, veuillez suivre le guide « [Créer un réseau privé avec une Gateway](/pages/public_cloud/public_cloud_network_services/getting-started-02-create-private-network-gateway) ». Ce guide explique comment :

- Sélectionner et créer la Gateway appropriée en termes de performance et de géo-disponibilité.
- Rattacher un réseau privé vRack existant ou nouvellement créé à la Gateway.

### Création d'une liste blanche d'adresses IP sur la Gateway

Une fois la Gateway créée et associée à un réseau privé vRack, l'étape suivante consiste à mettre sur liste blanche un ensemble d'adresses IP de votre Object Storage. Pour ce faire, plusieurs moyens existent :

- Utilisation des politiques du bucket Object Storage : cette fonctionnalité n'est pas encore implémentée, elle sera bientôt disponible.
- Nous avons mis en place un processus interne afin de vous aider à créer une liste blanche pour un ensemble d'adresses IP en fonction de la configuration de votre Gateway et de votre réseau privé vRack.

Pour suivre ce processus, veuillez ouvrir une demande auprès de notre support technique avec l'objet suivant « Object Storage - IP whitelisting process », et indiquez dans votre demande les plages d'adresses IP que vous souhaitez placer en liste blanche. Notre équipe automatisera la configuration pour vous, ce processus peut prendre jusqu'à 24 heures.

Après cette dernière étape, vous êtes prêt à utiliser votre Object Storage avec les ressources rassemblées dans un réseau privé vRack.

## Aller plus loin

Si vous avez besoin d'une formation ou d'une assistance technique pour la mise en oeuvre de nos solutions, contactez votre commercial ou cliquez sur [ce lien](/links/professional-services) pour obtenir un devis et demander une analyse personnalisée de votre projet à nos experts de l’équipe Professional Services.

Échangez avec notre [communauté d'utilisateurs](/links/community).
