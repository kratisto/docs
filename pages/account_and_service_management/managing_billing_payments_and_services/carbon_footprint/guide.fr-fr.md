---
title: "Comment obtenir l'empreinte carbone de vos services OVHcloud"
excerpt: "Découvrez comment récupérer, à une date antérieure et via nos API, l'empreinte carbone des services Bare Metal associés à votre identifiant client OVHcloud"
updated: 2025-02-11
---

## Objectif

Dans le cadre de vos activités profesionnelles ou par intérêt sur le sujet, vous pouvez être amené à devoir calculer l'empreinte carbone de vos services.

**Découvrez comment récupérer, à une date antérieure et via nos API, l'empreinte carbone des services Bare Metal associés à votre identifiant client OVHcloud.**

> [!warning]
>
> OVHcloud met à votre disposition des services dont la configuration, la gestion et la responsabilité vous incombent. Il vous revient de ce fait d'en assurer le bon fonctionnement.
> 
> Nous mettons à votre disposition ce guide afin de vous accompagner au mieux sur des tâches courantes. Toutefois, nous vous recommandons de faire appel à un [prestataire spécialisé](/links/partner) si vous éprouvez des difficultés. En effet, nous ne serons pas en mesure de vous fournir une assistance complémentaire sur les API. Plus d'informations dans la section [« Aller plus loin »](#go-further) de ce guide.
>

## Prérequis

- Disposer d'au moins un [Serveur Dédié](/links/bare-metal/bare-metal) ou d'un [Serveur Dédié Eco](/links/bare-metal/eco) élligible au calcul de l'empreinte carbone (Advance, Game, Scale, High Grade, Storage, Rise, Kimsufi et So You Start).
- Être contact « Facturation » du (des) service(s) pour le(s)quel(s) vous souhaitez obtenir l'empreinte carbone.

## En pratique

Par défaut, les API OVHcloud sont mises à disposition pour permettre aux développeurs ou aux intégrateurs d'associer, par exemple, des fonctionnalités présentes ou non dans l'espace client OVHcloud directement dans leurs applications ou solutions.

### Étape 1 - Se connecter aux API OVHcloud et leur permettre l'accès à vos services

Pour cela, effectuez les actions suivantes : 

- Rendez-vous sur notre site [API OVHcloud](/links/api) (vérifiez bien que vous êtes sur `https://eu.api.ovh.com` si vos services sont hébergés en Europe et sur `https://ca.api.ovh.com` s'ils sont hébergés en dehors de l'Europe).
- Sur la page qui s'affiche, cliquez au centre sur `Explore the OVHcloud API`{.action}.
- Sur la nouvelle page qui apparaît et dans la partie gauche de la page, positionnez-vous sur le formulaire situé à droite du formulaire `v1`{.action}, puis sélectionnez/saisissez le choix `/me`.
- Parmi la liste d'API qui apparaît en dessous dans la colonne de gauche, recherchez et cliquez sur l'API suivante : **POST /me/carbonCalculator/task**. Vous pouvez aussi cliquer directement sur l'API pour y accéder :

> [!api]
>
> @api {v1} /me POST /me/carbonCalculator/task
>

- Sur la partie droite de la page s'affiche alors l'API avec son encadré à compléter.
- Cliquez sur le bouton situé en haut à droite intitulé `Authenticate`{.action}, puis sur le bouton `Login with OVHcloud SSO`{.action}.
- L'interface de connexion à votre [espace client OVHcloud](/links/manager) s'ouvre.
- Connectez-vous avec votre identifiant client, puis cliquez sur `Authorize`{.action} pour utiliser les API OVHcloud avec les services présents dans votre espace client.
- Vous êtes ensuite automatiquement redirigé vers la page précédente de l'API **POST /me/carbonCalculator/task** tout en étant connecté à votre espace client OVHcloud.

### Étape 2 - Demander la génération du bilan et récupérer l'ID de la tâche demandée

Pour cela, remplacez la date du jour qui apparaît dans l'encadré de l'API par la date à laquelle vous souhaitez arrêter le calcul du bilan. Veuillez respecter le format de date suivant :

```bash
{
  "date": "YYYY-MM-DD"
}
```

![API](/pages/assets/screens/api/post-me-carboncalculator-task.png){.thumbnail}

> [!warning]
>
> Plusieurs points sont à prendre en compte : 
> - Vous ne pouvez pas générer de bilan pour le mois en cours.
> - Que vous saisissiez une date en début, milieu ou fin de mois pour le mois choisi, le bilan prendra en compte le mois complet.
> - Aucun bilan ne peut être généré au delà des 24 derniers mois. Par ailleurs, aucun bilan ne peut être généré avant le mois de mai 2023 (date où la fonctionnalité a été mise en place).

Une fois la date choisie et correctement saisie, cliquez sur le bouton bleu `EXECUTE`{.action} situé en bas à droite de la section préalablement remplie.

Si tout a été effectué correctement, un `taskID` apparaît dans la fenêtre `RESPONSE`{.action} lorsque vous descendez sur la page en dessous du bouton `EXECUTE`{.action}.

![API](/pages/assets/screens/api/post-me-carboncalculator-task-response.png){.thumbnail}

Par exemple, si votre identifiant client OVHcloud est le `aa00000-ovh` et que la date choisie précédemment était le `31-01-2025`, alors vous obtiendrez le résultat suivant :

```bash
{
  "taskID": "aa00000-ovh_202501"
}
```

Copiez uniquement la valeur que vous obtenez de votre côté et équivalente à la valeur de notre exemple `aa00000-ovh_202501` (sans copiez les deux `"` situés aux extrémités).

### Étape 3 - Récupérer le fichier contenant le bilan carbone de vos services au format PDF

Grâce à la valeur du `taskID` précédemment récupérée, vous pourrez récupérer le bilan carbone de vos services au format PDF.

Pour cela, restez sur notre site [API OVHcloud](/links/api) et effectuez les actions suivantes :

- Dans la partie gauche de la page, positionnez-vous sur le formulaire situé à droite du formulaire `v1`{.action}, puis sélectionnez/saisissez le choix `/me`{.action}.
- Parmi la liste d'API qui apparaît en dessous dans la colonne de gauche, recherchez et cliquez sur l'API suivante : **GET /me/carbonCalculator/task/{taskID}**. Vous pouvez aussi cliquer directement sur l'API pour y accéder :

> [!api]
>
> @api {v1} /me GET /me/carbonCalculator/task/{taskID}
>

- Sur la partie droite de la page s'affiche alors l'API avec un formulaire à remplir.

Remplissez le formulaire de la partie `PATH PARAMETERS` ainsi :

- `taskID` : Copiez ici la valeur du taskID récupéré précédemment lors de l'étape 2.

![API](/pages/assets/screens/api/get-me-carboncalculator-task-taskid.png){.thumbnail}

Une fois la valeur de votre `taskID` correctement saisie, cliquez sur le bouton bleu `EXECUTE`{.action} situé en bas à droite de la section préalablement remplie.

Le résultat suivant apparaît dans la fenêtre `RESPONSE`{.action} lorsque vous descendez sur la page en dessous du bouton `EXECUTE`{.action} :

![API](/pages/assets/screens/api/get-me-carboncalculator-task-taskid-response.png){.thumbnail}

```bash
{
  "link": "Find here the complete URL to download the carbon footprint in PDF format",
  "status": "SUCCESS",
  "taskID": "aa00000-ovh_202501"
}
```

Dans ce résultat, copiez l'intégralité de l'URL en « HTTPS » **sans les guillements** présente à droite de la mention `"link":`, puis collez-la dans la barre de recherche de votre navigateur internet pour initier le téléchargement du bilan carbone au format PDF.

Votre navigateur Internet va automatiquement télécharger le fichier, puis l'afficher.

> [!primary]
>
> En fonction de la configuration de votre navigateur, le téléchargement et l'affichage du fichier peut se retrouver bloqué. S'il tel est le cas, vérifiez la configuraiton de votre navigateur, puis rechargez la page.

Une fois le fichier ouvert, vous y trouverez, entre autre, les éléments suivants :

- Un tableau récapitulatif des émissions de C02 par catégories pour le mois demandé via nos API.
- Un tableau récapitulatif des émissions de C02 par catégories entre le début de l'année civile et le mois demandé via nos API.
- Un tableau détaillant les valeurs par type de produit souscrit.
- Un graphe présentant les émissions de C02 par catégories.

## Aller plus loin <a name="go-further"></a>

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](/links/partner).

Échangez avec notre [communauté d'utilisateurs](/links/community).