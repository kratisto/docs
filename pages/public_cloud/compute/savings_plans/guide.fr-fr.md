---
title: 'Fonctionnement des Savings Plans'
excerpt: 'Savings Plans : Tout ce que vous devez savoir pour optimiser vos coûts'
updated: 2025-01-06
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

## Objectif

Ce guide a pour objectif de vous fournir une compréhension claire et pratique des Savings Plans, afin de vous aider à optimiser vos coûts d'infrastructure. Nous expliquerons ce que sont les Savings Plans, leur fonctionnement, et comment choisir le modèle le plus adapté à vos besoins spécifiques. À travers des exemples concrets, vous découvrirez comment ces plans peuvent réduire vos dépenses tout en offrant une flexibilité dans la gestion de vos ressources.

Le guide détaillera également l'utilisation du tableau de bord associé aux Savings Plans, qui vous permettra de suivre vos coûts, le nombre de ressources  utilisées et couvertes, ainsi que les économies générées. Enfin, nous vous aiderons à comprendre les aspects liés à la facturation afin que vous puissiez analyser et maximiser les bénéfices de vos choix en matière de Savings Plans.

## Fonctionnement des Savings Plans

### Qu'est ce qu'un Savings Plan ?

Un Savings Plan est une offre par laquelle un client, en échange de la couverture d'un certain nombre de ressources simultanées, s'engage à payer un montant fixe pour une période déterminée. Ce modèle d'engagement permet aux clients de bénéficier de tarifs réduits pour les instances couvertes, par rapport à la facturation horaire.

### Fonctionnement général d’un Savings Plan

> [!primary]
>
> Lorsqu’un client souscrit à un Savings Plan, il s’engage à payer un **montant fixe** pour une **durée donnée**. En contrepartie, ce plan couvre un nombre de ressources simultanées spécifiques pour lesquels il ne paiera pas d’autres frais, ce qui lui permet de bénéficier d’une facturation avantageuse.
>

Voici quelques scénarios pour mieux comprendre ce fonctionnement : 

- **Cas "1:1" :** Imaginons qu’un client dispose de 10 instances de type B3-8 sur OVHcloud et qu'il souscrit à un Savings Plan qui couvre précisément 10 instances B3-8 pour une durée de 1 an. Dans ce cas, le client ne paiera que le montant de son Savings Plan, et ce montant couvrira entièrement les coûts associés à ses 10 instances B3-8 pendant toute la durée de l'engagement. Il n’y a pas de frais supplémentaires à la fin de chaque mois, puisque les instances sont couvertes par le plan.
- **Cas "1,5:1" :** Supposons maintenant qu’un autre client utilise 15 instances de type B3-8, mais qu'il souscrit à un Savings Plan couvrant uniquement 10 instances de type B3-8. Dans ce cas, le client bénéficie du tarif avantageux du Savings Plan pour les 10 premières instances. Cependant, les 5 autres instances, qui ne sont pas couvertes par le Savings Plan, seront facturées selon le tarif standard à l'heure. Si ces 5 instances sont utilisées pendant tout le mois, le client sera facturé pour les 5 instances restantes, en plus de son engagement pour les 10 instances couvertes par le Savings Plan.
- **Cas "0,8 :1" :** Dernier cas, un client a souscrit à un Savings Plan pour 10 instances de type B3-8, mais il n’utilise que 8 instances simultanément au cours du mois. Même si ce client n’utilise pas toutes les instances couvertes par son plan, il ne paiera pas de frais supplémentaires. Le Savings Plan couvrira toujours les 8 instances simultanées utilisées, et le client bénéficiera de la tarification avantageuse des 10 instances sans frais supplémentaires. Cette situation reste avantageuse sur le plan financier, même si le client n'utilise pas la totalité des 10 instances du Savings Plan.

> [!warning]
> 
> Point sur le terme **ressources simultanées**.
>
> Un Savings Plan couvre un certain nombre de ressources actives simultanément. Par exemple, pour un Svings Plan de 1 ressource, si un client démarre une ressource à 10h05 et l'efface à 10h10, puis crée une autre ressource à 10h17 et l'efface à 10h30, même s'il a démarré et effacé deux ressources, seules les ressources qui ont été allumées en même temps sont comptabilisées. Dans ce cas, une seule ressource est active en même temps, de sorte que le Savings plan couvre les deux ressources sans facturation supplémentaire. Il en va de même si les ressources sont utilisées à différents moments du mois (par exemple, du 1er au 10, puis du 15 au 30), pour autant qu'elles ne soient pas actives en même temps.
>

### Eligible / compatible services

Ce tableau résume l'éligibilité des services OVHcloud :

| Service                  | Eligible    |
| ------------------------ | ----------- |
| Compute instances        | Yes         |
| Managed Rancher          | Yes         |
| Storage                  | No          |
| Public Cloud Databases   | No          |

### Fonctionnement des Savings Plans pour les instances

Les Savings Plans pour les instances sont basés sur l'engagement d'une quantité d'instances pour une durée déterminée, offrant une facturation avantageuse pour celles-ci.

Le point essentiel à retenir est que seules les instances actives simultanément sont prises en compte dans la couverture du savings plan. Les instances qui ne sont pas actives en même temps n'ont pas d'impact sur le plan, tant que le nombre d'instances actives à un moment donné reste dans la limite de la couverture de votre plan.

> [!warning]
>
> En ce qui concerne les instances actives simultanément, pour savoir si une ressource suspendue ou mise en pause est considérée comme active, veuillez vous référer au guide suivant : [Shelve or pause an instance](/pages/public_cloud/compute/suspend_or_pause_an_instance#suspendre-shelve-une-instance)
>
> Veuillez noter que seules les **instances** Gen3 sont éligibles aux Savings Plans. Assurez-vous que votre instance appartient à cette génération pour bénéficier de cette offre.
>

### Fonctionnement des Savings Plans pour Rancher

Les Savings Plans pour Rancher reposent sur l'engagement d’une quantité de vCPUs sur une durée définie, ce qui permet de réaliser des économies sur le service Managed Rancher. Ce modèle offre une flexibilité accrue, car les vCPUs engagés peuvent être partagés entre tous vos environnements Rancher, optimisant la facturation des ressources utilisées d'une manière flexible et évolutive.

En souscrivant à un Savings PLan pour Rancher, vous vous engagez à utiliser une certaine quantité de vCPU, qui est ensuite répartie entre vos clusters Rancher, ce qui garantit la rentabilité même si votre utilisation fluctue au fil du temps.

> [!info]
>
> The Savings Plans for Rancher only apply to vCPUs. Other resources, such as storage, instances, and other services, are not covered by this Savings Plan and will still be billed separately. Be sure to account for these additional costs when planning your Rancher resources.
>
> Pour que les vCPU inclus dans votre Savings Plan soient consommés, il est impératif d'attribuer une instance à vos noeuds Kubernetes. Sans instance configurée, les ressources couvertes par le Savings Plan resteront inutilisées, et vous continuerez à payer pour ces ressources non consommées. Assurez-vous de bien dimensionner vos instances pour qu'elles correspondent à vos besoins en vCPU et RAM.
>

### Gestion automatisée de l’infrastructure avec les Savings Plans

Les clients n’ont pas à associer manuellement leurs instances aux Savings Plans. Nous prenons en charge cette gestion de manière automatique, en prenant en compte toutes les instances, qu'elles soient existantes ou futures, pour le calcul de la consommation du Savings Plan.

Par exemple : 
- Si un client dispose de 10 instances de type B3-8 et souscrit à un Savings Plan pour 10 instances B3-8, celles-ci seront automatiquement couvertes par la facturation du Savings Plan.
- Si le client dispose de 15 instances de type B3-8 et souscrit à un Savings Plan pour 10 instances B3-8, les 10 premières seront automatiquement couvertes par la facturation du Savings Plan et les 5 autres seront facturées à l’heure sans remise.

### Créer un modèle d’économie sur mesure

Pour optimiser les coûts tout en s’adaptant aux besoins variés des clients, il est possible de cumuler plusieurs Savings Plans ayant des caractéristiques différentes, comme la taille, la flavor, ou la durée d’engagement. Cette approche permet d’aligner la couverture avec des usages spécifiques, tout en maximisant les économies.

/// details | **Exemple réel :**

- Un client utilise deux types de workloads :
  - Un environnement de production stable avec 20 VMs B3-16, utilisées 24h/24 et 7j/7 toute l’année.
  - Un environnement de développement variable, avec une moyenne de 10 VMs B3-8, utilisées principalement sur 8 mois de l’année.
- Après analyse de ses besoins, le client opte pour la combinaison suivante :
  - Un Savings Plan de 3 ans couvrant 20 VMs B3-16. Cela représente une **réduction de 54 %** par rapport à une facturation à l’heure.
  - Un Savings Plan de 1 an couvrant 10 VMs B3-8. Cela représente une **réduction de 35 %** par rapport à une facturation à l’heure.

Grâce à cette combinaison, le client réalise des économies substantielles en optimisant ses ressources de production à long terme, tout en maintenant la flexibilité nécessaire pour son environnement de développement, avec des réductions respectives de 54 % et 35 % par rapport à une facturation horaire.

///

## Analyser vos Savings Plans grâce au dashboard

Le tableau de bord des Savings Plans vous permet de suivre et d'analyser vos Savings Plans, en fournissant des informations essentielles sur leur utilisation, leur couverture et les économies réalisées. Vous pouvez consulter des données spécifiques selon la période, le service, le type d'instance ou d'autres critères pertinents.

/// details | **a. Filtres de sélection**

<!-- Image avec focus sur les filtres -->

- **Service :** Vous permet de filtrer les données en fonction du service spécifique auquel les Savings Plans sont associés.
- **Type d'instance :** Permet de choisir entre différents types d'instances ("instances" ou "Managed Rancher Services").
- **Modèle :** Choix du modèle spécifique de ressources pour affiner le suivi des Savings Plans.
- **Période :** Permet de sélectionner une période précise pour observer l’utilisation des Savings Plans et la couverture associée.

///

/// details | **b. KPIs (Indicateurs Clés de Performance)**

> [!primary]
>
> Les données des KPIs dans le dashboard des Savings Plans sont ajustées en fonction des filtres appliqués. Cela permet de personnaliser l'affichage des indicateurs pour se concentrer sur des périodes spécifiques, des services particuliers, ou des types d'instances choisis.
>

<!-- Image avec focus sur les KPIs -->

- **Nombre de Savings Plans actifs :** Affiche le nombre total de Savings Plans actifs.
- **% d'usage des Savings Plans :** Indique le pourcentage d’utilisation des Savings Plans par rapport à la capacité totale disponible.
- **% de couverture des Savings Plans :** Montre la proportion des ressources couvertes par les Savings Plans par rapport à l'utilisation totale.
- **Économies réalisées :** Affiche le montant total des économies réalisées grâce aux Savings Plans pendant la période spécifiée.
- **Montant du hors-forfait :** Affiche le montant des consommations excédentaires qui génèrent des frais non remisés.

///

/// details | **c. Graphiques**

<!-- Image avec focus sur le graphique -->

- **Légende axe Y du graphique :**
  - Si "Instances" est sélectionné, l'axe Y affichera le nombre d'instance(s) utilisées.
  - Si "Managed Rancher Services" est sélectionné, l'axe Y affichera le nombre de vCPU(s) utilisés.
- **Légendes des couleurs du graphique :**
  - **Vert :** Représente le nombre de ressources couvertes par un Savings Plan.
  - **Rouge :** Représente le nombre de ressources non couvertes par un Savings Plan et facturées à l’heure.

///

/// details | **d. Tableau de suivi de consommation**

<!-- Image avec focus sur la parti de suivi de consommation -->

- **Créer un Savings Plan :** Un bouton permettant de créer un nouveau Savings Plan.
- **Télécharger (Exporter en CSV) :** Un bouton pour exporter les données du **tableau de suivi de consommation** au format CSV, afin de les analyser en détail ou les conserver pour vos archives.
- **Colonnes du tableau de suivi de consommation :**
  - **Début :** Cette colonne indique la date et l’heure de début de la période de consommation des ressources.
  - **Fin :** Cette colonne indique la date et l’heure de fin de la période de consommation des ressources.
  - **Utilisation des Savings Plans :** Montre la quantité de ressources consommées durant la période. Cette valeur représente l'utilisation effective des ressources pendant la période sélectionnée.
  - **Couverture totale des Savings Plans :** Indique la couverture totale des ressources durant la période, c’est-à-dire la quantité de ressources couvertes par vos Savings Plans pour cette période spécifique.

///

Grâce à ce tableau de bord, vous pouvez suivre en temps réel l'utilisation et l'efficacité de vos Savings Plans, ajuster votre stratégie en fonction des données observées et optimiser ainsi vos coûts pour une gestion plus performante de vos ressources OVHcloud.

## Comprendre la facturation

> [!info]
>
> Veuillez noter qu'il n'est pas encore possible de modifier un Savings Plan. Veuillez contacter l'équipe Sales.
>

Pour mieux comprendre votre facturation une fois que vous souscrivez à un Savings Plan, voici une explication des différentes lignes que vous pouvez y retrouver.

/// details | Facturation de Savings Plan pour les instances

<!-- Image facture avec deux lignes  -->

- **a. Facturation de vos Savings Plans**
Lorsque vous souscrivez à un Savings Plan, vous vous engagez à payer un montant fixe pour un certain nombre d'instances sur une période déterminée. Cependant, les instances couvertes par ce plan ne sont pas détaillées individuellement sur votre facture.
Sur votre facture, vous ne verrez que le montant total correspondant au Savings Plan, et non les instances spécifiques qu'il couvre. Cela permet de simplifier la facturation en ne montrant qu'une ligne regroupant l'ensemble des instances couvertes par votre engagement, sans besoin de détailler chaque instance.

- **b. Facturation de vos instances supplémentaires**
Les instances supplémentaires, c'est-à-dire celles qui ne sont pas couvertes par votre Savings Plan, sont facturées à l'heure, comme pour une facturation classique.
Par exemple, si vous utilisez 10 instances Gen3 pendant 10 heures au cours du mois, la facturation s’effectuera sur la base de l’heure consommée. Cela donne une facture de 100 heures (10 instances x 10 heures), facturées au tarif horaire standard, en plus de la ligne du Savings Plan.

///

/// details | Facturation de Savings Plan pour Rancher

<!-- Image facture avec deux lignes -->

- **a. Facturation de vos Savings Plans**
Lorsque vous souscrivez à un Savings Plan, vous vous engagez à payer un montant fixe pour un certain nombre de vCPUs sur une période déterminée. Cependant, les vCPUs couverts par ce plan ne sont pas détaillés individuellement sur votre facture.
Sur votre facture, vous ne verrez que le montant total correspondant au Savings Plans. Vous n'aurez pas le détail des différents Rancher avec le nombre de vCPUs qui les couvrent appartenant au Savings Plan.

- **b. Facturation de vos vCPUs supplémentaires**
Les vCPUs supplémentaires, c'est-à-dire ceux qui ne sont pas couverts par votre Savings Plan, sont facturés sur une base horaire, comme pour la facturation standard.
Par exemple, si vous utilisez 10 vCPUs pendant 10 heures au cours du mois, vous serez facturé à l'heure. Cela donne une facture pour 100 heures (10 vCPUs x 10 heures), facturées au taux horaire standard, en plus de la ligne du Savings Plan.

> [!info]
>
> Rancher est facturé en fonction du nombre total de vCPU de chacun des nœuds de travail de vos « downstream clusters » .
Les vCPU des nodes de type control-plane ne sont pas facturés.
>
> Le minimum de consommation pour Managed Rancher Service est de 20 vCPU par Rancher, toutefois vous pouvez créer un ou plusieurs Saving Plan à partir de 1 vCPU. Les vCPU souscrits seront décomptés du nombre total de vCPU consommés.
>

///

## Aller plus loin

Échangez avec notre [communauté d'utilisateurs](/links/community).
