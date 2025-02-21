---
title: "MX Plan - Konfiguration Ihres E-Mail-Accounts in Outlook für iOS"
excerpt: "Erfahren Sie hier, wie Sie Ihre MX Plan E-Mail-Adresse in der Outlook App für iOS einrichten"
updated: 2025-02-10
---

<style>
.w-400 {
  max-width:400px !important;
}
.h-600 {
  max-height:600px !important;
}
</style>

## Ziel

MX Plan Accounts können auf verschiedenen kompatiblen E-Mail-Clients eingerichtet werden. So können Sie Ihr bevorzugtes Gerät für Ihre E-Mail-Adressen verwenden. Die Microsoft Outlook App für iOS ist kostenlos im Apple App Store verfügbar.

**Erfahren Sie, wie Sie Ihre MX Plan E-Mail-Adresse auf der mobilen Outlook App für iOS konfigurieren**

> [!warning]
> OVHcloud stellt Ihnen Dienstleistungen zur Verfügung, für deren Konfiguration und Verwaltung Sie die alleinige Verantwortung tragen. Es liegt somit bei Ihnen, sicherzustellen, dass diese ordnungsgemäß funktionieren.
> 
> Diese Anleitung soll Sie bei allgemeinen Aufgaben bestmöglich unterstützen. Wir empfehlen Ihnen jedoch, bei Schwierigkeiten einen [spezialisierten Dienstleister](/links/partner) oder den Herausgeber des Dienstes zu kontaktieren. Weitere Informationen finden Sie am [Ende dieser Anleitung](#go-further).
>

## Voraussetzungen

- Sie haben einen MX Plan E-Mail-Account (als MX Plan Dienst oder in einem [OVHcloud Webhosting](/links/web/hosting) enthalten).
- Microsoft Outlook ist auf Ihrem [iOS Gerät](https://apps.apple.com/app/microsoft-outlook/id951937596) installiert.
- Sie verfügen über die Login-Daten für den E-Mail-Account, den Sie konfigurieren möchten.

## In der praktischen Anwendung

### Account hinzufügen <a name="add-account"></a>

- **Wenn Sie die Anwendung zum ersten Mal starten**: Ein Konfigurationsassistent wird angezeigt. Tippen Sie auf `Account hinzufügen`{.action}.

![Outlook iOS](images/outlook-app-ios-add01.png){.thumbnail .w-400 .h-600}

- **Wenn bereits ein Account eingerichtet wurde**:
    1. Tippen Sie auf den Kreis mit den Initialen des E-Mail-Accounts oder das Home Icon "&#8962;" oben links auf dem Bildschirm.
    2. Tippen Sie das Zahnrad "&#9881;" unten links auf dem Bildschirm.
    3. Tippen Sie im Menü **Einstellungen** auf `Konten`{.action}.
    4. Tippen Sie auf `Konto hinzufügen`{.action}.
    5. Tippen Sie `E-Mail-Konto`{.action}.

![Outlook iOS](images/outlook-app-ios-add02.png){.thumbnail .w-400 .h-600}

Folgen Sie den Installationsschritten, indem Sie auf die Tabs klicken:

> [!tabs]
> **Schritt 1**
>>
>> Geben Sie Ihre E-Mail-Adresse ein und tippen Sie auf `Account hinzufügen`{.action}.
>>
>> ![Outlook iOS](images/outlook-app-ios-add-step01.png){.thumbnail .w-400 .h-600}
>>
> **Schritt 2**
>>
>> Sie haben zwei Möglichkeiten:
>>
>> - Wenn am oberen Seitenrand " **IMAP** " steht, fahren Sie mit Schritt 3 fort.
>> - Wenn im Fenster für die Kontoeinstellungen oben "**Exchange**" angezeigt wird, Tippen Sie die Schaltfläche `?` in der rechten oberen Ecke des Bildschirms **(1)** und wählen Sie `Kontoanbieter wechseln`{.action} **(2)**. Wählen Sie nun `IMAP`**(3)** aus und fahren Sie mit Schritt 3 fort.
>>
>> ![Outlook iOS](images/outlook-app-ios-add-step02.png){.thumbnail .w-400 .h-600}
>>
> **Schritt 3**
>>
>> Aktivieren Sie im folgenden Fenster `Erweiterte Einstellungen`{.action} und geben Sie die folgenden Informationen ein:
>>
>> - **E-Mail-Adresse**
>> - **Anzeigename**: Vollständige E-Mail-Adresse
>> - **Beschreibung**
>> - **IMAP-Posteingangsserver**:<br>- **IMAP-Hostname**: Für **EUROPA**: `imap.mail.ovh.net` oder `ssl0.ovh.net`. Für **AMERIKA/ASIEN**: `imap.mail.ovh.ca`<br>- **IMAP-Port**: 993<br>- **IMAP-Benutzername**: Vollständige E-Mail-Adresse.<br>- **IMAP-Passwort**: Passwort Ihres E-Mail-Accounts.<br>- **Portsicherheit**: SSL
>> - **SMTP-Posteingangsserver**:<br>- **SMTP-Hostname**: Für **EUROPA**: `smtp.mail.ovh.net` oder `ssl0.ovh.net`. Für **AMERIKA/ASIEN**: `smtp.mail.ovh.ca`<br>- **SMTP-Port**: 465<br>- **SMTP-Benutzername**: Vollständige E-Mail-Adresse.<br>- **SMTP-Passwort**: Passwort Ihres E-Mail-Accounts.<br>- **Portsicherheit**: SSL
>>
>> Um die Konfiguration abzuschließen, tippen Sie `Verbinden`{.action}.
>>
>> ![Outlook iOS](images/outlook-app-ios-add-step03-imap-eu.png){.thumbnail .w-400 .h-600}
>>

> [!warning]
>
> Wenn Sie nach dem Befolgen der Konfigurationsschritte Fehler beim Senden oder Empfangen feststellen, lesen Sie den Abschnitt "[Bestehende Einstellungen ändern](#modify-settings)".

### E-Mail-Account verwenden

Nach der Konfiguration des E-Mail-Accounts können Sie diesen verwenden und Nachrichten senden und empfangen.

OVHcloud bietet auch eine Web-Anwendung für den Zugriff auf Ihren E-Mail-Account über den Browser an. Sie können sich hier mit Ihren E-Mail-Login-Daten anmelden: [Webmail](/links/web/email). Wenn Sie Fragen zur Verwendung des Webmail für Ihren E-Mail-Dienst haben, folgen Sie der passenden Anleitung:

- [OWA Webmail](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa)
- [RoundCube Webmail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_roundcube)
- [Zimbra Webmail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra)

### Bestehende Einstellungen ändern <a name="modify-settings"></a>

1. Tippen Sie auf den Kreis mit den Initialen des E-Mail-Accounts oder das Home Icon "&#8962;" oben links auf dem Bildschirm.
2. Tippen Sie das Zahnrad "&#9881;" unten links auf dem Bildschirm.
3. Tippen Sie im Menü **Einstellungen** auf `Konten`{.action}.
4. Wählen Sie das entsprechende Konto aus.
5. Tippen Sie auf `Anmeldeinformationen bearbeiten`{.action}.

![Outlook iOS](images/outlook-app-ios-modify-account-01.png){.thumbnail .w-400 .h-600}

Die Einstellungen finden Sie in **Schritt 3** unter [Account hinzufügen](#add-account).

### E-Mail-Account löschen <a name="delete"></a>

1. Tippen Sie auf den Kreis mit den Initialen des E-Mail-Accounts oder das Home Icon "&#8962;" oben links auf dem Bildschirm.
2. Tippen Sie das Zahnrad "&#9881;" unten links auf dem Bildschirm.
3. Tippen Sie im Menü **Einstellungen** auf `Konten`{.action}.
4. Wählen Sie das entsprechende Konto aus.
5. Tippen Sie `Account löschen`{.action}.

![Outlook iOS](images/outlook-app-ios-modify-delete-01.png){.thumbnail .w-400 .h-600}

### POP-, IMAP- und SMTP-Einstellungen <a name="popimap-settings"></a>

#### IMAP und POP - Empfang

Für eingehende E-Mails empfehlen wir bei der Auswahl des Kontotyps die Verwendung von **IMAP**. Sie können aber auch **POP** auswählen.

> [!warning]
>
> Geben Sie nur die passenden Werte für Ihren Standort ein (**EUROPA** oder **AMERIKA/ASIEN-PAZIFIK**).

Folgen Sie den Installationsschritten, indem Sie auf die Tabs klicken:

> [!tabs]
> **IMAP-Konfiguration**
>>
>> - **Benutzername**: Geben Sie die **vollständige** E-Mail-Adresse ein.
>> - **Passwort**: Geben Sie das Passwort des E-Mail-Accounts ein.
>> - **Server eingehend EUROPA**: imap.mail.ovh.net **oder** ssl0.ovh.net
>> - **Server eingehend AMERIKA/ASIEN-PAZIFIK**: imap.mail.ovh.ca
>> - **Port**: 993
>> - **Sicherheitstyp**: SSL/TLS
>>
> **POP-Konfiguration**
>>
>> - **Benutzername**: Geben Sie die **vollständige** E-Mail-Adresse ein.
>> - **Passwort**: Geben Sie das Passwort des E-Mail-Accounts ein.
>> - **Server eingehend EUROPA**: pop.mail.ovh.net **oder** ssl0.ovh.net
>> - **Server eingehend AMERIKA/ASIEN-PAZIFIK**: pop.mail.ovh.ca
>> - **Port**: 995
>> - **Sicherheitstyp**: SSL/TLS

#### SMTP - Senden

Wenn Sie zum Senden von E-Mails die **SMTP**-Parameter in den Kontoeinstellungen manuell eingeben müssen, verwenden Sie die folgenden Werte:

**SMTP-Konfiguration**

- **Benutzername**: Geben Sie die **vollständige** E-Mail-Adresse ein.
- **Passwort**: Geben Sie das Passwort des E-Mail-Accounts ein.
- **Server eingehend EUROPA**: pop.mail.ovh.net **oder** ssl0.ovh.net
- **Server eingehend AMERIKA/ASIEN-PAZIFIK**: pop.mail.ovh.ca
- **Port**: 465
- **Sicherheitstyp**: SSL/TLS

> [!primary]
>
> **Konfiguration ändern**
>
> Wenn Ihr E-Mail-Account mit **IMAP** konfiguriert ist und Sie diese Konfiguration in **POP** ändern möchten, müssen der Account gelöscht und als **POP** neu erstellt werden. Lesen Sie den Abschnitt "[Vorhandene Einstellungen ändern](#modify-settings)" in dieser Anleitung.

## Weiterführende Informationen <a name="go-further"></a>

Kontaktieren Sie für spezialisierte Dienstleistungen (SEO, Web-Entwicklung etc.) die [OVHcloud Partner](/links/partner).

Wenn Sie Hilfe bei der Nutzung und Konfiguration Ihrer OVHcloud Lösungen benötigen, beachten Sie unsere [Support-Angebote](/links/support).

Treten Sie unserer [User Community](/links/community) bei.
