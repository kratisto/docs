---
title: "Email Pro - Configuring your email account in Outlook for iOS"
excerpt: "Find out how to configure your Email Pro address on the Outlook for iOS mobile application"
updated: 2025-02-13
---

<style>
.w-400 {
max-width:400px !important;
}
.h-600 {
max-height:600px !important;
}
</style>

## Objective

You can configure Email Pro accounts on email clients, if they are compatible. This allows you to use your email address from the device of your choice. The Microsoft Outlook app on iOS is available for free from the Apple App Store.

**Find out how to configure your Email Pro address on the Outlook mobile application for iOS**

> [!warning]
> OVHcloud is providing you with services for which you are responsible, with regard to their configuration and management. You are therefore responsible for ensuring they function correctly.
>
> This guide is designed to assist you in common tasks as much as possible. Nevertheless, we recommend contacting a specialised provider and/or the software publisher for the service if you encounter any difficulties. We will not be able to assist you ourselves. You can find more information in the [Go further](#gofurther) section of this guide.

## Requirements

- an [Email Pro address](/links/web/email-pro).
- You must have the Outlook application installed on your mobile device [iOS](https://apps.apple.com/app/microsoft-outlook/id951937596).
- You must have the login details for the email address you would like to configure.

## Instructions

### Add the account <a name="add-account"></a>

> [!warning]
>
> In our examples, we use the server comment: pro**?**.mail.ovh.net. You will need to replace the "?" with the number designating the server of your Email Pro service.
>
> Find this number in your [OVHcloud Control Panel](/links/manager), in the `Web Cloud`{.action} section, then `Email Pro`{.action}. The server name is visible in the **Connection** box in the `General information`{.action} tab.
>

- **When you start the application for the first time**: A configuration wizard will appear. Tap `Add account`{.action}.

![outlook iOS](images/outlook-app-ios-add01.png){.thumbnail .w-400 .h-600}

- **If an account has already been set up**:
    1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
    2. Press the gear "&#9881;" in the lower left of your screen.
    3. Then press `Accounts`{.action} in the **Settings** menu.
    4. Press `Add Account`{.action}.
    5. Press `Email account`{.action}.

![outlook iOS](images/outlook-app-ios-add02.png){.thumbnail .w-400 .h-600}

Follow the installation steps by clicking on the tabs below:

> [!tabs]
> **Step 1**
>>
>> Enter your email address and press `Add account`{.action}.
>>
>> ![outlook iOS](images/outlook-app-ios-add-step01.png){.thumbnail .w-400 .h-600}
>>
> **Step 2**
>>
>> You have two options:
>>
>> - If you have "**IMAP**" at the top of the page, go to step 3.
>> - If the account parameter window displays "**Exchange**" at the top, press the `?` button in the top right corner of the **(1)** screen, then choose `Change account provider`{.action} **(2)**. Then select `IMAP` **(3)** and proceed to step 3.
>>
>> ![outlook iOS](images/outlook-app-ios-add-step02.png){.thumbnail .w-400 .h-600}
>>
> **Step 3**
>>
>> In the next window, tick `Advanced settings`{.action} and enter the following information:
>>
>> - **Email address**
>> - **Full name** : enter your full email address
>> - **Description**
>> - **IMAP Incoming Mail Server**:<br>- **IMAP Hostname**: Type `pro**?**.mail.ovh.net` (replace "**?**" with your server number)<br>- **IMAP Port**: 993<br>- **IMAP Username**: Your full email address<br>- **IMAP Password**: Your email address password<br>- **Port Security**: SSL
>> - **SMTP Incoming Mail Server**:<br>- **SMTP Hostname**: Type `pro**?**.mail.ovh.net` (replace "**?**" with your server number)<br>- **SMTP Port**: 587<br>- **SMTP Username**: Your full email address<br>- **SMTP password**: Your email address password<br>- **Port security**: STARTTLS command failures
>>
>> To finalize the configuration, press `Login`{.action}.
>>
>> ![outlook iOS](images/outlook-app-ios-add-step03-imap-emailpro.png){.thumbnail .w-400 .h-600}
>>

> [!warning]
>
> If, after following the configuration steps above, you encounter a sending or receiving error, please refer to the topic "[Modify existing settings](#modify-settings)".

### Use the email address

Once you have configured your email address, you can start using it! You can now send and receive messages.

OVHcloud also offers a web application that can be used to access your email address from a web browser. You can access it here: [Webmail](/links/web/email). You can log in using your email credentials. If you have any questions on how to use it, please refer to our guide [View your account via the OWA interface](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa).

### Modify existing settings <a name="modify-settings"></a>

1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
2. Press the gear "&#9881;" in the lower left of your screen.
3. Then press `Accounts`{.action} in the **Settings** menu.
4. Select the account.
5. Press `Modify login information`{.action}.

![outlook iOS](images/outlook-app-ios-modify-account-01.png){.thumbnail .w-400 .h-600}

Find the settings in **Step 3** of the [Add account](#add-account) chapter.

### Delete an email account <a name="delete"></a>

1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
2. Press the gear "&#9881;" in the lower left of your screen.
3. Then press `Accounts`{.action} in the **Settings** menu.
4. Select the account.
5. Press `Delete Account`{.action}.

![outlook iOS](images/outlook-app-ios-modify-delete-01.png){.thumbnail .w-400 .h-600}

### Reminder of POP, IMAP and SMTP settings <a name="popimap-settings"></a>

### IMAP and POP Receive Settings

When you choose your account type, we recommend using **IMAP** to receive emails. However, you can select **POP**.

Click on the tab corresponding to your receive protocol:

> [!tabs]
> **IMAP configuration**
>>
>> - **Username**: Enter the full **email address**
>> - **Password**: Enter the password for the email address
>> - **Server (incoming)**: pro**?**.mail.ovh.net
>> - **Port**: 993
>> - **Security type**: SSL/TLS
>>
> **POP configuration**
>>
>> - **Username**: Enter the full **email address**
>> - **Password**: Enter the password for the email address
>> - **Server (incoming)**: pro**?**.mail.ovh.net
>> - **Port**: 995
>> - **Security type**: SSL/TLS

#### SMTP Send Settings

For sending emails, if you have to enter the **SMTP** settings manually in your account preferences, you will find the settings below:

**SMTP configuration**

- **Username**: Enter the **full** email address
- **Password**: Enter the password for the email address
- **Server (incoming)**: pro**?**.mail.ovh.net
- **Port**: 587
- **Security type**: SSL/TLS

## Go further <a name="gofurther"></a>

> [!primary]
>
> For more information about setting up an email address from the Outlook app on iOS, see [the Microsoft Help Center](https://support.microsoft.com/office/set-up-the-outlook-app-for-ios-b2de2161-cc1d-49ef-9ef9-81acd1c8e234).

For specialised services (SEO, development, etc.), contact [OVHcloud partners](/links/partner).

If you would like assistance using and configuring your OVHcloud solutions, please refer to our [support offers](/links/support).

Join our [community of users](/links/community).