---
title: 'Augmenter et diminuer la bande passante via l'API OVHcloud'
excerpt: 'Découvrez comment augmenter ou diminuer la bande passante d'un serveur dédié via l'API OVHcloud'
updated: 2025-01-17
---

## Objectif

Chacun de nos serveurs dédiés dispose d’une bande passante publique minimale de 500 Mbit/s. Dans ce guide, nous vous expliquons comment augmenter ou diminuer facilement la bande passante d’un serveur dédié.

## Prérequis

- Disposer d’un [serveur dédié](/links/bare-metal/bare-metal) dans votre compte OVHcloud
- Accès à l’[API OVHcloud](/pages/manage_and_operation/api/first-steps)

## Instructions

### Trouver les services disponibles

Utilisez l'appel API suivant pour répertorier tous les services disponibles pour augmenter (ou diminuer) la bande passante, et vérifiez que le service que vous souhaitez utiliser est répertorié :

> [!api]
>
> @api {v1} /order GET /order/upgrade/bare metalPublicBandwidth
>

![bandwidth](images/bandwidth_01.png){.thumbnail}

### Trouver le code de l'offre (*planCode*)

Lister les offres disponibles et retrouver le **planCode** de votre choix avec l'appel API ci-dessous :

> [!api]
>
> @api {v1} /order GET /order/upgrade/bare metalPublicBandwidth/{serviceName}
>

Renseignez les variables :

- serviceName : nom de votre serveur dédié, par exemple `ns1234567.ip-203.0.113.eu`

![bandwidth](images/bandwidth_02.png){.thumbnail}

Le champ `RESPONSE` doit afficher des informations similaires à celles qui suivent :

![bandwidth](images/bandwidth_02_1.png){.thumbnail}

### Vérifier votre commande

Utilisez l'appel API suivant pour obtenir un aperçu de votre commande, incluant la tarification :

> [!api]
>
> @api {v1} /order GET /order/upgrade/bare metalPublicBandwidth/{serviceName}/{planCode}
>

Renseignez les variables :

- planCode : la référence récupérée à l'étape précédente
- serviceName : nom de votre serveur dédié
- quantity : 1

![bandwidth](images/bandwidth_03.png){.thumbnail}

Le champ `RESPONSE` doit afficher des informations similaires à celles qui suivent :

![bandwidth](images/bandwidth_03_1.png){.thumbnail}

### Soumettre votre commande

Pour envoyer officiellement la commande, utilisez l'appel API suivant :

> [!api]
>
> @api {v1} /order POST /order/upgrade/bare metalPublicBandwidth/{serviceName}/{planCode}
>

![bandwidth](images/bandwidth_04.png){.thumbnail}

La commande sera traitée une fois que vous aurez cliqué sur `Execute`{.action}. Veuillez noter que si votre bande passante est augmentée après le 1er du mois, un prorata vous sera facturé.

## Aller plus loin

Rejoignez notre [communauté d'utilisateurs](/links/community).