---
title: 'Comment installer un certificat SSL sur un VPS OVHcloud'
excerpt: 'Découvrez comment installer un certificat SSL sur un VPS OVHcloud'
updated: 2025-01-15
---

## Objectif

La sécurisation de votre site web est essentielle pour protéger les données sensibles de vos utilisateurs et améliorer leur confiance. Grâce à un certificat SSL (**S**ecure **S**ockets **L**ayer), vous pouvez chiffrer les échanges entre vos visiteurs et votre site web, tout en renforçant sa crédibilité. OVHcloud propose plusieurs solutions pour installer un certificat SSL sur votre VPS, notamment l'utilisation de **Let's Encrypt**, un service gratuit et automatisé, ainsi que l'option **SSL Gateway**, une solution simple et performante.

**Découvrez comment installer un certificat SSL sur un VPS OVHcloud.**

> [!warning]
>
> OVHcloud met à votre disposition des services dont la configuration, la gestion et la responsabilité vous incombent. Il vous revient de ce fait d'en assurer le bon fonctionnement.
>
> Nous mettons à votre disposition ce tutoriel afin de vous accompagner au mieux sur des tâches courantes. Néanmoins, nous vous recommandons de faire appel à un [prestataire spécialisé](https://partner.ovhcloud.com/fr/directory/) et/ou de contacter l'éditeur du service si vous éprouvez des difficultés. En effet, nous ne serons pas en mesure de vous fournir une assistance. Plus d'informations dans la section [Aller plus loin](#gofurther) de ce tutoriel.
>

## Prérequis

- Disposer d'une offre [VPS](https://www.ovhcloud.com/fr/vps/)
- Disposer d'un accès administrateur (sudo) via SSH à votre VPS
- Disposer d'un site web fonctionnel accéssible en http

## En pratique

### Sommaire

- [Étape 1 - Connectez-vous à votre VPS OVHcloud](#step1)
- [Étape 2 - Installez Certbot](#step2)
- [Étape 3 - Obtenez un certificat SSL avec Let's Encrypt](#step3)
- [Étape 4 - Configurez votre serveur web](#step4)
- [Étape 5 - Activez le renouvellement automatique](#step5)
- [SSL Gateway OVHcloud](#ssl-gateway)

### Étape 1 - Connectez-vous à votre VPS OVHcloud <a name="step1"></a>

1. Téléchargez un client SSH comme [PuTTY](https://www.putty.org/) ou utilisez le terminal intégré de votre système d'exploitation.

2. Connectez-vous à votre VPS OVHcloud avec les informations de connexion fournies :

```bash
ssh root@<vps_ip>
```
Remplacez `<vps_ip>` par l'adresse IP de votre VPS OVHcloud.

### Étape 2 - Installez Certbot <a name="step2"></a>

Certbot est un outil permettant de gérer automatiquement les certificats Let's Encrypt. Suivez les étapes ci-dessous pour installer Certbot selon votre distribution Linux.

> [!tabs]
> **Ubuntu/Debian**
>> ```bash
>> sudo apt update
>> sudo apt install certbot
>> ```
>>
> **CentOS**
>> ```bash
>> sudo yum install epel-release
>> sudo yum install certbot
>> ```
>>
> **Fedora**
>> ```bash
>> sudo dnf install certbot
>> ```

Assurez-vous que Certbot est correctement installé en exécutant la commande :

```bash
certbot --version
```
Cela doit afficher la version de Certbot installée.

### Étape 3 - Obtenez un certificat SSL avec Let's Encrypt <a name="step3"></a>

> [!primary]
>
> Si vous avez installé votre serveur web (Nginx ou Apache), nous vous recommandons d'utiliser les plugins Certbot pour automatiser la configuration SSL et activer les redirections HTTPS. Ces plugins simplifient l'installation en gérant directement les fichiers de configuration du serveur web.

#### Utilisation automatique avec les plugins Certbot Nginx ou Apache (recommandée)

Selon votre serveur web, utilisez les lignes de commandes correspondantes :

> [!tabs]
> **Nginx**
>> Installez le plugin Certbot Nginx :
>> ```bash
>> sudo apt install python3-certbot-nginx -y
>> ```
>>
>> Générez le certificat SSL :
>> ```bash
>> sudo certbot --nginx -d your_domain
>> ```
>>
> **Apache**
>> Installez le plugin Certbot Apache :
>> ```bash
>> sudo apt install python3-certbot-apache -y
>> ```
>>
>> Générez le certificat SSL :
>> ```bash
>> sudo certbot --apache -d your_domain
>> ```

Certbot configurera automatiquement le certificat SSL et la redirection HTTPS. Vérifiez que votre site web est accéssible en `https`.

#### Utilisation en mode autonome

Si vous préférez configurer manuellement votre serveur, utilisez Certbot en mode autonome. Ce mode utilise un serveur temporaire intégré à Certbot pour valider votre nom de domaine et générer un certificat SSL.

Utilisez la commande suivante pour demander un certificat :

```bash
sudo certbot certonly --standalone -d your_domain
```

Remplacez `your_domain` par votre nom de domaine.

> [!warning]
> Cette méthode arrête temporairement tout service utilisant le port 80 (par exemple un autre serveur web).

Une fois le certificat généré, les fichiers sont disponibles dans `/etc/letsencrypt/live/your_domain/` :

- `fullchain.pem` : le certificat complet.
- `privkey.pem` : la clé privée.

### Étape 4 - Configurez votre serveur web <a name="step4"></a>

> [!primary]
> Si vous avez utilisé la solution automatique (avec les plugins Certbot) précédemment ([Étape 3](#step3)), et que votre site web est accéssible en `https`, passez à l'[étape 5](step5).

#### Exemple pour Nginx

1. Ouvrez le fichier de configuration de votre site web (par exemple, `/etc/nginx/sites-available/your_domain.conf`).

2. Ajoutez les lignes suivantes pour activer le SSL :

```nginx
server {
    listen 443 ssl;
    server_name your_domain;

    ssl_certificate /etc/letsencrypt/live/your_domain/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/your_domain/privkey.pem;

    # Paramètres de sécurité supplémentaires
    ssl_protocols TLSv1.2 TLSv1.3;
    ssl_ciphers HIGH:!aNULL:!MD5;

    # Redirection HTTP vers HTTPS
    location / {
        try_files $uri $uri/ =404;
    }
}
```

3. Ajoutez une redirection automatique HTTP vers HTTPS :

```nginx
server {
    listen 80;
    server_name your_domain;
    return 301 https://$host$request_uri;
}
```

4. Testez et redémarrez Nginx :

```bash
sudo nginx -t
sudo systemctl reload nginx
```

Vérifiez que votre site web est accéssible en `https`.

#### Exemple pour Apache

1. Activez les modules SSL et headers :

```bash
sudo a2enmod ssl
sudo a2enmod headers
```

2. Modifiez la configuration de votre site web (par exemple `/etc/apache2/sites-available/your_domain.conf`) pour inclure :

```apache
<VirtualHost *:80>
    ServerName your_domain
    DocumentRoot /var/www/your_domain

    Redirect permanent / https://your_domain/

    <Directory /var/www/your_domain>
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/ssltest_error.log
    CustomLog ${APACHE_LOG_DIR}/ssltest_access.log combined
</VirtualHost>

<VirtualHost *:443>
    ServerName your_domain
    DocumentRoot /var/www/your_domain

    # Activer SSL
    SSLEngine on
    SSLCertificateFile /etc/letsencrypt/live/your_domain/fullchain.pem
    SSLCertificateKeyFile /etc/letsencrypt/live/your_domain/privkey.pem

    # Paramètres de sécurité supplémentaires
    SSLProtocol all -SSLv3 -TLSv1 -TLSv1.1
    SSLCipherSuite HIGH:!aNULL:!MD5
    SSLHonorCipherOrder on

    <Directory /var/www/your_domain>
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/ssltest_error.log
    CustomLog ${APACHE_LOG_DIR}/ssltest_access.log combined
</VirtualHost>
```

4. Testez et redémarrez Apache :

```bash
sudo apachectl configtest
sudo systemctl restart apache2
```

Vérifiez que votre site web est accéssible en `https`.

### Étape 5 - Activez le renouvellement automatique <a name="step5"></a>

Les certificats Let's Encrypt sont valides pendant 90 jours. Configurez un renouvellement automatique avec Certbot :

Testez le renouvellement automatique :

```bash
sudo certbot renew --dry-run
```

Certbot configure automatiquement une tâche `cron` ou un timer systemd pour gérer le renouvellement. Vérifiez son état avec :

```bash
sudo systemctl list-timers | grep certbot
```

### SSL Gateway OVHcloud <a name="ssl-gateway"></a>

La SSL Gateway d'OVHcloud automatise la gestion des certificats SSL, y compris leur configuration et leur renouvellement. Elle offre également une protection Anti-DDoS pour garantir la disponibilité et la sécurité des sites web.

1. Accédez à la page [SSL Gateway OVHcloud](https://www.ovhcloud.com/fr/security/ssl-gateway/).
2. Choisissez l'offre qui correspond à vos besoins et cliquez sur **Commander maintenant**.
3. Associez votre domaine à la SSL Gateway via l'interface OVHcloud.
4. Modifiez vos enregistrements DNS pour pointer vers l'adresse IP de la SSL Gateway.
5. Testez votre site web pour vérifier qu'il est bien accéssible en HTTPS.

## Aller plus loin <a name="go-further"></a>

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](https://partner.ovhcloud.com/fr/directory/).

Échangez avec notre [communauté d'utilisateurs](/links/community).