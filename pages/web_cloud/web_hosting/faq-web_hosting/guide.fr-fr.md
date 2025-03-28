---
title: "Hébergement Web - FAQ"
excerpt: "Retrouvez les principales questions posées sur les hébergements web OVHcloud"
updated: 2025-03-28
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
> Si besoin, consultez en complément notre guide détaillé « [Modifier le mot de passe de votre compte OVHcloud](/pages/account_and_service_management/account_information/manage-ovh-password) ».

///

/// details | Comment gérer le mot de passe de l'espace de stockage FTP de son hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `FTP - SSH`{.action}.

A cet endroit, vous pourrez gérer le mot de passe FTP de votre hébergement web.

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Hébergement Web - Modifier le mot de passe d'un utilisateur FTP](/pages/web_cloud/web_hosting/ftp_change_password) »

///

/// details | Comment gérer le(s) mot(s) de passe de ma (mes) base(s) de données associée(s) à mon hébergement web ?

> [!warning]
>
> Si vous changez le mot de passe d'une base de données utilisée par l'un de vos sites web, mettez-le à jour également dans le fichier de configuration du site web concerné. En effet, sans cette mise à jour, votre site web sera déconnecté de sa base de données et dysfonctionnera.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Bases de données`{.action}.

A cet endroit, vous pourrez gérer le(s) mot(s) de passe de votre (vos) base(s) de données associé(s) à votre hébergement web.

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Hébergement Web - Modifier le mot de passe d'une base de données](/pages/web_cloud/web_hosting/sql_change_password) »

///

/// details | Comment gérer le(s) mot(s) de passe de ma (mes) adresse(s) e-mail comprise(s) dans la solution e-mail incluse dans mon hébergement web ?

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `E-mails`{.action} (ou sur le menu `MX Plan`{.action} si vous utilisez la version bêta de l'espace client OVHcloud), puis choisissez le nom de domaine concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Emails`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite de l'adresse e-mail concernée, puis cliquez sur `Changer le mot de passe`{.action}.

A cet endroit, vous pourrez modifier le mot de passe de votre adresse e-mail (en respectant la politique des mots de passe présents dans la fenêtre de saisie).

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Modifier le mot de passe d'une adresse e-mail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_change_password) »
>
> Si vous utilisez un logiciel de messagerie (Outlook, Mail de Mac, Thunderbird, etc.), mettez à jour le mot de passe pour votre adresse e-mail. Ceci lorsque le logiciel de messagerie vous le demandera lors de son ouverture ou de sa synchronisation.
>
> Si vous avez d'autres questions sur la solution e-mail *MX Plan*, consultez notre [FAQ - E-mails](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/faq-emails)

///

/// details | Comment mettre mon site web en ligne ? 

Pour mettre en ligne votre site web, vous devez disposer au préalable des éléments suivants :

- Un [nom de domaine](/links/web/domains) qui correspondra à l'adresse Web depuis laquelle votre site web sera accessible via un navigateur internet (exemple : *domain.tld*).
- Un [hébergement web](/links/web/hosting) sur lequel installer votre site web.

Les principales étapes à suivre sont le suivantes : 

1. Délimiter votre projet (site web clés en main (CMS) installé manuellement ou grâce aux modules en 1 clic OVHcloud, site web créé par vous-même ou par un prestataire, etc.).
2. Mettre en ligne les fichiers du site web sur l'espace de stockage FTP de votre hébergement web.
3. Lier le site web à une base de données (si ce dernier en utilise une).
4. Accéder à votre site web.

> [!success]
>
> Pour plus de détails sur la mise en ligne d'un site web sur un hébergement web, consultez en complément notre guide détaillé « [Hébergement web - Mettre en ligne un site web](/pages/web_cloud/web_hosting/hosting_how_to_get_my_website_online) ».
>
> Si vous choisissez d'installer un CMS (WordPress, Joomla!, PrestaShop, Drupal) avec notre solution « Modules en 1 clic », consultez en complément notre guide détaillé « [Installer son site avec les modules en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) ».
>
> Si votre site web existe déjà ailleurs et si vous souhaitez le rappatrier chez OVHcloud, consultez en complément notre guide détaillé « [Migrer son site web et ses services associés vers OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh) ».
>
> Pour vous aider à configurer votre hébergement web, n'hésitez pas à consulter notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting)

///

/// details | Comment transférer sans interruption de service mon site web, ma base de données, mon nom de domaine et mes e-mails chez OVHcloud ? 

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
> Si besoin, consultez en complément notre guide « [Migrer son site web et ses services associés vers OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh) » pour obtenir le détail des étapes à suivre.

///

/// details | Comment héberger plusieurs sites web sur un même hébergement web ?

Pour cela (et si votre [hébergement web](/links/web/hosting) est compatible), réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Multisite`{.action}.

A cet endroit, vous pourrez gérer les noms de domaine/sous-domaines déclarés en multisite sur votre hébergement web.

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Partager son hébergement web entre plusieurs sites web](/pages/web_cloud/web_hosting/multisites_configure_multisite) ».

///

/// details | Comment afficher mon site web avec une URL en « HTTPS » ?

Pour que votre site web soit accessible avec une URL en « HTTPS » (exemple: `https://domain.tld`), deux prérequis sont nécessaires:

- Vous devez disposer d'un certificat SSL actif pour votre nom de domaine (ou installé sur votre hébergement web)
- Au niveau du code source de votre site web, celui-ci doit forcer la réécriture des URLs en « HTTPS ».

Sur les hébergements web, OVHcloud propose plusieurs certificats SSL.

Pour activer un certificat SSL sur votre hébergement web pour votre site web, réaliser les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} situé à droite de la mention **Certificat SSL**, puis sur `Commander un certificat SSL`{.action}.
4. [Choisissez le certificat que vous souhaitez parmi la liste des certificats disponibles](/pages/web_cloud/web_hosting/ssl_on_webhosting), puis poursuivez jusqu'à la finalisation du bon de commande.

> [!success]
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement web - Gérer un certificat SSL](/pages/web_cloud/web_hosting/ssl_on_webhosting) ».
> - « [Hébergement web - Activer un certificat SSL gratuit Let's Encrypt](/pages/web_cloud/web_hosting/ssl_letsencrypt) ».
> - « [Hébergement web - Activer un certificat SSL Sectigo DV](/pages/web_cloud/web_hosting/ssl_dv) ».
> - « [Hébergement web - Activer un certificat SSL Sectigo EV](/pages/web_cloud/web_hosting/ssl_ev) ».
> - « [Hébergement web - Installer un certificat SSL personnalisé](/pages/web_cloud/web_hosting/ssl_custom) ».

Une fois le certificat SSL de votre choix installé et mis en place côté OVHcloud, vérifiez que le code source de votre site web réécrit bien les URLs d'accès à votre site web en « HTTPS ». Si vous épprouvez des difficultés sur ce point, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

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
> Si besoin, consultez en complément notre guide détaillé « [Faire évoluer son offre d’hébergement web »](/pages/web_cloud/web_hosting/how_to_upgrade_web_hosting_offer) ».

///

/// details | Comment conserver l'offre e-mail liée à mon hébergement web lors d'une résiliation ?

Lorsque vous résiliez ou supprimez votre hébergement web, l'offre e-mail qui est attachée est également résiliée. Pour conserver vos adresses e-mails, il vous faudra détacher l'offre e-mail **avant** la résiliation de l'hébergement web concerné.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Adresses e-mails`, puis sur `Délier mon option e-mail`{.action}.
4. Suivez les instructions pour commander une offre e-mail indépendante qui vous permettra de conserver vos adresses e-mails déjà créées.

///

/// details | Lors d'une résiliation d'un hébergement web « Performance », comment conserver l'offre « Web Cloud Databases » liée ?

Les hébergements web **Performance** comprennent une offre Web Cloud Databases activable gratuitement.
Lorsque vous résiliez ou supprimez votre hébergement web **Performance**, l'offre Web Cloud Databases éventuellement attachée est également résiliée. Pour conserver votre solution Web Cloud Databases, vous devrez la détacher **avant** la résiliation de l'hébergement.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Web Cloud Databases`, puis sur `Délier`{.action}.
4. Suivez les instructions pour commander une offre Web Cloud Databases indépendante qui vous permettra de conserver votre solution Web Cloud Databases déjà créée.

**Cette action est irréversible et l'offre Web Cloud Databases sera ensuite facturée indépendamment de votre hébergement web Performance.**

///

/// details | Comment augmenter la RAM d'une offre « Web Cloud Databases » liée à un hébergement web « Performance » ?

Pour augmenter la RAM d'une offre Web Cloud Databases liée à un hébergement web **Performance**, vous devrez obligatoirement et préalablement délier l'offre Web Cloud Databases de votre hébergement **Performance** pour basculer sur une offre supérieure.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche et dans l'encadré **Configuration**, cliquez sur le bouton `...`{.action} à droite de la mention `Web Cloud Databases`, puis sur `Délier`{.action}.
4. Choisissez la durée du renouvellement la plus courte, puis poursuivez jusqu'à la validation de la commande.

**Cette action est irréversible et l'offre Web Cloud Databases sera ensuite facturée indépendamment de votre hébergement web Performance.**

Pour ensuite augmenter la RAM de votre solution « Web Cloud Databases », effectuez les étapes suivantes :

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
> Si vous rencontrez un dysfonctionnement non-répertorié dans cette FAQ, consultez la rubrique « *Dépanner* » présente sur notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting).

/// details | Que faire si mon site web dysfonctionne ? 

Plusieurs raisons peuvent expliquer le dysfonctionnement de votre site web. 
Pour en identifier la cause, commencez par vérifier qu'aucun de vos abonnements n'a besoin d'être **renouvelé**.

Pour cela, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Sur la page qui s'affiche, cliquez sur votre nom dans le coin supérieur droit, puis choisissez `Mes offres & services`{.action}.

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Comment renouveler mes services OVHcloud](/pages/account_and_service_management/managing_billing_payments_and_services/how_to_use_automatic_renewal) ».

Consultez ensuite les [évènements en cours sur notre infrastructure](https://www.status-ovhcloud.com/). Si tous vos services sont actifs et ne sont affectés par aucun incident ou maintenance, nous vous invitons à réaliser un diagnostic plus approfondi.

> [!success]
>
> Si besoin, consultez la rubrique « *Dépanner* » présente sur notre page regroupant l'ensemble des [guides relatifs à nos solutions d'hébergement web](/products/web-cloud-hosting).

///

/// details | Que faire si la page « Site en construction » d'OVHcloud reste affichée une fois mon site web mis en ligne ?

![site-en-construction](/pages/assets/screens/other/browsers/errors/site-en-construction.png){.thumbnail}

À l'installation de votre hébergement web, OVHcloud met en place cette page d'attente sous la forme d'un fichier **index.html** contenu dans le dossier `www` présent dans l'espace de stockage FTP de votre hébergement web.

Deux cas de figure sont possibles :

- Si vous avez installé un « [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) »: ce fichier est automatiquement supprimé par nos robots d'installation.
- Si vous avez installé votre site web manuellement: suivez alors les étapes ci-dessous:
    - [Connectez-vous à l'espace de stockage FTP de votre hébergement web](/pages/web_cloud/web_hosting/ftp_connection).
    - Une fois connecté à l'espace de stockage FTP, descendez dans le répertoire `www`.
    - Renommer le fichier **index.html** par **index.html.old**. Cela désactivera la page au bout de quelques minutes.

> [!success]
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Se connecter à l'espace FTP](/pages/web_cloud/web_hosting/ftp_connection) ».
> - « [Hébergement Web - Modifier le mot de passe d'un utilisateur FTP](/pages/web_cloud/web_hosting/ftp_change_password) ».
> - « [Tutoriel - Utiliser FileZilla avec votre hébergement web](/pages/web_cloud/web_hosting/ftp_filezilla_user_guide) ».
> - « [Tutoriel - Utiliser Cyberduck avec votre hébergement web](/pages/web_cloud/web_hosting/ftp_cyberduck_user_guide_on_mac) ».

///

/// details | Que faire si mon site web s'affiche avec une adresse web de type « xxxxx.clusterXXX.hosting.ovh.net » suite à sa création ?

![url-cluster](/pages/assets/screens/other/browsers/urls/url-cluster.png){.thumbnail}

Votre site web a été créé avec un « [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) » en utilisant, lors de son installation, l'adresse web par défaut de votre hébergement web « xxxxx.clusterXXX.hosting.ovh.net ».

> [!warning]
>
> La suppression d'une base de données, tout comme celle d'un « [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) », est définitive. Elle entraîne également la **suppression des sauvegardes** des données concernées. Avant de supprimer votre site web sur l'hébergement web, **assurez-vous d'être capable de le recréer à l'identique**. Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Restaurer l'espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».
> - « [Hébergement Web - Exporter le contenu d'une base de données](/pages/web_cloud/web_hosting/sql_database_export) ».

Par conséquent et **seulement** après avoir réalisé toutes les sauvegardes nécessaires, supprimez votre « [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) » en réalisant les actions suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Modules en 1 clic`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite dans la ligne du « module en 1 clic » concerné, puis sur `Supprimer le module`{.action}.

La suppression du « module en 1 clic » peut prendre **plusieurs minutes**.

Supprimez ensuite la base de données qui lui était associée en réalisant les actions suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Bases de données`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite dans la ligne de la base de données concernée, puis sur `Supprimer la base de données`{.action}.

La suppression de la base de données associée peut prendre **plusieurs minutes**.
 
Dès lors où les suppressions sont terminées, réalisez une nouvelle installation de votre « module en 1 clic » en veillant à bien sélectionner le nom de domaine souhaité.

> [!success]
>
> Si besoin, consultez en complément notre guide détaillé « [Hébergement Web - Installer un module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) ».

///

/// details | Que faire si mon site web s'affiche avec une adresse web de type « xxxxx.clusterXXX.hosting.ovh.net » suite à une modification ?

![url-cluster](/pages/assets/screens/other/browsers/urls/url-cluster.png){.thumbnail}

Votre site web (« [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) ») s'affiche avec l'adresse web par défaut de votre hébergement web de type « xxxxx.clusterXXX.hosting.ovh.net » suite à une modification de votre « [module en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules) ».

Si votre site web s'affiche avec cette URL suite à une manipulation, la solution la plus rapide sera de le restaurer dans un état antérieur où il fonctionnait correctement.

> [!alert]
>
> La restauration d'un hébergement web entraîne la restauration de **l'ensemble des sites web** qu'il contient.
>
> Lors d'une restauration, le contenu de votre espace de stockage FTP, ou celui de votre base de données, est remplacé de manière irréversible par une sauvegarde. Les données présentes **avant le lancement de la restauration** sur l'espace de stockage FTP ou sur la base de données à restaurer seront écrasées et perdues définitivement. Si nécessaire, veillez à récupérer une sauvegarde de ce contenu au préalable. Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Restaurer l'espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».
> - « [Hébergement Web - Exporter le contenu d'une base de données](/pages/web_cloud/web_hosting/sql_database_export) ».

Pour restaurer le code source de votre site web, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `FTP - SSH`{.action}.
4. Sur la nouvelle page qui apparaît cliquez sur le bouton `Restaurer une sauvegarde`{.action}.
5. Dans la fenêtre qui s'affiche, choisissez la date de la sauvegarde à restaurer, puis poursuivez jusqu'au lancement de la restauration.

La restauration de l'espace de stockage FTP peut prendre **plusieurs minutes**.

Pour restaurer une sauvegarde de votre base de données, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Bases de données`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite dans la ligne de la base de données concernée, puis sur `Restaurer une sauvegarde`{.action}.
5. Sur la nouvelle page qui s'affiche, choisissez la sauvegarde à restaurer (**idéalement celle correspondant à la date choisie pour la restauration du code source de votre site web juste avant**).
6. Une fois la sauvegarde choisie, cliquez sur le bouton `...`{.action} situé à droite de la sauvegarde à restaurer, puis sur `Restaurer la sauvegarde`{.action}.

La restauration de la sauvegarde d'une base de données peut prendre **plusieurs minutes**.

> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Restaurer l'espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».
> - « [Restaurer une sauvegarde de votre base de données](/pages/web_cloud/web_hosting/sql_importing_mysql_database) ».

///

/// details | Que faire si mon site web redirige vers l'interface de connexion au Webmail OVHcloud ?

![webmail-login-interface](/pages/assets/screens/website/webmail/webmail-login-interface.png){.thumbnail}

Cette situation indique une configuration erronée au niveau des [serveurs DNS](/pages/web_cloud/domains/dns_server_edit) ou de la [zone DNS](/pages/web_cloud/domains/dns_zone_edit) associés à votre nom de domaine.

Le cas le plus courant est le suivant : vous avez commandé séparément votre nom de domaine et votre hébergement web, ils ne sont donc pas automatiquement reliés entre eux via la zone DNS de votre nom de domaine.

Pour corriger cela, réaliser les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Noms de domaine`{.action}, puis choisissez le nom de domaine concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Serveurs DNS`{.action}.
4. Notez ensuite les noms des serveurs DNS indiqués, puis rendez-vous dans l'onglet `Zone DNS`{.action} (à droite de l'onglet `Serveurs DNS`{.action}).
5. Dans le tableau (représentant la zone DNS du nom de domaine) qui apparaît, comparez les `Cibles` des entrées de type `NS` présentes dans la zone DNS avec les noms des serveurs DNS récupérés précédemment. 3 cas de figure peuvent survenir. Cliquez sur les onglets ci-dessous afin d'afficher successivement chacun des **3** cas.

> [!tabs]
> **Cas n°1**
>>
>> Les `Cibles` (serveurs DNS) des entrées de type `NS` déclarées dans la zone DNS du nom de domaine **sont identiques** à ceux récupérés dans l'onglet `Serveurs DNS`{.action}.
>>
>> Dans ce cas, cela signifie que votre nom de domaine (ou son sous-domaine en *www*) pointe vers l'adresse IP de notre serveur de redirection (213.186.33.5).
>>
>> 1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
>> 2. Cliquez sur le menu `Noms de domaine`{.action} (ou sur le menu `Zones DNS`{.action} si vous utilisez la version bêta de l'espace client OVHcloud), puis choisissez le nom de domaine concerné.
>> 3. Sur la page qui s'affiche, cliquez sur l'onglet `Zone DNS`{.action}.
>> 4. Dans le tableau qui apparaît (représentant la zone DNS de votre nom de domaine), identifiez l'entrée de type `A` dont la `Cible` a pour valeur l'adresse IP `213.186.33.5`.
>> 5. Cliquez sur le bouton `...`{.action} situé à droite de la ligne, puis sur `Modifier l'entrée`{.action}.
>> 6. Dans la fenêtre qui s'ouvre, remplacer dans le formulaire `Cible*` l'adresse IP `213.186.33.5` par l'adresse IP de l'hébergement web où se trouve votre site web.
>>
>> > [!success]
>> >
>> > Si besoin, consultez en complément les guides détaillés suivants :
>> >
>> > - « [Éditer une zone DNS OVHcloud](/pages/web_cloud/domains/dns_zone_edit) ».
>> > - « [Hébergement web - Liste des adresses IP par cluster](/pages/web_cloud/web_hosting/clusters_and_shared_hosting_IP) ».
>>
> **Cas n°2**
>>
>> Les `Cibles` (serveurs DNS) des entrées de type `NS` déclarées dans la zone DNS du nom de domaine **ne sont pas identiques** à ceux récupérés dans l'onglet `Serveurs DNS`{.action}. Cependant, les `Cibles` (serveurs DNS) ont l'une des formes suivantes : 
>>
>> - `nsXX.ovh.net` et `dnsXX.ovh.net` **ou** `nsXXX.ovh.net` et `dnsXXX.ovh.net` (où chaque `X` désigne un chiffre compris entre **0** et **9**);
>> - `nsXX.ovh.ca` et `dnsXX.ovh.ca` **ou** `nsXXX.ovh.ca` et `dnsXXX.ovh.ca` (où chaque `X` désigne un chiffre compris entre **0** et **9**);
>> - `ns200.anycast.me` et `dns200.anycast.me` (si vous avez souscrit à l'option [DNS anycast](/links/web/domains-options)).
>>
>> > [!primary]
>> > 
>> > Si l'un de vos serveurs DNS déclarés dans l'onglet `Serveurs DNS`{.action} à la forme suivante : `sdnsX.ovh.net`, `sdnsX.ovh.ca`, `vpsXXXXXX.ovh.net` ou `vpsXXXXXX.ovh.ca` (où chaque `X` désigne un chiffre compris entre **0** et **9**), consultez directement le **Cas n°3**.
>> > En effet, il s'agit de noms de serveurs DNS fournis par OVHcloud permettant uniquement à nos clients d'héberger leur configuration DNS directement sur leur propre serveurs (Serveurs dédiés, VPS, etc.).
>>
>> Dans ce cas, cela signifie que votre nom de domaine n'utilise pas les bons serveurs DNS OVHcloud pour appliquer la configuration de la zone DNS présente dans l'onglet `Zone DNS`{.action}.
>>
>> Pour corriger cela, réalisez les étapes suivantes :
>>
>> 1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
>> 2. Cliquez sur le menu `Noms de domaine`{.action}, puis choisissez le nom de domaine concerné.
>> 3. Sur la page qui s'affiche, cliquez sur l'onglet `Serveurs DNS`{.action}.
>> 4. Sur la nouvelle page qui apparaît, cliquez sur le bouton `Modifier les serveurs DNS`{.action}.
>> 5. Sur la page qui s'affiche, sélectionnez le choix `Utiliser les DNS par défaut d'OVHcloud`{.action}, puis cliquez sur le bouton `Appliquez la configuration`{.action}.
>>
>> La propagation de la mise à jour des serveurs DNS appliqués à un nom de domaine peut prendre jusqu'à **48** heures.
>>
>> > [!success]
>> >
>> > Si besoin, consultez en complément notre guide détaillé « [Modifier les serveurs DNS d'un nom de domaine OVHcloud](/pages/web_cloud/domains/dns_server_edit) ».
>>
> **Cas n°3**
>>
>> Les `Cibles` (serveurs DNS) des entrées de type `NS` déclarées dans la zone DNS du nom de domaine **ne sont pas identiques** à ceux récupérés dans l'onglet `Serveurs DNS`{.action}. De plus, les noms des serveurs DNS récupérés dans l'onglet `Serveurs DNS`{.action} n'ont aucune des formes décrites dans le **Cas n°2**; exception faite pour les formes suivantes : `sdnsX.ovh.net`, `sdnsX.ovh.ca`, `vpsXXXXXX.ovh.net` ou `vpsXXXXXX.ovh.ca` (où chaque `X` désigne un chiffre compris entre **0** et **9**).
>>
>> Dans ce cas, cela siginfie que la zone DNS active appliquée à votre nom de domaine n'est pas gérée par OVHcloud directement. Contactez votre Webmaster, votre fournisseur de nom de domaine, votre fournisseur DNS ou l'un de nos [partenaires](/links/partner).

///

/// details | Que faire si mon site web affiche une erreur « La page ne se redirige pas correctement » ?

![the-page-isnt-redirecting-properly](/pages/assets/screens/other/browsers/errors/the-page-isnt-redirecting-properly.png){.thumbnail}

Dans ce cas de figure, la solution la plus rapide sera de le restaurer dans un état antérieur où il fonctionnait correctement.

> [!alert]
>
> La restauration d'un hébergement web entraîne la restauration de **l'ensemble des sites web** qu'il contient.
>
> Lors d'une restauration, le contenu de votre espace de stockage FTP, ou celui de votre base de données, est remplacé de manière irréversible par une sauvegarde. Les données présentes **avant le lancement de la restauration** sur l'espace de stockage FTP ou sur la base de données à restaurer seront écrasées et perdues définitivement. Si nécessaire, veillez à récupérer une sauvegarde de ce contenu au préalable. Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Restaurer l'espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».
> - « [Hébergement Web - Exporter le contenu d'une base de données](/pages/web_cloud/web_hosting/sql_database_export) ».

Pour restaurer le code source de votre site web, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `FTP - SSH`{.action}.
4. Sur la nouvelle page qui apparaît cliquez sur le bouton `Restaurer une sauvegarde`{.action}.
5. Dans la fenêtre qui s'affiche, choisissez la date de la sauvegarde à restaurer, puis poursuivez jusqu'au lancement de la restauration.

La restauration de l'espace de stockage FTP peut prendre **plusieurs minutes**.

Pour restaurer une sauvegarde de votre base de données, réalisez les étapes suivantes :

1. Connectez-vous à votre [espace client OVHcloud](/links/manager), puis rendez-vous dans la partie `Web Cloud`{.action}.
2. Cliquez sur le menu `Hébergements`{.action}, puis choisissez l'hébergement web concerné.
3. Sur la page qui s'affiche, cliquez sur l'onglet `Bases de données`{.action}.
4. Dans le tableau qui apparaît, cliquez sur le bouton `...`{.action} situé à droite dans la ligne de la base de données concernée, puis sur `Restaurer une sauvegarde`{.action}.
5. Sur la nouvelle page qui s'affiche, choisissez la sauvegarde à restaurer (**idéalement celle correspondant à la date choisie pour la restauration du code source de votre site web juste avant**).
6. Une fois la sauvegarde choisie, cliquez sur le bouton `...`{.action} situé à droite de la sauvegarde à restaurer, puis sur `Restaurer la sauvegarde`{.action}.

La restauration de la sauvegarde d'une base de données peut prendre **plusieurs minutes**.

> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement Web - Restaurer l'espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_save_and_backup) ».
> - « [Restaurer une sauvegarde de votre base de données](/pages/web_cloud/web_hosting/sql_importing_mysql_database) ».

Si les restaurations ne vous permettent pas de rétablir l'accès à votre site web, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

///

/// details | Que faire si mon site web affiche une erreur « 503 error Backend fetch failed (Varnish cache) » ?

![503_varnish](/pages/assets/screens/other/browsers/errors/http-503-backend-varnish.png){.thumbnail}

Si vous avez activé [l'option CDN](/pages/web_cloud/web_hosting/cdn_how_to_use_cdn) de votre hébergement web, désactivez le mode *Maintenance* sur votre site WordPress ou PrestaShop.

Si vous n'avez pas activé cette option ni utilisé le mode *Maintenance*, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

> [!success]
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Accélérer mon site web en utilisant le CDN](/pages/web_cloud/web_hosting/cdn_how_to_use_cdn) ».
> - « [Résoudre les erreurs les plus fréquentes liées aux modules en 1 clic](/pages/web_cloud/web_hosting/diagnostic_errors_module1clic) ».

///

/// details | Que faire si mon site web affiche une erreur « Your request has been blocked » ?

![your-request-has-been-blocked](/pages/assets/screens/other/browsers/errors/your-request-has-been-blocked.png){.thumbnail}

Ce message indique que le type de requête HTTP que vous tentez de faire sur votre site web est interdit pour un temps limité. Ceci généralement pour des raisons de sécurité.

Dans cette situation, plusieurs actions sont requises :

- [Examinez les logs](/pages/web_cloud/web_hosting/logs_and_statistics) de votre site web, afin de déterminer quelles requêtes ont provoqué ce blocage.
- Vérifiez que vos appareils (ordinateurs, smartphones, etc.) ne sont pas infectés par un logiciel espion ou malveillant à l'aide d'un logiciel anti-virus ou anti-spyware.
- Vérifiez le code source de votre site web (espace de stockage FTP et base(s) de données). 

Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

> [!success]
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement web - Consulter les statistiques et logs d'un site web](/pages/web_cloud/web_hosting/logs_and_statistics) ».
> - « [Cas d'usage - Conseils suite au piratage de votre site Web](/pages/web_cloud/web_hosting/cms_what_to_do_if_your_site_is_hacked) ».

///

/// details | Que faire si mon site web affiche une erreur « Your IP has been banned » ?

![your-ip-has-been-banned](/pages/assets/screens/other/browsers/errors/your-ip-has-been-banned.png){.thumbnail}

Ce message indique que l'adresse IP que vous utilisez pour vous connecter à votre site web est bloquée pour un temps limité. Ceci généralement pour des raisons de sécurité.

Dans cette situation, plusieurs actions sont requises :

- [Examinez les logs](/pages/web_cloud/web_hosting/logs_and_statistics) de votre site web, afin de déterminer quelles requêtes ont provoqué ce blocage.
- Vérifiez que vos appareils (ordinateurs, smartphones, etc.) ne sont pas infectés par un logiciel espion ou malveillant à l'aide d'un logiciel anti-virus ou anti-spyware.
- Vérifiez le code source de votre site web (espace de stockage FTP et base(s) de données). 

Si vous n'êtes pas certain des manipulations à effectuer, contactez votre Webmaster ou l'un de nos [partenaires](/links/partner).

> [!success]
>
> Si besoin, consultez en complément les guides détaillés suivants :
>
> - « [Hébergement web - Consulter les statistiques et logs d'un site web](/pages/web_cloud/web_hosting/logs_and_statistics) ».
> - « [Cas d'usage - Conseils suite au piratage de votre site Web](/pages/web_cloud/web_hosting/cms_what_to_do_if_your_site_is_hacked) ».

///

/// details | J'ai commandé un nom de domaine comportant des accents et il s'affiche écrit de façon étrange dans mon espace client. Que dois-je faire ?

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

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](/links/partner).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](/links/support).

Échangez avec notre [communauté d'utilisateurs](/links/community).