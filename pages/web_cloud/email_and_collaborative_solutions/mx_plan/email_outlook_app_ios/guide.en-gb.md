---
title: "MX Plan - Configuring your email account in Outlook for iOS"
excerpt: "Find out how to configure your MX Plan email address on the Outlook mobile app for iOS"
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

## Objective

MX Plan accounts can be configured on various compatible email clients. This allows you to use your email address from the device of your choice. The Microsoft Outlook app on iOS is available for free from the Apple App Store.

**Find out how to configure your MX Plan email address on the Outlook mobile app for iOS**

> [!warning]
>
> OVHcloud provides services that you are responsible for configuring, managing and managing. It is therefore up to you to ensure that it works properly.
>
> We have provided you with this guide in order to help you with common tasks. Nevertheless, we recommend contacting a [specialized partner](https://marketplace.ovhcloud.com/c/support-collaboration) and/or the service publisher if you experience any difficulties. We will not be able to assist you. You can find more information in the “Go further” section of this guide.

## Requirements

- an MX Plan email address (included in the MX Plan solution, or in an [OVHcloud Web Hosting] solution (/links/web/hosting)).
- You must have the Outlook application installed on your mobile device [iOS](https://apps.apple.com/app/microsoft-outlook/id951937596).
- You must have the login details for the email address you would like to configure.

## In practice

### Add the <a name="add-account"></a> account

- **When you start the application for the first time**: A configuration wizard will appear. Tap `Add account`{.action}.

![outlook ios](images/outlook-app-ios-add01.png){.thumbnail .w-400 .h-600}

- **If an account has already been set up**:
    1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
    2. Press the gear ‘&#9881;’ in the lower left of your screen.
    3. Then press `Accounts`{.action} in the **Settings** menu.
    4. Press `Add Account`{.action}.
    5. Press `Email account`{.action}.

![outlook ios](images/outlook-app-ios-add02.png){.thumbnail .w-400 .h-600}

Follow the installation steps by clicking on the tabs below:

> [!tabs]
> **Step 1**
>>
>> Enter your email address and press `Add account`{.action}.
>>
>>![outlook ios](images/outlook-app-ios-add-step01.png){.thumbnail .w-400 .h-600}
>>
> **Step 2**
>>
>> You have two options:
>>
>> - If you have “**IMAP**” at the top of the page, go to step 3.
>> - If the account parameter window displays “**Exchange**” at the top, press the `?” button in the top right corner of the **(1)** screen, then choose `Change account provider`{.action} **(2)**. Then select `IMAP`**(3)** and proceed to step 3.
>>
>>![outlook ios](images/outlook-app-ios-add-step02.png){.thumbnail .w-400 .h-600}
>>
> **Step 3**
>>
>> In the next window, tick `Advanced settings`{.action} and enter the following information:
>>
>> - **Email address**
>> - **Full name** : enter your full email address
>> - **Description**
>> - **IMAP Incoming Mail Server**:<br>- **IMAP Hostname**: For the**EUROPE**, type `imap.mail.ovh.net` or `ssl0.ovh.net`. For**AMERICA/ASIA**, type `imap.mail.ovh.ca`<br>- **IMAP Port**: 993<br>- **IMAP Username**: Your full email address<br>- **IMAP Password**: Your email address<br>- **Port Security**: SSL
>> - **SMTP Incoming Mail Server**:<br>- **SMTP Hostname**: For the**EUROPE**, type `smtp.mail.ovh.net` or `ssl0.ovh.net`. For**AMERICA/ASIA**, type `smtp.mail.ovh.ca`<br>- **SMTP Port**: 465<br>- **SMTP Username**: Your full email address<br>- **SMTP Password**: Your email address<br>- **Port Security**: SSL
>>
>> To finalize the configuration, press `Login`{.action}.
>>
>>![outlook ios](images/outlook-app-ios-add-step03-imap-eu.png){.thumbnail .w-400 .h-600}
>>

> [!warning]
>
> If, after following the configuration steps above, you encounter a sending or receiving error, please refer to the topic “[Modify existing settings](#modify-settings)”.

### Use the email address

Once you have configured your email address, you can start using it! You can now send and receive messages.

OVHcloud also offers a web application that can be used to access your email address from a web browser. You can access it here: [Webmail](/links/web/email). You can log in using your email credentials. If you have any questions on how to use it, and which webmail solution is associated with your solution, please refer to our guides:

- [View your account via the OWA interface](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa)
- [Use your email address from the Roundcube webmail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_roundcube)
- [Use Zimbra webmail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_zimbra).

### Modify existing settings <a name="modify-settings"></a>

1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
2. Press the gear ‘&#9881;’ in the lower left of your screen.
3. Then press `Accounts`{.action} in the **Settings** menu.
4. Select the account.
5. Press `Modify login information`{.action}.

![outlook ios](images/outlook-app-ios-modify-account-01.png){.thumbnail .w-400 .h-600}

Find the settings in **Step 3** of the [Add account](#add-account) chapter.

### Delete an email account <a name="delete"></a>

1. Tap the circle containing the initials of the email account you are viewing, or the home icon "&#8962;" at the top left of your screen.
2. Press the gear ‘&#9881;’ in the lower left of your screen.
3. Then press `Accounts`{.action} in the **Settings** menu.
4. Select the account.
5. Press `Delete Account`{.action}.

![outlook ios](images/outlook-app-ios-modify-delete-01.png){.thumbnail .w-400 .h-600}

### Reminder of POP, IMAP and SMTP settings <a name="popimap-settings"></a>

### IMAP and POP Receive Settings

When you choose your account type, we recommend using **IMAP** to receive emails. However, you can select **POP**.

> [!warning]
>
> Please note down the value that corresponds to your location (**EUROPE** or **AMERICA/ASIA-PACIFIC**)

Follow the installation steps by clicking on the tabs below:

> [!tabs]
> **IMAP configuration**
>>
>> - **Username**: Enter the full **email address**
>> - **Password**: Enter the password for the email address
>> - **EUROPE Server (incoming)**: imap.mail.ovh.net **ou** ssl0.ovh.net
>> - **AMERICA/ASIA-PACIFIC server (incoming)**: imap.mail.ovh.ca
>> - **Port**: 993
>> - **Security type**: SSL/TLS
>>
> **POP configuration**
>>
>> - **Username**: Enter the full **email address**
>> - **Password**: Enter the password for the email address
>> - **EUROPE server (incoming)**: pop.mail.ovh.net **or** ssl0.ovh.net
>> - **AMERICA/ASIA-PACIFIC server (incoming)**: pop.mail.ovh.ca
>> - **Port**: 995
>> - **Security type**: SSL/TLS

#### SMTP Send Settings

For sending emails, if you have to enter the **SMTP** settings manually in your account preferences, you will find the settings below:

**SMTP configuration**

- **Username**: Enter the **full** email address
- **Password**: Enter the password for the email address
- **EUROPE server (incoming)**: pop.mail.ovh.net **ou** ssl0.ovh.net
- **AMERICA/ASIA-PACIFIC server (incoming)**: pop.mail.ovh.ca
- **Port**: 465
- **Security type**: SSL/TLS

> [!primary]
>
> **Change your configuration**
>
> If your email address is configured in **IMAP** and you want to change this configuration to **POP**, you will need to delete the account, then recreate it in **POP**. Refer to the “[Modify existing settings](#modify-settings)” chapter of this guide.

## Go further

For specialized services (SEO, development, etc.), contact the [OVHcloud partners](/links/partner).

If you would like assistance with using and configuring your OVHcloud solutions, we recommend referring to our range of [support solutions](/links/support).

Join our [community of users](/links/community).