---
title: "Wie Sie richtig mit Ihrem Webhosting starten"
excerpt: "Erfahren Sie, wie Sie mit unseren Optionen für „1-Klick-Module“ eine neue Website online stellen, wie Sie eine neue personalisierte E-Mail-Adresse mit Ihrem Domainnamen erstellen, und all das mit unserer Webhosting-Lösung"
updated: 2025-04-02
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

## Ziel

Sie möchten eine Website für Ihr Unternehmen oder einen persönlichen Blog erstellen? Oder können Sie einen E-Commerce einrichten, um Ihre Produkte online zu verkaufen? In dieser Anleitung für die ersten Schritte mit dem OVHcloud Webhosting werden die wichtigsten Schritte für dessen Konfiguration beschrieben. Dazu gehört auch die Erstellung von professionellen E-Mail-Adressen, die mit Ihrer Domain verbunden sind. So können Sie Ihr Projekt einfach und schnell online stellen und effizient mit Ihrem Publikum kommunizieren.

**Hier erfahren Sie, wie Sie mit unserer 1-Klick-Modul-Lösung ganz einfach und schnell eine neue Website online stellen. In dieser Anleitung erfahren Sie auch, wie Sie eine neue personalisierte E-Mail-Adresse mit Ihrer Domain erstellen.**

> [!PRIMARY]
>
> Wenn Sie eine bereits bestehende Website zu einem anderen Hosting-Anbieter migrieren möchten, lesen Sie unsere Anleitung direkt: [Website und zugehörige Dienste zu OVHcloud migrieren](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh).

## Voraussetzungen

- Sie verfügen über ein [OVHcloud Webhosting](/links/web/hosting) Angebot mit mindestens einer verfügbaren Datenbank.
- Sie haben die Bestätigungs-E-Mail zur Installation Ihres Webhostings erhalten.
- Sie besitzen eine [Domainname](/links/web/domains) und eine zugehörige DNS-Zone bei OVHcloud.
- Alle oben genannten Dienste müssen von einem einzigen OVHcloud Account aus erreichbar sein.
- Sie sind in Ihrem [OVHcloud Kundencenter](/links/manager) eingeloggt und befinden sich im Bereich `Web Cloud`{.action}.

## In der praktischen Anwendung

### 1 - Verbinden Sie Ihre Domain mit Ihrem Webhosting <a name="part-1"></a>

> [!success]
>
> Wenn Sie Ihren Domainnamen und Ihr Webhosting in einer Bestellung abonniert haben, sind diese beiden Dienste bereits verbunden. Wechseln Sie direkt zu [Teil 2](#part-2) dieser Anleitung.

1. Klicken Sie auf das Menü `Hosting-Pakete`{.action} und wählen Sie das betreffende Webhosting aus.
2. Wählen Sie den Tab `Multisite`{.action}, nachdem Sie sich auf dem betreffenden Webhosting befinden.
3. Klicken Sie auf der angezeigten Seite auf den Button `Aktionen`{.action} oberhalb der Tabelle, in der die bereits für das Webhosting deklarierten Domainnamen aufgeführt sind. Klicken Sie dann auf `Domain oder Subdomain hinzufügen`{.action}.
4. Aktivieren Sie im angezeigten Fenster die angeforderten Elemente, und geben Sie sie ein, bis sie validiert wurden.

/// details | Klicken Sie hier für weitere Informationen.

Lesen Sie unsere detaillierten Anleitungen:

- [Webhosting - Mehrere Websites auf einem Webhosting hosten](/pages/web_cloud/web_hosting/multisites_configure_multisite).
- [Webhosting - Bereits zugewiesenen Domainnamen bearbeiten](/pages/web_cloud/web_hosting/multisites_modify_domain).

///

### 2 - Installieren Sie ein „1-Klick-Module“ für Ihre Website <a name="part-2"></a>

Auf seinen Webhostings bietet OVHcloud die kostenlose Installation der CMS WordPress, Joomla!, PrestaShop und Drupal mit der Option „1-Klick-Module“ an.

1. Klicken Sie auf das Menü `Hosting-Pakete`{.action} und wählen Sie das betreffende Webhosting aus.
2. Wählen Sie den Tab `1-Klick-Module`{.action}, nachdem Sie sich auf dem betreffenden Webhosting befinden.
3. Klicken Sie auf der angezeigten Seite auf die Schaltfläche `Modul hinzufügen`{.action}.
4. Wählen Sie im angezeigten Fenster das CMS aus, das Sie installieren möchten. Wählen Sie dann die Domain aus, auf der das Modul installiert werden soll, indem Sie den gewünschten Domainnamen auswählen **ohne** die vorangestellten „www“ (Beispiel: `domain.tld` und nicht `www.domain.tld`) und klicken Sie dann direkt auf `Installieren`{.action}.

/// details | Klicken Sie hier für weitere Informationen.

Lesen Sie unsere detaillierten Anleitungen:

- [Installation Ihrer Website mit einem „1-Klick-Module“ (CMS)](/pages/web_cloud/web_hosting/cms_install_1_click_modules).
- [Wie kann ich mein 1-Klick-Module verwalten?](/pages/web_cloud/web_hosting/cms_manage_1_click_module).

///

### 3 - Aktivieren Sie die in Ihrem Webhosting enthaltenen E-Mail-Adressen <a name="part-3"></a>

> [!success]
>
> Wenn Sie Ihren Domainnamen und Ihr Webhosting in einer einzigen Bestellung bestellt haben, sind die im Webhosting enthaltenen E-Mail-Adressen bereits mit Ihrem Domainnamen verbunden. Wechseln Sie direkt zu [Teil 4](#part-4) dieser Anleitung.

1. Klicken Sie auf das Menü `Hosting-Pakete`{.action} und wählen Sie das betreffende Webhosting aus.
2. Klicken Sie auf der angezeigten Seite und in der Randleiste **Konfiguration** auf den Button `...`{.action} rechts neben `E-Mail-Adressen`{.action} und dann auf `Mein E-Mail-Angebot aktivieren`{.action}. Wählen Sie auf der neu angezeigten Seite im Bereich `(1)` die betreffende Domain aus und fahren Sie mit der Aktivierung der E-Mail-Adressen fort.

/// details | Klicken Sie hier für weitere Informationen.

Lesen Sie unsere detaillierte Anleitung „[Webhosting - Inklusiv-E-Mail-Adressen aktivieren](/pages/web_cloud/web_hosting/activate-email-hosting)“.

///

### 4 - Erstellen Sie eine personalisierte E-Mail-Adresse mit Ihrem Domainnamen <a name="part-4"></a>

1. Klicken Sie auf das Menü `E-Mails`{.action} (oder `MX Plan`{.action}, wenn Sie die neue Version des OVHcloud Kundencenters verwenden) und wählen Sie die betreffende Domain aus.
2. Klicken Sie auf der angezeigten Seite auf den Tab `E-Mails`{.action}.
3. Klicken Sie auf der neu angezeigten Seite auf die Schaltfläche `Eine E-Mail-Adresse erstellen`{.action}.
4. Geben Sie im angezeigten Fenster die angeforderten Daten ein, bis sie validiert wurden.

Wiederholen Sie diesen Vorgang für jede E-Mail-Adresse, die Sie erstellen möchten (im Rahmen Ihres Webhosting Angebots).

/// details | Klicken Sie hier für weitere Informationen.

Lesen Sie unsere detaillierte Anleitung „[E-Mail-Adresse erstellen](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_creation)“.

///

### 5 - Zusätzliche Optionen für Ihr Webhosting <a name="part-5"></a>

Ihr Webhosting ist nicht auf die Installation eines „1-Klick-Moduls“ beschränkt. Sie können selbst oder von einem Webentwickler erstellte Websites hosten (Blog, CMS, Webshop...). Wenn Sie mehr über die Möglichkeiten Ihres Webhostings erfahren möchten, lesen Sie unsere ausführlichere Anleitung „[Erstellen einer Website - Realisieren Sie Ihr Projekt in 5 Schritten](/pages/web_cloud/web_hosting/website-project)“.

## Weiterführende Informationen

Hier finden Sie einige Links zu unseren Anleitungen zu den wichtigsten Optionen, die bei unseren Webhostings verfügbar sind:

- [Webhosting - SSL-Zertifikat verwalten](/pages/web_cloud/web_hosting/ssl_on_webhosting).
- [Meine Website mithilfe des CDN beschleunigen](/pages/web_cloud/web_hosting/cdn_how_to_use_cdn).
- [Webhosting - Umgebung, PHP-Version, “.ovhconfig“](/pages/web_cloud/web_hosting/configure_your_web_hosting).
- [Webhosting - Statistiken und Logs einer Website einsehen](/pages/web_cloud/web_hosting/logs_and_statistics).
- [Verfolgen und verwalten Sie die automatischen E-Mails Ihres Webhostings](/pages/web_cloud/web_hosting/mail_function_script_records).
- [Wie kann ich eine Website in einem bestimmten Land geolokalisieren?](/pages/web_cloud/web_hosting/multisites_geolocation).
- [Application Firewall aktivieren](/pages/web_cloud/web_hosting/multisites_activating_application_firewall).
- [Konfigurieren und verwenden Sie Git mit Ihrem OVHcloud Webhosting](/pages/web_cloud/web_hosting/git_integration_webhosting).
- [Mit dem FTP-Speicherplatz Ihres Webhostings verbinden](/pages/web_cloud/web_hosting/ftp_connection).
- [Automatisierte Tasks (CRON) auf Ihrem Webhosting erstellen](/pages/web_cloud/web_hosting/cron_tasks).

Kontaktieren Sie für spezialisierte Dienstleistungen (SEO, Web-Entwicklung etc.) die [OVHcloud Partner](/links/partner).
 
Wenn Sie Hilfe bei der Nutzung und Konfiguration Ihrer OVHcloud Lösungen benötigen, beachten Sie unsere [Support-Angebote](/links/support).
 
Treten Sie unserer [User Community](/links/community) bei.