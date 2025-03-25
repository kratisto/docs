---
title: "Hébergement Web - FAQ"
excerpt: "Retrouvez les principales questions posées sur les hébergements web OVHcloud"
updated: 2025-03-25
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

**Cliquez sur les questions ci-dessous pour afficher les explications.**

## Gestion de votre offre

/// details | Comment configurer mon hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.

A cet endroit, vous pourrez gérer vos certificats SSL, la version PHP appliqué à votre hébergement web, l'option CDN, les éventuels multisites, les bases de données, etc.

> [!success]
>
> Pour vous aider à configurer votre hébergement web, n'hésitez pas à consulter les rubriques « *Premiers pas* » et « *Configurer son hébergement web Perso, Pro ou Performance* » présentes sur notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting).

///


/// details | J'ai oublié le mot de passe ou l'identifiant client OVHcloud où se trouve mon hébergement web, que faire ?

En cas d'oubli de votre identifiant client OVHcloud ou du mot de passe associé à cet identifiant, réalise les étapes suivantes :

1. Rendez-vous sur l'[interface de connexion à l'espace client OVHcloud](/links/manager).
2. Cliquez sur le lien `Identifiant ou mot de passe oublié ?`{.action} présent sous la fenêtre de connexion.
3. Précisez votre identifiant client OVHcloud (exemple : **aa00000-ovh**) ou l'adresse e-mail de contact associé à votre identifiant client OVHcloud.
4. Cliquez ensuite sur le bouton `Envoyer`{.action}.

Un e-mail vous sera envoyé sur votre adresse e-mail de contact avec une procédure de réinitialisation.

> [!success]
>
> Si besoin, consultez en complément notre guide « [Modifier le mot de passe de votre compte OVHcloud](/pages/account_and_service_management/account_information/manage-ovh-password) ».

///


/// details | Comment gérer le mot de passe de l'espace de stockage FTP de son hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `FTP - SSH`{.action}.

A cet endroit, vous pourrez gérer le mot de passe FTP de votre hébergement web.

> [!success]
>
> Si besoin, consultez en complément notre guide « [Hébergement Web - Modifier le mot de passe d'un utilisateur FTP](/pages/web_cloud/web_hosting/ftp_change_password) »

///


/// details | Comment gérer le(s) mot(s) de passe de ma (mes) base(s) de données associée(s) à mon hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Bases de données`{.action}.

A cet endroit, vous pourrez gérer le(s) mot(s) de passe de votre (vos) base(s) de données associé(s) à votre hébergement web.


- Pour modifier le mot de passe de votre adresse e-mail MX Plan, suivez les instructions de [ce guide](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_change_password).

> [!success]
>
> Si besoin, consultez en complément notre guide « [Hébergement Web - Modifier le mot de passe d'une base de données](/pages/web_cloud/web_hosting/sql_change_password) »

///

/// details | Comment gérer le(s) mot(s) de passe de ma (mes) adresse(s) e-mail comprise(s) dans la solution e-mail incluse dans mon hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `E-mails`{.action} (ou `MX Plan`{.action}), puis choisissez le nom de domaine concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Emails`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite de l'adresse e-mail conernée, puis cliquez sur `Changer le mot de passe`{.action}.

A cet endroit, vous pourrez modifier le mot de passe de votre adresse e-mail (en respectant la politique des mots de passe présents dans la fenêtre de saisie).

> [!success]
>
> Si besoin, consultez en complément notre guide « [Modifier le mot de passe d'une adresse e-mail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_change_password) »

///


/// details | Comment mettre mon site web en ligne ? 

Pour mettre en ligne votre site web, vous devez disposer des éléments suivants :

- Un [nom de domaine](/links/web/domains) qui correspondra à l'adresse Web depuis laquelle votre site web sera accessible via un navigateur internet (exemple : *domain.tld*).
- Un [hébergement web](/links/web/hosting) sur lequel installer votre site web.

Les principales étapes à suivre sont le suivantes : 

1. Délimiter votre projet (site web clés en main (CMS) installé manuellement ou grâce aux modules en 1 clic OVHcloud, site web créé par vous-même ou par un prestataire, etc.).
2. Mettre en ligne les fichiers du site web sur l'espace de stockage FTP de votre hébergement web.
3. Lier le site web à une base de données (si ce dernier en utilise une).
4. Accéder à votre site web.

> [!success]
>
> Pour plus de détails sur la mise en ligne d'un site web sur un hébergement web, consultez en complément notre guide « [Hébergement web - Mettre en ligne un site web](/pages/web_cloud/web_hosting/hosting_how_to_get_my_website_online) ».
>
> Si vous choisissez d'installer un CMS (WordPress, Joomla!, PrestaShop, Drupal) avec notre solution « Modules en 1 clic », consultez en complément notre guide « [Installer son site avec les modules en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) ».
>
> Si votre site web existe déjà ailleurs et si vous souhaitez le rappatrier chez OVHcloud, consultez en complément notre guide « [Migrer son site web et ses services associés vers OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh) ».
>
> Pour vous aider à configurer votre hébergement web, n'hésitez pas à consulter notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting)

///


/// details | Comment transférer sans interruption de service mon site web, ma base de données, mon nom de domaine et mes e-mails sur les serveurs OVHcloud ? 

Les principales étapes à suivre sont le suivantes : 

1. Commander l'hébergement et les adresses e-mail chez OVHcloud
2. Créer et pré-configurer une zone DNS pour votre nom de domaine chez OVHcloud
3. Récupérer une sauvegarde complète de votre site web
4. Importer la sauvegarde de votre site web sur votre offre d'hébergement OVHcloud
5. Recréer vos adresses e-mail à l'identique chez OVHcloud
6. Déclarer les serveurs e-mail OVHcloud dans la zone DNS active de votre nom de domaine
7. Transférer le contenu de vos anciennes adresses e-mail dans vos nouvelles adresses chez OVHcloud
8. Reconfigurer vos logiciels de messagerie
9. Remplacer les serveurs DNS actifs de votre nom de domaine par ceux d'OVHcloud
10. Transférer votre nom de domaine chez OVHcloud

> [!success]
>
> Si besoin, consultez en complément notre guide « [Migrer son site web et ses services associés vers OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh) » pour obtenir l'ensemble des étapes à suivre.

///


/// details | Comment héberger plusieurs sites web sur un même hébergement web ?

Pour cela (et si votre [hébergement web](/links/web/hosting) est compatible), réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Multisite`{.action}.

A cet endroit, vous pourrez gérer les noms de domaine/sous-domaines déclarés en multisite sur votre hébergement web.

> [!success]
>
> Si besoin, consultez en complément notre guide « [Partager son hébergement web entre plusieurs sites web](/pages/web_cloud/web_hosting/multisites_configure_multisite) ».

///


/// details | Comment changer de formule d'hébergement web ?

Pour commander la formule d'hébergement web la plus adaptée à vos besoins, consultez nos offres sur [cette page](/links/web/hosting).

> [!primary]
>
> En fonction de votre formule d'hébergement web actuelle, certaines offres d'hébergement web peuvent être indisponibles. Consultez notre guide « [Faire évoluer son offre d’hébergement web »](/pages/web_cloud/web_hosting/how_to_upgrade_web_hosting_offer) » pour plus d'informations sur le sujet.

Une fois votre choix fait, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Abonnement**, cliquez sur le bouton `...`{.action} à droite de la mention `Offre`, puis sur `Changer d'offre`{.action}.
4. Sélectionnez ensuite votre nouvel abonnement, ainsi que sa durée. Validez les contrats correspondants, puis cliquez sur `Envoyer`{.action}.

> [!success]
>
> Si besoin, consultez en complément notre guide « [Faire évoluer son offre d’hébergement web »](/pages/web_cloud/web_hosting/how_to_upgrade_web_hosting_offer) ».

///


/// details | Comment conserver l'offre e-mail liée à mon hébergement web lors d'une résiliation ?

Lorsque vous résiliez ou supprimez votre hébergement web, l'offre e-mail qui est attachée est également résiliée. Pour conserver vos adresses e-mails, il vous faudra détacher l'offre e-mail **avant** la résiliation de l'hébergement web concerné.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Adresses e-mails`, puis sur `Délier mon option e-mail`{.action}.
4. Suivez les instructions pour commander une offre e-mail indépendante qui vous permettra de conserver vos adresses e-mails déjà créées.

///


/// details | Lors d'une résiliation d'un hébergement web « Performance », comment conserver l'offre Web Cloud Databases liée ?

Les hébergements web **Performance** comprennent une offre Web Cloud Databases activable gratuitement.
Lorsque vous résiliez ou supprimez votre hébergement web **Performance**, l'offre Web Cloud Databases éventuellement attachée est également résiliée. Pour conserver votre solution Web Cloud Databases, vous devrez la détacher **avant** la résiliation de l'hébergement.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Web Cloud Databases`, puis sur `Délier`{.action}.
4. Suivez les instructions pour commander une offre Web Cloud Databases indépendante qui vous permettra de conserver votre solution Web Cloud Databases déjà créée.

**Cette action est irréversible et l'offre Web Cloud Databases sera ensuite facturée indépendamment de votre hébergement web Performance.**

///


/// details | Comment augmenter la RAM d'une offre Web Cloud Databases liée à un hébergement web « Performance » ?

Pour augmenter la RAM d'une offre Web Cloud Databases liée à un hébergement web **Performance**, vous devrez obligatoirement et préalablement délier l'offre Web Cloud Databases de votre hébergement **Performance** pour basculer sur une offre supérieure.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Web Cloud Databases`, puis sur `Délier`{.action}.
4. Choisissez la durée du renouvellement la plus courte, puis poursuivez jusqu'à la validation de la commande.

**Cette action est irréversible et l'offre Web Cloud Databases sera ensuite facturée indépendamment de votre hébergement web Performance.**

Pour ensuite augmenter la RAM de votre solution Web Cloud Databases, effectuez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Web Cloud Databases`{.action}, puis choisissez la solution Web Cloud Databases concernée.
3. Sur la page qui s'affiche et dans l'encadré **Informations générales**, cliquez sur le bouton `...`{.action} à droite de la mention `RAM`, puis sur `Changer la quantité de la RAM`{.action}.
4. Suivez les instructions pour commander la quantité de RAM désirée, puis poursuivez jusqu'à la validation de la commande.

> [!success]
>
> Si besoin, consultez en complément la partie « *Modifier votre offre Web Cloud Databases* » de notre guide « [Configuration d'une offre Web Cloud Databases](/pages/web_cloud/web_cloud_databases/configure-database-server) ».

///


## Diagnostic

> [!warning]
>
> Si vous rencontrez une anomalie non-répertoriée dans cette FAQ, consultez la rubrique « *Dépanner* » présente sur notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting).

/// details | Que faire si mon site web dysfonctionne ? 

Plusieurs raisons peuvent expliquer le dysfonctionnement de votre site web. Pour en identifier la cause, commencez par vérifier qu'aucun de vos abonnements n'a besoin d'être **renouvelé** en vous connectant à votre [espace client OVHcloud](/links/manager).

Consultez ensuite les [évènements en cours sur notre infrastructure](https://www.status-ovhcloud.com/). Si tous vos services sont actifs et ne sont affectés par aucun incident ou maintenance, nous vous invitons à réaliser un diagnostic plus approfondi.

///


/// details | Que faire si, après la mise en ligne de mon site, la page « Site en construction » d'OVHcloud reste affichée ?

![site-en-construction](/pages/assets/screens/other/browsers/errors/site-en-construction.png){.thumbnail}

À l'installation de votre hébergement, OVHcloud met en place cette page d'attente sous la forme d'un fichier **index.html** contenu dans le dossier `www` de votre serveur FTP.

Ce fichier est automatiquement désactivé lors de la création de votre [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules).

Si vous avez choisi [d'installer votre site manuellement](/pages/web_cloud/web_hosting/cms_manual_installation), [connectez-vous à votre espace FTP](/pages/web_cloud/web_hosting/ftp_connection) afin de le renommer en **index.html.old**.

///


/// details | Que faire si mon site s'affiche sur une adresse web de type « xxxxx.clusterXXX.hosting.ovh.net » ?

![url-cluster](/pages/assets/screens/other/browsers/urls/url-cluster.png){.thumbnail}

Deux scénarii sont possibles. Soit votre site a été créé avec cette adresse web, soit celle-ci est apparue suite à une modification.

- **Scénario 1 :** votre site a été créé avec une adresse web de type « xxxxx.clusterXXX.hosting.ovh.net »

> [!warning]
>
> La suppression d'une base de données, comme celle d'un module en 1 clic, est définitive. Elle entraîne également la **suppression des sauvegardes** des données concernées. Avant de supprimer votre site sur l'hébergement OVHcloud, **assurez-vous d'être capable de le recréer à l'identique**. Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).
>

Dans le premier cas, après avoir réalisé toutes les sauvegardes nécessaires, supprimez votre module depuis la partie `Hébergements` de votre espace client OVHcloud :

![delete-a-module](/pages/assets/screens/control_panel/product-selection/web-cloud/web-hosting/1-click-modules/delete-a-module.png){.thumbnail}

Puis supprimez sa base de données depuis l'onglet du même nom situé à droite de votre écran, toujours dans la partie `Hébergements` :

![delete_a_database](/pages/assets/screens/control_panel/product-selection/web-cloud/web-hosting/databases/sharedsql-deletion.png){.thumbnail}
 
Enfin, relancez son installation sur le nom de domaine souhaité, en utilisant la fonctionnalité [Module en 1 clic](/pages/web_cloud/web_hosting/cms_manage_1_click_module).

- **Scénario 2 :** votre site s'affiche avec une adresse web de type « xxxxx.clusterXXX.hosting.ovh.net » suite à une modification

Si votre site s'affiche avec cette URL suite à une manipulation, restaurez-le à son état antérieur.

> [!alert]
>
> La restauration de votre hébergement OVHcloud entraînera celle de **l'ensemble des sites** qu'il contient.
>
> Lors d'une restauration, le contenu de votre espace FTP, ou celui de votre base de données, est remplacé par une sauvegarde. Vous ne pourrez donc pas récupérer ensuite les données présentes sur le serveur FTP ou celles de la base de données avant la restauration.
>

Pour restaurer le code source de votre site, consultez notre guide « [Restaurer l’espace de stockage de son hébergement web](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».

Si votre site comporte une base de données, consultez notre guide « [Restaurer une sauvegarde de votre base de données](/pages/web_cloud/web_hosting/sql_importing_mysql_database#restaurer-une-sauvegarde-depuis-lespace-client) ».

///


/// details | Que faire si mon site redirige vers le webmail-login-interface OVHcloud ?

![webmail-login-interface](/pages/assets/screens/website/webmail/webmail-login-interface.png){.thumbnail}

Cette anomalie indique une configuration erronée au niveau des [serveurs DNS](/pages/web_cloud/domains/dns_server_edit) ou de la [zone DNS](/pages/web_cloud/domains/dns_zone_edit) associés à votre nom de domaine.

Le cas le plus courant est le suivant : vous avez commandé séparément votre nom de domaine et votre hébergement, ils ne sont donc pas reliés entre eux via leur zone DNS.

Rendez-vous dans la partie `Noms de domaine`{.action} de votre [espace client OVHcloud](/links/manager). Cliquez sur le nom de domaine concerné puis sur l'onglet `Serveurs DNS`{.action}.

Notez ensuite les serveurs DNS indiqués puis rendez-vous dans l'onglet `Zone DNS`{.action}.

Comparez les `Cibles` des entrées de type `NS` indiquées dans l'onglet `Zone DNS`{.action} avec les `Serveurs DNS` indiqués dans l'onglet du même nom :

- Si les éléments sont identiques, remplacez la cible `213.186.33.5` par le code à quatre nombres noté dans l'onglet `Informations générales` sous la mention `IPv4` (pour plus de détails sur les manipulations à effectuer, suivez les instructions de [ce guide](/pages/web_cloud/domains/dns_zone_edit)).

- Si les éléments ne sont pas identiques, mais que les `Serveurs DNS` indiqués dans l'onglet du même nom apparaissent dans [cette liste](/pages/web_cloud/web_hosting/clusters_and_shared_hosting_IP), effectuez une réinitialisation en suivant les instructions de [ce guide](/pages/web_cloud/domains/dns_server_edit).

- Si les éléments ne sont pas identiques et que les `Serveurs DNS` indiqués dans l'onglet du même nom n'apparaissent pas dans [cette liste](/pages/web_cloud/web_hosting/clusters_and_shared_hosting_IP), contactez votre Webmaster ou recherchez un [prestataire spécialisé](/links/partner) via la page des [partenaires OVHcloud](/links/partner).

///


/// details | Que faire si mon site affiche une erreur « La page ne se redirige pas correctement » ?

![the-page-isnt-redirecting-properly](/pages/assets/screens/other/browsers/errors/the-page-isnt-redirecting-properly.png){.thumbnail}

> [!alert]
>
> La restauration de votre hébergement OVHcloud entraînera celle de l'ensemble des sites qu'il contient.
>
> Lors d'une restauration, le contenu de votre espace FTP, ou celui de votre base de données, est remplacé par une sauvegarde. Vous ne pourrez donc pas récupérer ensuite les données présentes sur le serveur FTP ou celles de la base de données juste avant la restauration.
>

Restaurez votre site à son état précédent :

- Pour restaurer le code source de votre site, consultez notre guide « [Restaurer l’espace de stockage de son hébergement web](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».

- Si votre site comporte une base de données, consultez notre guide « [Restaurer une sauvegarde de votre base de données](/pages/web_cloud/web_hosting/sql_importing_mysql_database#restaurer-une-sauvegarde-depuis-lespace-client) ».

Si les restaurations ne vous permettent pas de rétablir l'accès à votre site, contactez votre Webmaster ou recherchez un [prestataire spécialisé](/links/partner) sur le site des [partenaires OVHcloud](/links/partner).

///


/// details | Que faire si mon site affiche une erreur « 503 error Backend fetch failed (Varnish cache) » ?

![503_varnish](/pages/assets/screens/other/browsers/errors/http-503-backend-varnish.png){.thumbnail}

Si vous avez activé [l'option CDN](/pages/web_cloud/web_hosting/cdn_how_to_use_cdn) de votre hébergement, désactivez le mode *Maintenance* sur votre site WordPress ou PrestaShop.

Si vous n'avez pas activé cette option ni utilisé le mode *Maintenance*, contactez votre Webmaster ou recherchez un [prestataire spécialisé](/links/partner) sur le site des [partenaires OVHcloud](/links/partner).

///


/// details | Que faire si mon site affiche une erreur « Your request has been blocked » ?

![your-request-has-been-blocked](/pages/assets/screens/other/browsers/errors/your-request-has-been-blocked.png){.thumbnail}

Ce message indique que le type de requête HTTP que vous tentez de faire sur votre site est interdit pour un temps limité. Dans cette situation, [examinez les logs](/pages/web_cloud/web_hosting/logs_and_statistics) de votre site afin de déterminer quelles requêtes ont provoqué ce blocage.

Pour vous aider à corriger ces anomalies, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

///


/// details | Que faire si mon site affiche une erreur « Your IP has been banned » ?

![your-ip-has-been-banned](/pages/assets/screens/other/browsers/errors/your-ip-has-been-banned.png){.thumbnail}

Ce message indique que l'adresse IP que vous utilisez pour vous connecter à votre site est bloquée pour un temps limité. 

Dans cette situation, [examinez les logs](/pages/web_cloud/web_hosting/logs_and_statistics) de votre site, afin de déterminer quelles requêtes ont provoqué ce blocage.<br>
Vérifiez également que votre poste informatique n'est pas infecté par un virus.<br>
Vous pouvez enfin contacter l'un de [nos partenaires](/links/partner), afin qu'il vérifie le code informatique de votre site.

///


/// details | J'ai commandé un domaine comportant des accents et il s'affiche écrit de façon étrange dans mon espace client. Que dois-je faire ?

![idn-notation](/pages/assets/screens/control_panel/product-selection/web-cloud/domain-dns/general-information/idn-notation.png){.thumbnail}

Vous n'avez aucune action à mener dans cette situation. Même si votre domaine s'affiche en [notation internationalisée (IDN)](https://fr.wikipedia.org/wiki/Nom_de_domaine_internationalis%C3%A9){.external} dans votre espace client, il fonctionnera et s'affichera de façon tout à fait normale ailleurs. L'adresse Web de votre site s'affichera telle que vous l'avez demandée. Vos adresses e-mail s'afficheront également telles que vous le souhaitez chez vos correspondants.

> [!alert]
>
> Il est déconseillé d'utiliser une adresse e-mail avec un nom de domaine IDN (Internationalized Domain Name) depuis un client de messagerie (Outlook, Mail de macOS, etc.). En effet, certains clients de messagerie n'interprètent pas les noms de domaine avec des caractères accentués, ce qui bloque la transmission des e-mails. Un expéditeur vous envoyant un e-mail reçoit alors un message automatique indiquant que votre adresse e-mail n'existe pas.
>
> **Il est recommandé de réserver, en complément de votre nom de domaine avec caractères accentués, le même nom de domaine sans ces accents, afin d'éviter toute incompatibilité au niveau des échanges d'e-mails.**
>

///


## Aller plus loin <a name="go-further"></a>

[FAQ - E-mails mutualisés MX Plan](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/faq-emails)

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](/links/support).

Échangez avec notre [communauté d'utilisateurs](/links/community).