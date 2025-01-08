---
title: "Synchroniser votre calendrier Zimbra dans votre agenda"
excerpt: "Découvrez comment ajouter votre calendrier Zimbra sur une application via le protocole CalDAV"
updated: 2025-01-03
---

<style>
.w-600 {
  max-width:600px !important;
}
.h-600 {
  max-height:600px !important;
}
</style>

> [!warning]
>
> **Important**
>
> L'offre Zimbra est un produit en phase bêta.
>
> Il est uniquement disponible aux personnes ayant complété le [formulaire d'inscription à la bêta](https://labs.ovhcloud.com/en/zimbra-beta/).
>
> Certaines fonctionnalités ou limitations présentées dans ce guide sont susceptibles d'évoluer lorsque le produit sera commercialisé.

## Objectif

Les comptes e-mail Zimbra peuvent être configurés sur différents logiciels de messagerie compatibles. Cela vous permet d’utiliser votre adresse e-mail depuis l’appareil de votre choix. L'application Zimbra est disponible gratuitement sur Android et iOS

**Découvrez comment configurer votre adresse e-mail Zimbra sur l'application Zimbra.**

> [!warning]
>
> OVHcloud met à votre disposition des services dont la configuration, la gestion et la responsabilité vous incombent. Il vous revient de ce fait d'en assurer le bon fonctionnement.
>
> Nous mettons à votre disposition ce guide afin de vous accompagner au mieux sur des tâches courantes. Néanmoins, nous vous recommandons de faire appel à un [partenaire spécialisé](/links/partner) et/ou de contacter l'éditeur du service si vous éprouvez des difficultés. En effet, nous ne serons pas en mesure de vous fournir une assistance. Plus d'informations dans la section « Aller plus loin » de ce guide.

## Prérequis

- Disposer d’une adresse e-mail Zimbra.
- Avoir installé une application prenant en charge le protocole de calendrier CalDAV
- Posséder les identifiants relatifs à l'adresse e-mail attachée au calendrier que vous souhaitez paramétrer.

## En pratique

### CalDAV c'est quoi ?

CalDAV est un protocole permetant le partage de calendrier et de tâches en ligne. Les adresses e-mail Zimbra dispose de calendrier utilisant le protocole CalDAV. Leur configuration est similaire à celle d'une adresse e-mail et nécessite une application prenant en charge le protocole

### Ajouter un calendrier sur Thunderbird

Ouvrez Thunderbird et cliquez sur l'onglet calendrier dans la partie supérieure de l'écran ou cliquez sur l'icône à droite.

Cliquez droit sur un calendrier existant e sélectionnez `Nouveau calendrier` dans le menu qui s'affiche.

Sélectionnez `Sur le réseau` et cliquez sur Suivant.

- **Nom d’utilisateur** : saisissez l'adresse e-mail complète associée à votre calendrier.

- **Adresse** : Saisissez l'adresse du serveur Zimbra OVHcloud `zimbra1.mail.ovh.net`

Cliquez sur `Rechercher des agendas` pour initier la synchronisation du calendrier.Saisissez le mot de passe de l'adresse e-mail associée au nom d'utilisateur

Pour ajouter un calendrier CalDAV sur Thunderbird, suivez les étapes d'installation en cliquant sur les onglets ci-dessous :

> [!tabs]
> **Etape 1**
>>
>> Dirigez-vous dans les `Réglages` de votre iPhone ou iPad retrouvez la section `Calendrier` en défillant le menu ou en saisissant « calendrier » dans la barre de recherche.
>>
>> ![zimbra_app](images/zimbra-calendar-thunderbird01.png){.thumbnail .w-600 .h-600}
>>
> **Etape 2**
>>
>> Dirirgez vous dans `Comptes Calendrier` puis sélectionnez `Ajouter un compte`
>>
>> ![zimbra_app](images/zimbra-calendar-thunderbird02.png){.thumbnail .w-600 .h-600}
>>
> **Etape 3**
>>
>> Choisissez `Autre` puis sélectionnez `Ajoutez un compte CalDAV` dans la section « CALENDRIER »
>>
>> ![zimbra_app](images/zimbra-calendar-thunderbird03.png){.thumbnail .w-600 .h-600}
>>
> **Etape 4**
>>
>> Saisissez les informations de connexion à votre calendrier :
>>
>> - **Serveur** : saisissez la valeur `zimbra1.mail.ovh.net`.
>> - **Nom d'utilisateur** : saisissez l'adresse e-mail complète assossiée à votre calendrier.
>> - **Mot de passe** : saisissez le mot de passe de l'adresse e-mail assossiée à votre calendrier.
>> - **Description** : ajoutez une descriptio nde votre calendrier.
>>
>> Validez votre choix avec le bouton `Suivant` et finalisez votre configuration en choisisant les applications `Calendrier` et `Rappel` qui utiliseront les inforamtions de votre calendrier Zimbra.
>>
>> ![zimbra_app](images/zimbra-calendar-ios04.png){.thumbnail .w-600 .h-600}
>>

### Ajouter un calendrier sur iOS et ipadOS

> [!warning]
>
> La configuiration ci-dessous a été réalisée à partir d'un iPhone. Néanmoins la manipulation reste la même depuis un iPad.

Pour ajouter un calendrier CalDAV sur l'application Apple `Calendrier` de votre iPhone ou iPad, suivez les étapes d'installation en cliquant sur les onglets ci-dessous :

> [!tabs]
> **Etape 1**
>>
>> Dirigez-vous dans les `Réglages` de votre iPhone ou iPad retrouvez la section `Calendrier` en défillant le menu ou en saisissant « calendrier » dans la barre de recherche.
>>
>> ![zimbra_app](images/zimbra-calendar-ios01.png){.thumbnail .w-600 .h-600}
>>
> **Etape 2**
>>
>> Dirirgez vous dans `Comptes Calendrier` puis sélectionnez `Ajouter un compte`
>>
>> ![zimbra_app](images/zimbra-calendar-ios02.png){.thumbnail .w-600 .h-600}
>>
> **Etape 3**
>>
>> Choisissez `Autre` puis sélectionnez `Ajoutez un compte CalDAV` dans la section « CALENDRIER »
>>
>> ![zimbra_app](images/zimbra-calendar-ios03.png){.thumbnail .w-600 .h-600}
>>
> **Etape 4**
>>
>> Saisissez les informations de connexion à votre calendrier :
>>
>> - **Serveur** : saisissez la valeur `zimbra1.mail.ovh.net`.
>> - **Nom d'utilisateur** : saisissez l'adresse e-mail complète assossiée à votre calendrier.
>> - **Mot de passe** : saisissez le mot de passe de l'adresse e-mail assossiée à votre calendrier.
>> - **Description** : ajoutez une descriptio nde votre calendrier.
>>
>> Validez votre choix avec le bouton `Suivant` et finalisez votre configuration en choisisant les applications `Calendrier` et `Rappel` qui utiliseront les inforamtions de votre calendrier Zimbra.
>>
>> ![zimbra_app](images/zimbra-calendar-ios04.png){.thumbnail .w-600 .h-600}
>>

### Ajouter un calendrier sur macOS

Pour ajouter un calendrier CalDAV sur l'application Apple `Calendrier` de votre Mac, lancez l'application et suivez les étapes d'installation en cliquant sur les onglets ci-dessous :

> [!tabs]
> **Etape 1**
>>
>> Cliquez sur `Calendrier` dans la barre de menu supérieure, puis sur `Ajouter un compte`. Sélectionnez `Ajoutez un compte CalDAV`, puis cliquez sur `Continuer`{.action}.
>>
>> ![zimbra_app](images/zimbra-calendar-macos01.png){.thumbnail .w-600 .h-600}
>>
> **Etape 2**
>>
>> Depuis la fenêtre de configration complétez les inforamtions suivantes 
>>
>> - **Type de compte** : choisissez `Manuel` dans le menu déroulant.
>> - **Nom d'utilisateur** : saisissez l'adresse e-mail complète assossiée à votre calendrier.
>> - **Mot de passe** : saisissez le mot de passe de l'adresse e-mail assossiée à votre calendrier.
>> - **Adresse du serveur** : saisissez la valeur `zimbra1.mail.ovh.net`.
>>
>> Pour finaliser, cliquez sur `Se connecter`{.action}
>>
>> ![zimbra_app](images/zimbra-calendar-macos02.png){.thumbnail .w-600 .h-600}
>>

### Ajouter son calendrier sur une application ou logiciel prenant en charge CalDAV

Lorsque vous lancez l'application pour la première fois, la fenêtre ci-dessous s'affiche. Saisissez l'URL du serveur Zimbra OVHcloud `https://zimbra1.mail.ovh.net`, appuyez sur `Continue`{.action} pour valider.

- **Serveur** : saisissez la valeur `zimbra1.mail.ovh.net`.
- **Nom d'utilisateur** : saisissez l'adresse e-mail complète assossiée à votre calendrier.
- **Mot de passe** : saisissez le mot de passe de l'adresse e-mail assossiée à votre calendrier.

## Aller plus loin <a name="go-further"></a>

[Premiers pas avec l'offre Zimbra](/pages/web_cloud/email_and_collaborative_solutions/zimbra/getting_started_zimbra)

[Configurer son adresse e-mail Zimbra sur un logiciel de messagerie](/pages/web_cloud/email_and_collaborative_solutions/zimbra/zimbra_mail_apps)

[Utiliser le webmail Zimbra](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra)

[FAQ sur la solution Zimbra OVHcloud](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/faq-zimbra)

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](/links/partner).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](/links/support).

Échangez avec notre [communauté d'utilisateurs](/links/community).