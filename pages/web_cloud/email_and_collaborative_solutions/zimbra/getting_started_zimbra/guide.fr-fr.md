---
title: "Premiers pas avec l'offre Zimbra"
excerpt: "Découvrez comment débuter avec votre offre Zimbra depuis votre espace client OVHcloud"
updated: 2025-02-13
---

<style>
.w-400 {
  max-width:400px !important;
}
.h-400 {
  max-height:400px !important;
}
</style>

## Objectif

Avec l'offre Zimbra, OVHcloud vous propose une plateforme de messagerie collaborative open source offrant toutes les fonctionnalités nécessaires à une utilisation professionnelle. Vous trouverez dans ce guide les éléments permettant de débuter dans la configuration de vos comptes e-mail Zimbra.

**Découvrez comment débuter avec l'offre e-mail Zimbra**

<iframe class="video" width="560" height="315" src="https://www.youtube-nocookie.com/embed/G5cumO64sjw?si=kZr5AHHaoYBONkGl" title="Zimbra OVHcloud" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Prérequis

- Avoir souscrit à un compte e-mail sur notre solution e-mail Zimbra OVHcloud.
- Disposer d'un [nom de domaine OVHcloud](/links/web/domains).
- Être connecté à votre [espace client OVHcloud](/links/manager).

## En pratique

### Accéder à la gestion de votre service

1. Connectez-vous à votre [espace client OVHcloud](/links/manager).
1. Cliquez sur l'onglet `Web Cloud`{.action} .
1. Cliquez sur `Zimbra Mail`{.action}.

![zimbra](images/zimbra_general_information.png){.thumbnail .w-400}

### Configurer votre service Zimbra

Avant de débuter la configuration de vos comptes e-mail Zimbra, prenez connaissance des trois éléments qui structurent hiérarchiquement votre service Zimbra :

- [**Organisation**](#organizations) : elle permet de regrouper les noms de domaine afin de les associer.
- [**Nom de domaine**](#domains) : il est indispensable pour créer un compte e-mail. Vous devez en gérer au moins un depuis votre espace client OVHcloud et l'ajouter sur votre service Zimbra.
- [**Comptes e-mail**](#emails) : en utilisant les noms de domaines ajoutés à votre service Zimbra, vous pourrez créer une adresse e-mail.

> [!primary]
>
> L'*organisation* sert à représenter une entité (une entreprise, une association, un projet personnel, etc.). Elle permet le cloisonnement des comptes e-mail, l'application de politiques de sécurité spécifiques (fonctionnalité à venir) et de déléguer les droits des comptes e-mail qui la compose (fonctionnalité à venir). L'utilisation d'organisations permet de faciliter la navigation dans votre plateforme Zimbra ainsi que sa gestion.

Le schéma ci-dessous résume le lien hiérarchique entre les éléments précédemment cités.

![zimbra](images/zimbra_organization.png){.thumbnail .w-400}

### Organisations <a name="organizations"></a>

Si vous ajoutez un grand nombre de noms de domaine sur votre service Zimbra, il peut être utile de les regrouper en les associant à une « organisation ». Depuis votre service Zimbra, cliquez sur `Organisation`{.action}.

![zimbra](images/zimbra_organization_tab.png){.thumbnail .w-400}

#### Créer une organisation

Pour créer une organisation, cliquez sur `Ajouter une organisation`{.action}. Définissez le `Nom` de l'organisation et le `Label de l'organisation`, ce dernier étant une description courte de l'organisation vous permettant de vous repérer lorsque vous filtrez l'affichage des noms de domaine et comptes e-mail de votre service Zimbra.

![zimbra](images/zimbra_organization_add.png){.thumbnail .w-400}

#### Filtrer par organisation

Depuis les onglets `Organisation`{.action}, `Domaine`{.action} et `Comptes e-mail`{.action}, en cliquant sur le label d'une organisation, vous créez un filtre qui affichera uniquement les éléments liés à cette organisation.

Vous pouvez constater que le filtre est appliqué lorsque le label s'affiche à côté du nom de votre service Zimbra.

Pour retirer le filtre, cliquez simplement sur la croix du filtre.

![zimbra](images/zimbra_organization_filter.png){.thumbnail .w-400}

### Domaines <a name="domains"></a>

> [!warning]
>
> Pour un fonctionnement optimal lorsque vous utilisez le même nom de domaine entre les offres OVHcloud [Exchange](/links/web/emails-hosted-exchange), [E-mail Pro](/links/web/email-pro) et Zimbra, il est nécessaire de configurer le nom de domaine en `non-authoritatif`. Pour savoir comment configurer un nom de domaine en non-authoritatif sur une plateforme Exchange ou E-mail Pro, consultez notre guide [Ajouter un nom de domaine sur une plateforme e-mail](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/exchange_adding_domain).

Vous retrouvez dans cet onglet l'ensemble des noms de domaine ajoutés à votre service Zimbra. Ils doivent être gérés depuis votre espace client OVHcloud pour être ajoutés.

Le tableau des noms de domaine vous donne deux informations :

- **Organisation** : elle est déterminée lorsque vous ajoutez votre nom de domaine, vous retrouverez automatiquement son label dans cette colonne.
- **Nombre de comptes** : Vous retrouvez ici tous les comptes qui ont été créés sous le nom de domaine concerné.

![zimbra](images/zimbra_domain_tab.png){.thumbnail .w-400}

#### Ajouter un nom de domaine

> [!warning]
>
> Il est nécessaire de [créer une organisation](#organisations) pour pouvoir ajouter un nom de domaine à votre service Zimbra.

Pour ajouter un nom de domaine à votre service Zimbra, cliquez sur l'onglet `Domaine`{.action} puis cliquez sur `Ajouter un domaine`{.action}.

Sélectionnez une organisation dans le menu déroulant puis sélectionnez l'une des deux options suivantes :

- **Sélectionner un domaine dans la liste** (domaine interne) : dans cette liste, vous trouverez les noms de domaine dont vous avez la gestion depuis votre espace client OVHcloud.
- **Saisir un nom de domaine non géré par votre compte OVHcloud** (domaine externe) : renseignez un nom de domaine qui n'est pas géré dans votre espace client OVHcloud ou qui est enregistré dans un autre bureau d'enregistrement et dont vous avez la gestion.

Sélectionnez l'onglet correspondant à votre choix :

> [!tabs]
> **Domaine interne**
>>
>> Sélectionnez dans la liste un nom de domaine géré depuis votre espace client OVHcloud.
>>
>> ![zimbra](images/zimbra_domain_add_internal01.png){.thumbnail .w-400 .h400}
>>
>> Pour configurer votre zone DNS, sélectionnez l'une des deux options suivantes:
>>
>> - **Configuration recommandée** : votre zone DNS sera configurée automatiquement. Cette option convient si vous n'avez pas configuré d'offre e-mail sur votre nom de domaine.
>> - **Configuration personnalisée** : si vous avez déjà configuré une offre e-mail sur votre nom de domaine, vous pouvez choisir les éléments qui vous intéressent.
>>    - *Configurer l'enregistrement MX automatiquement* : il permet de saisir automatiquement les serveurs de réception OVHcloud (s'applique à toutes les offres e-mail OVHcloud).
>>    - *Configurer l'enregistrement SPF automatiquement* : il permet de saisir automatiquement l'enregistrement autorisant les serveurs e-mail d'envoi OVHcloud à transmettre vos e-mails. Cet enregistrement est valable pour l'ensemble des offres e-mail OVHcloud.
>>    - *Configurer l'enregistrement DKIM automatiquement* : il permet de saisir automatiquement les enregistrements nécessaires pour authentifier vos envois d'e-mails.
>>
>> ![zimbra](images/zimbra_domain_add_internal02.png){.thumbnail .w-400 .h400}
>>
>> Cliquez sur `Confirmer`{.action} pour finaliser l'ajout de votre domaine et lancer le processus de configuration.
>>
> **Domaine externe**
>>
>> Saisissez un nom de domaine qui n'est pas géré dans votre espace client. Assurez-vous que vous avez les accès pour modifier la zone DNS du nom de domaine concerné.
>>
>> Cliquez ensuite sur `Confirmer`{.action}
>>
>> ![zimbra](images/zimbra_domain_add_external01.png){.thumbnail .w-400 .h400}
>>
>> La fenêtre ci-dessous s'affiche, il est nécessaire de renseigner cet enregistrement CNAME dans la zone DNS du nom de domaine pour qu'il soit validé sur votre plateforme Zimbra.
>>
>> ![zimbra](images/zimbra_domain_add_external02.png){.thumbnail .w-400 .h400}
>>
>> > [!warning]
>> >
>> > Après 48 heures, si le CNAME n'est pas visible dans la zone DNS, l'opération est annulée. Il sera alors nécessaire de recommencer l'opération.

#### Modifier un nom de domaine

Vous pouvez modifier votre nom de domaine pour changer son organisation ou vérifier ses enregistrements DNS associés.

Depuis l'onglet `Domaine`{.action} de votre service Zimbra, cliquez sur l'icône « &#8285; » à droite du nom de domaine concerné pour afficher les options.

![zimbra](images/zimbra_domain_modify01.png){.thumbnail .w-400 .h400}

- Cliquez sur `Configurer`{.action} pour modifier l'organisation associée à votre nom de domaine.
- Cliquez sur `Diagnostics`{.action} pour afficher l'interface de diagnostic des enregistrement DNS du nom de domaine. Il est nécessaire de s'assurer qu'aucune alerte n'est affichée pour chacun des enregistrements DNS mentionnés dans les onglets. Suivez les instructions détaillées dans chaque onglet mentionnant une alerte pour configurer les enregistrements DNS :
    - **MX** : indispensable pour la réception de vos e-mails.
    - **SPF** : sécurité exigée par la majorité des serveurs e-mail destinataires pour légitimer les serveurs d'envoi e-mail d'OVHcloud avec votre nom de domaine.
    - **DKIM** : permet de mettre en place un système de signature pour chaque e-mail envoyé par votre service Zimbra. La signature est vérifiée par le destinataire à l'aide de la clé publique visible dans votre zone DNS.

![zimbra](images/zimbra_domain_modify02.png){.thumbnail .w-400 .h400}

### Comptes e-mail <a name="emails"></a>

La gestion des adresses e-mail de votre service Zimbra se fait depuis l'onglet `Comptes e-mail`{.action}. Le tableau affiche la liste des comptes e-mail présents sur votre service ainsi que 3 informations pour chacun d'eux :

- **Organisation** : si le nom de domaine de votre compte e-mail est associé à une organisation, vous retrouverez automatiquement son label dans cette colonne.
- **Offre** : comme votre service Zimbra peut héberger plusieurs offres Zimbra en son sein, vous retrouverez l'offre associée à votre compte e-mail dans cette colonne.
- **Taille** : cette colonne vous affiche la capacité totale de votre compte e-mail et l'espace qu'il occupe actuellement.

Vous retrouvez également en haut de cette page un lien vers le [Webmail](/links/web/email) pour pouvoir vous connecter directement au contenu de votre compte e-mail depuis votre navigateur internet.

![zimbra](images/zimbra_emailaccounts_tab.png){.thumbnail .w-400}

#### Créer un compte e-mail

Pour créer un compte e-mail sur votre service Zimbra, cliquez sur l'onglet `Comptes e-mail`{.action} puis sur `Créer un compte`{.action}.

Complétez les informations qui s'affichent.

- **Compte e-mail** : renseignez le *nom du compte* que portera votre adresse e-mail (votre prénom.nom, par exemple) et *sélectionnez un nom de domaine* dans le menu déroulant.

> [!warning]
>
> Le choix du nom de votre adresse e-mail doit respecter les conditions suivantes :
>
> - Minimum 2 caractères
> - Maximum 32 caractères
> - Aucun caractère accentué
> - Pas de caractères spéciaux, à l'exception des caractères suivants : `.`, `+`, `-` et `_`

- **Prénom** : renseignez un prénom.
- **Nom** : renseignez un nom.
- **Nom à afficher** : renseignez le nom qui s'affichera en tant qu'expéditeur lorsque des e-mails seront envoyés depuis cette adresse.
- **Mot de passe** : définissez un mot de passe fort composé de (au minimum) 10 caractères, une majuscule, une minuscule et un chiffre. Pour des raisons de sécurité, n'utilisez pas deux fois le même mot de passe. Choisissez-en un qui n'a aucun rapport avec vos informations personnelles (évitez par exemple de mentionner vos nom, prénom et date de naissance). Changez-le régulièrement.

> [!warning]
>
> Le choix du mot de passe doit respecter les conditions suivantes :
>
> - Minimum 10 caractères
> - Maximum 64 caractères
> - Minimum 1 majuscule
> - Minimum 1 caractère spécial
> - Aucun caractère accentué

Cliquez sur `Confirmer`{.action} pour lancer la création du compte.

![zimbra](images/zimbra_emailaccounts_add.png){.thumbnail .w-400}

### Consulter son compte e-mail <a name="mail-consult"></a>

Pour consulter votre compte e-mail :

- Connectez-vous au [webmail](/links/web/email) depuis un navigateur internet et saisissez votre adresse e-mail et votre mot de passe. Pour plus de détails consultez, notre page « [Utiliser le webmail Zimbra](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra) ».
- Configurez un logiciel de messagerie sur votre ordinateur, votre smartphone ou votre tablette. Consultez notre page « [Configurer son adresse e-mail Zimbra sur un logiciel de messagerie](/pages/web_cloud/email_and_collaborative_solutions/zimbra/zimbra_mail_apps) ».

## Aller plus loin <a name="go-further"></a>

[Configurer son adresse e-mail Zimbra sur un logiciel de messagerie](/pages/web_cloud/email_and_collaborative_solutions/zimbra/zimbra_mail_apps)

[Utiliser le webmail Zimbra](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra)

[FAQ sur la solution Zimbra OVHcloud](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/faq-zimbra)

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](/links/partner).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](/links/support).

Échangez avec notre [communauté d'utilisateurs](/links/community).