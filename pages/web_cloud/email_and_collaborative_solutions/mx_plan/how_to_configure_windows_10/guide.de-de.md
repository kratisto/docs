---
title: MX Plan - Konfiguration Ihres E-Mail-Accounts in Mail für Windows
excerpt: Erfahren Sie hier, wie Sie Ihre MX Plan E-Mail-Adresse in der Mail App von Windows einrichten
updated: 2024-10-01
---

## Ziel

E-Mail-Adressen aus dem MX Plan Angebot können auf einem kompatiblen E-Mail-Client eingerichtet werden. So können Sie Ihre bevorzugte App für den Versand und den Empfang Ihrer E-Mails verwenden.

**Diese Anleitung erklärt, wie Sie Ihren MX Plan E-Mail-Account in der Mail App von Windows 10 einrichten.**

## Voraussetzungen

- Sie verfügen über einen MX Plan E-Mail-Account (im MX Plan Angebot oder in einem [OVHcloud Webhosting](/links/web/hosting) enthalten).
- Sie haben die Anwendung Mail auf Ihrem Gerät installiert.
- Sie verfügen über die Login-Daten für den E-Mail-Account, den Sie konfigurieren möchten.

## In der praktischen Anwendung

### Schritt 1: Account hinzufügen

Nachdem Sie die Mail App auf Ihrem Gerät gestartet haben, können Sie einen Account auf zwei Arten hinzufügen:

- **Wenn Sie die App zum ersten Mal starten**, öffnet sich ein Fenster mit der Option `Konto hinzufügen`{.action}.

- **Wenn Sie bereits einen Account eingerichtet haben**, klicken Sie im linken Menü der Anwendung auf `Konten verwalten`{.action} und im daraufhin rechts angezeigten Menü auf `Konto hinzufügen`{.action}.

![mx plan](images/configuration-mail-windows-step1.png){.thumbnail}

Klicken Sie im nächsten Fenster auf `Erweitertes Setup`{.action} und wählen Sie `Internet E-Mail`{.action} als Kontotyp aus.

Geben Sie nun folgende Informationen ein:

|Information|Beschreibung|
|---|---|
|E-Mail-Adresse|Geben Sie die vollständige E-Mail-Adresse ein.|
|Benutzername|Geben Sie die vollständige E-Mail-Adresse ein.|
|Kennwort|Geben Sie das Passwort der E-Mail-Adresse ein.|
|Kontoname|Geben Sie einen Namen für diesen Account ein, damit Sie ihn später von anderen Accounts in der Mail App unterscheiden können.|
|Sendet Ihre Nachrichten unter diesem Namen|Geben Sie den Namen an, der als Absender angezeigt werden soll, wenn E-Mails mit dieser Adresse verschickt werden.|
|Posteingangsserver|Geben Sie den Server „ssl0.ovh.net:993“ ein.|
|Kontotyp|Wir empfehlen die Verwendung von **IMAP**. Sie können auch **POP** im Drop-down-Menü auswählen (dann werden Ihre E-Mails lokal in Ihrer Mail App gespeichert).|
|Postausgangsserver|Geben Sie den Server „ssl0.ovh.net:465“ ein.|

Überprüfen Sie, dass die folgenden Haken gesetzt sind:

- „Ausgangsserver erfordert Authentifizierung“
- „Benutzernamen und Kennwort auch zum Senden von E-Mail verwenden“
- „SSL für eingehende E-Mails erforderlich“
- „SSL für ausgehende E-Mails erforderlich“

Nachdem Sie diese Informationen eingegeben haben, klicken Sie auf `Anmelden`{.action}. Sind die Angaben korrekt, wird die Verbindung zu Ihrem Account hergestellt.

Sie können eine Test-E-Mail versenden, um zu überprüfen, ob der Account korrekt eingerichtet ist.

![mx plan](images/configuration-mail-windows-step2.png){.thumbnail}

Wenn manuelle Änderungen in den Account-Einstellungen erforderlich sind, verwenden Sie die folgenden technischen Einstellungen für unser MX Plan Angebot:

- **IMAP-Konfiguration**

|Servertyp|Servername|SSL|Port|
|---|---|---|---|
|Eingangsserver|ssl0.ovh.net|Ja|993|
|Ausgangsserver|ssl0.ovh.net|Ja|465|

- **POP-Konfiguration**

|Servertyp|Servername|SSL|Port|
|---|---|---|---|
|Eingangsserver|ssl0.ovh.net|Ja|995|
|Ausgangsserver|ssl0.ovh.net|Ja|465|

### Schritt 2: E-Mail-Account verwenden

Ihr E-Mail-Account ist nun fertig konfiguriert und Sie können Nachrichten versenden und empfangen.

OVHcloud bietet Ihnen außerdem eine Webanwendung, mit der Sie über einen Webbrowser auf Ihren E-Mail-Account zugreifen können. Diese ist über [Webmail](/links/web/email) verfügbar. Sie können sich mit den Login-Daten Ihres E-Mail-Accounts anmelden.
 
## Weiterführende Informationen

> [!primary]
>
> Weitere Informationen zum Konfigurieren einer E-Mail-Adresse über den Mail-Client unter Windows finden Sie im [Microsoft Help Center](https://support.microsoft.com/de-de/office/configure-l-mail-in-l-mail-application-mail-7ff79e8b-439b-4b47-8ff9-3f9a33166c60).

[Konfiguration von E-Mail Pro auf der Windows Mail App](/pages/web_cloud/email_and_collaborative_solutions/email_pro/how_to_configure_windows_10)

[Konfiguration von Exchange auf der Windows Mail App](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/how_to_configure_windows_10)

Treten Sie unserer [User Community](/links/community) bei.
