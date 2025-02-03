---
title: 'Migrer une adresse e-mail MX Plan vers un compte Zimbra'
excerpt: 'Découvrez comment migrer une adresse e-mail MX Plan vers un compte Zimbra'
updated: 2025-02-04
---

## Objectif

Avec la transition progressive des comptes MX Plan vers Zimbra, certains clients souhaitent anticiper cette migration et effectuer eux-mêmes le transfert de leurs boîtes mail avant la mise en place d’un outil automatisé par OVHcloud. Ce guide vous explique comment effectuer cette migration manuellement.

**Découvrez comment migrer une adresse e-mail MX Plan vers Zimbra.**

## Prérequis

- Disposer d'une adresse e-mail MX Plan (via l'offre MX Plan ou incluse dans une offre d'[hébergement web OVHcloud](/links/web/hosting)).
- Disposer d'un compte e-mail actif sur Zimbra.
- **Ne pas avoir paramétré de redirection sur l'adresse e-mail MX Plan que vous souhaitez migrer**.
- Être connecté à votre [espace client OVHcloud](/links/manager).

## En pratique

### Étape 1 - Création d’une adresse e-mail sur Zimbra <a name="step1"></a>

> [!primary]
>
> Si vous disposez déjà d'une adresse e-mail Zimbra, passez à l'[Étape 2](#step2).

Pour créer une adresse e-mail Zimbra, consultez la section « Créer un compte e-mail » du guide [Premiers pas avec l'offre Zimbra](/pages/web_cloud/email_and_collaborative_solutions/zimbra/getting_started_zimbra).

### Étape 2 - Migration des e-mails <a name="step2"></a>

Utilisez l’outil de migration [**O**VH **M**ail **M**igrator](https://omm.ovh.net/){.external} (**OMM**) avec, par exemple, la configuration suivante :

- Compte e-mail source : contact@mondomaine.com (compte MX Plan)

- Compte e-mail de destination : contact2@mondomaine.com (compte Zimbra)

Pour plus de détails sur l'utilisation d'OMM, suivez notre guide « [Migrer des comptes e-mail via OVH Mail Migrator](/pages/web_cloud/email_and_collaborative_solutions/migrating/migration_omm)».

> [!primary]
>
> Le délai de migration dépend de la quantité de contenu à migrer vers votre nouveau compte. Celui-ci peut varier de quelques minutes à plusieurs heures. Une fois la migration terminée, vérifiez que tous les e-mails sont bien migrés.

### Étape 3 - Sauvegarde des e-mails du compte source (optionnelle) <a name="step3"></a>

> [!warning]
>
> Avant de supprimer votre compte MX Plan, effectuez une sauvegarde de vos e-mails pour éviter toute perte de données.

Utilisez les options d'export de votre client de messagerie. Si vous utilisez Outlook, suivez les instructions de la [documentation officielle de Microsoft](https://support.microsoft.com/fr-fr/office/sauvegarder-votre-courrier-e5845b0b-1aeb-424f-924c-aa1c33b18833){.external}.

### Étape 4 - Suppression de l'ancienne adresse e-mail MX Plan <a name="step4"></a>

Pour supprimer l'adresse e-mail MX Plan (contact@mondomaine.com), suivez notre guide « [Supprimer un compte e-mail](/pages/web_cloud/email_and_collaborative_solutions/common_email_features/email_reset_account)».

### Étape 5 - Renommage de l'adresse e-mail Zimbra <a name="step5"></a>

Dans votre espace client OVHcloud, accédez à votre service Zimbra Starter et renommez l'adresse de votre compte e-mail Zimbra (par exemple : contact2@mondomaine.com en contact@mondomaine.com).

### Conclusion <a name="conclusion"></a>

Votre compte e-mail est maintenant entièrement migré vers Zimbra Starter. Vous pouvez désormais utiliser Zimbra pour gérer votre messagerie.

> [!warning]
>
> Si votre compte e-mail gère des informations sensibles ou si vous rencontrez des problèmes lors de la migration, nous vous recommandons d’attendre la mise en place de l’outil d’automatisation prévu dans l’espace client OVHcloud.

## Aller plus loin <a name="go-further"></a>

[Premiers pas avec l'offre Zimbra](/pages/web_cloud/email_and_collaborative_solutions/zimbra/getting_started_zimbra)

[Configurer son adresse e-mail Zimbra sur un logiciel de messagerie](/pages/web_cloud/email_and_collaborative_solutions/zimbra/zimbra_mail_apps)

[FAQ sur la solution Zimbra OVHcloud](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/faq-zimbra)

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](/links/partner).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](/links/support).

Échangez avec notre [communauté d'utilisateurs](/links/community).