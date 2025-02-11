---
title: "MX Plan - Konfiguration Ihres E-Mail-Accounts auf Outlook für iOS"
excerpt: "Erfahren Sie, wie Sie Ihre MX Plan E-Mail-Adresse auf der mobilen Outlook für iOS-App einrichten."
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

MX Plan Accounts können auf verschiedenen, kompatiblen E-Mail-Clients eingerichtet werden. So können Sie Ihre E-Mail-Adresse von dem Gerät Ihrer Wahl aus verwenden. Die Microsoft Outlook-App für iOS ist kostenlos im Apple App Store verfügbar.

**Erfahren Sie, wie Sie Ihre MX Plan E-Mail-Adresse auf der mobilen Outlook App für iOS konfigurieren**

> [!warning]
>
> OVHcloud stellt Ihnen Dienste zur Verfügung, für deren Konfiguration, Verwaltung und Verwaltung Sie die alleinige Verantwortung tragen. Es liegt somit in Ihrer Verantwortung, sicherzustellen, dass diese ordnungsgemäß funktionieren.
>
> Wir stellen Ihnen diese Anleitung zur Verfügung, um Sie bei gängigen Aufgaben bestmöglich zu begleiten. Dennoch empfehlen wir Ihnen, falls Sie Hilfe brauchen, einen [spezialisierten Partner](https://marketplace.ovhcloud.com/c/support-collaboration) und/oder den Herausgeber des Dienstes zu kontaktieren. Für externe Dienstleistungen bieten wir leider keine Unterstützung. Weitere Informationen finden Sie im Abschnitt „Weiterführende Informationen“ dieser Anleitung.

## Voraussetzungen

- Sie besitzen eine MX Plan E-Mail-Adresse (im MX Plan Angebot oder in einem [OVHcloud Webhosting] Angebot enthalten).
- Sie haben die Outlook-App auf Ihrem mobilen Gerät [iOS](https://apps.apple.com/app/microsoft-outlook/id951937596).
- Sie haben die Login-Daten der E-Mail-Adresse, die Sie einrichten möchten.

## In der Praxis

## In der praktischen Anwendung <a name="add-account"></a>

- **Wenn die Anwendung zum ersten Mal gestartet wird** : Ein Konfigurationsassistent wird angezeigt. Tippen Sie auf `Account hinzufügen`{.action}.

![Outlook iOS](images/outlook-app-ios-add01.png){.thumbnail .w-400 .h-600}

- **Wenn bereits ein Account eingerichtet wurde** :
    1. Tippen Sie auf den Kreis mit den Initialen des angezeigten E-Mail-Accounts oder das Haussymbol &#8962; oben links auf Ihrem Bildschirm.
    2. Drücken Sie das Zahnrad &#9881; unten links auf Ihrem Bildschirm.
    3. Tippen Sie anschließend im Menü **Einstellungen** auf `Konten`{.action}.
    4. Tippen Sie auf `Konto hinzufügen`{.action}.
    5. Drücken Sie `E-Mail-Konto`{.action}.

![Outlook iOS](images/outlook-app-ios-add02.png){.thumbnail .w-400 .h-600}

Folgen Sie den Installationsschritten, indem Sie unten auf die Registerkarten klicken:

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
>> - Wenn im Fenster für die Kontoeinstellungen oben " **Exchange** " angezeigt wird, drücken Sie die Schaltfläche `?` in der rechten oberen Ecke des Bildschirms **(1)** und wählen Sie `Kontoanbieter wechseln`{.action} **(2)**. Wählen Sie nun `IMAP`**(3)** aus und fahren Sie mit Schritt 3 fort.
>>
>> ![Outlook iOS](images/outlook-app-ios-add-step02.png){.thumbnail .w-400 .h-600}
>>
> **Schritt 3**
>>
>> Aktivieren Sie im folgenden Fenster `Erweiterte Einstellungen`{.action} und geben Sie die folgenden Informationen ein:
>>
>> - **E-Mail-Adresse**
>> - **Anzeigename**: Geben Sie Ihre vollständige E-Mail-Adresse ein
>> - **Beschreibung**
>> - **IMAP-Posteingangsserver**:<br>- **IMAP-Hostname**: Geben Sie für den **EUROPE**: `imap.mail.ovh.net` oder `ssl0.ovh.net` ein. Geben Sie für das**AMERIKA/ASIEN** `imap.mail.ovh.ca`<br>- **IMAP-Port**: 993<br>- **IMAP-Benutzername**: Ihre vollständige E-Mail-Adresse<br>- **IMAP-Passwort**: das Passwort Ihrer E-Mail-Adresse<br>- **Portsicherheit**: SSL
>> - **SMTP-Posteingangsserver**:<br>- **SMTP-Hostname**: Geben Sie für den **EUROPE**: `smtp.mail.ovh.net` oder `ssl0.ovh.net` ein. Geben Sie für das**AMERIKA/ASIEN** `smtp.mail.ovh.ca`<br>- **SMTP-Port**: 465<br>- **SMTP-Benutzername**: Ihre vollständige E-Mail-Adresse<br>- **SMTP-Passwort**: das Passwort Ihrer E-Mail-Adresse<br>- **Portsicherheit**: SSL
>>
>> Um die Konfiguration abzuschließen, drücken Sie `Verbinden`{.action}.
>>
>> ![Outlook iOS](images/outlook-app-ios-add-step03-imap-eu.png){.thumbnail .w-400 .h-600}
>>

> [!warning]
>
> Wenn Sie nach dem Befolgen der obigen Konfigurationsschritte einen Fehler beim Senden oder Empfangen feststellen, lesen Sie den Abschnitt „[Vorhandene Einstellungen ändern](#modify-settings)“.

### E-Mail-Adresse verwenden

Nach der Konfiguration der E-Mail-Adresse können Sie diese verwenden! Sie können ab sofort Nachrichten senden und empfangen.

OVHcloud bietet auch eine Web-App, mit der Sie über einen Webbrowser auf Ihre E-Mail-Adresse zugreifen können. Sie können über folgenden Link darauf zugreifen: [Webmail](/links/web/email). Sie können sich mit den Login-Daten Ihrer E-Mail-Adresse anmelden. Wenn Sie Fragen zur Verwendung dieses Angebots haben, lesen Sie unsere Anleitungen zu dem Ihrem Angebot zugeordneten Webmail:

- [Den Account über das OWA Interface einsehen](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa)
- [E-Mail-Adresse über RoundCube Webmail verwenden](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_roundcube)
- [Zimbra Webmail verwenden](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra).

### Vorhandene Einstellungen ändern <a name=„modify-settings“></a>

1. Tippen Sie auf den Kreis mit den Initialen des angezeigten E-Mail-Accounts oder das Haussymbol „&#8962;“ oben links auf Ihrem Bildschirm.
2. Drücken Sie das Zahnrad „&#9881;“ unten links auf Ihrem Bildschirm.
3. Tippen Sie anschließend im Menü **Einstellungen** auf `Konten`{.action}.
4. Wählen Sie das entsprechende Konto aus.
5. Tippen Sie auf `Anmeldeinformationen bearbeiten`{.action}.

![Outlook iOS](images/outlook-app-ios-modify-account-01.png){.thumbnail .w-400 .h-600}

Die Einstellungen finden Sie in **Schritt 3** im Kapitel [Account hinzufügen](#add-account).

### E-Mail-Account löschen <a name=„delete“></a>

1. Tippen Sie auf den Kreis mit den Initialen des angezeigten E-Mail-Accounts oder das Haussymbol „&#8962;“ oben links auf Ihrem Bildschirm.
2. Drücken Sie das Zahnrad „&#9881;“ unten links auf Ihrem Bildschirm.
3. Tippen Sie anschließend im Menü **Einstellungen** auf `Konten`{.action}.
4. Wählen Sie das entsprechende Konto aus.
5. Drücken Sie `Account löschen`{.action}.

![Outlook iOS](images/outlook-app-ios-modify-delete-01.png){.thumbnail .w-400 .h-600}

### POP-, IMAP- und SMTP-Einstellungen zurückrufen <a name=„popimap-settings“></a>

#### IMAP- und POP-Empfangseinstellungen

Für den Empfang von E-Mails empfehlen wir Ihnen bei der Auswahl des Kontotyps die Verwendung von **IMAP**. Sie können jedoch **POP** auswählen.

> [!warning]
>
> Es ist notwendig, den Ihrem Standort entsprechenden Wert richtig zu notieren (**EUROPE** oder **AMERICA/ASIEN-PAZIFIK**)

Folgen Sie den Installationsschritten, indem Sie unten auf die Registerkarten klicken:

> [!tabs]
> **IMAP-Konfiguration**
>>
>> - **Benutzername**: Geben Sie die E-Mail-Adresse ein **vollständig**
>> - **Passwort**: Geben Sie das Passwort der E-Mail-Adresse ein
>> - **EUROPE Server (eingehend)**: imap.mail.ovh.net **oder** ssl0.ovh.net
>> - **SERVER AMERIKA/ASIEN-PAZIFIK (eingehend)**: imap.mail.ovh.ca
>> - **Port**: 993
>> - **Sicherheitstyp**: SSL/TLS
>>
> **POP-Konfiguration**
>>
>> - **Benutzername**: Geben Sie die E-Mail-Adresse ein **vollständig**
>> - **Passwort**: Geben Sie das Passwort der E-Mail-Adresse ein
>> - **EUROPE Server (eingehend)**: pop.mail.ovh.net **oder** ssl0.ovh.net
>> - **SERVER AMERIKA/ASIEN-PAZIFIK (eingehend)**: pop.mail.ovh.ca
>> - **Port**: 995
>> - **Sicherheitstyp**: SSL/TLS

#### SMTP-Sendeeinstellungen

Wenn Sie zum Senden von E-Mails die **SMTP**-Einstellungen in den Kontoeinstellungen manuell eingeben müssen, verwenden Sie die folgenden Einstellungen:

**SMTP-Konfiguration**

- **Benutzername**: Geben Sie die E-Mail-Adresse ein **vollständig**
- **Passwort**: Geben Sie das Passwort der E-Mail-Adresse ein
- **EUROPE Server (eingehend)**: pop.mail.ovh.net **oder** ssl0.ovh.net
- **SERVER AMERIKA/ASIEN-PAZIFIK (eingehend)**: pop.mail.ovh.ca
- **Port**: 465
- **Sicherheitstyp**: SSL/TLS

> [!PRIMARY]
>
> **Konfiguration ändern**
>
> Wenn Ihre E-Mail-Adresse mit **IMAP** konfiguriert ist und Sie diese Konfiguration in **POP** ändern möchten, müssen Sie den Account löschen und ihn anschließend mit **POP** neu erstellen. Lesen Sie das Kapitel „[Vorhandene Einstellungen ändern](#modify-settings)“ in dieser Anleitung.

## Weiterführende Informationen

Für spezielle Dienstleistungen (Referenzierung, Entwicklung etc.) wenden Sie sich bitte an die [OVHcloud Partner](/links/partner).

Wenn Sie Hilfe bei der Verwendung und Konfiguration Ihrer OVHcloud Lösungen benötigen, empfehlen wir Ihnen unsere verschiedenen [Support-Angebote](/links/support).

Für den Austausch mit unserer [User Community](/links/community).