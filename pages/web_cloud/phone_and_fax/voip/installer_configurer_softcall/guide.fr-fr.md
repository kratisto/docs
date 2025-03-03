---
title: 'Installer et configurer Softcall (Bêta)'
excerpt: 'Découvrez comment installer et configurer Softcall afin de profiter de la solution Softphone'
updated: 2025-03-04
---

> [!primary]
> L'application [Softcall](https://labs.ovhcloud.com/en/softphone-beta/) est disponible en phase bêta.
>
> Ce guide est susceptible d'être incomplet et sera mis à jour durant la phase bêta. Notre équipe reste disponible pour répondre à vos questions sur la mailing-list [voip@ml.ovh.net](mailto:voip@ml.ovh.net). Posez des questions, donnez votre avis et interagissez directement avec l’équipe qui construit nos services VoIP.
>
> **[Inscrivez-vous à la bêta dès maintenant !](https://survey.ovh.com/index.php/361586?lang=fr)**
> 

## Objectif

Le Softphone est une solution qui transforme votre ordinateur, smartphone ou tablette en un téléphone virtuel, vous permettant d'utiliser votre ligne SIP (**S**ession **I**nitiation **P**rotocol) n'importe où et à tout moment. Grâce à notre application [Softcall](https://labs.ovhcloud.com/en/softphone-beta/), facilement téléchargeable sur les plateformes Android, iOS, macOS et Windows, vous pouvez accéder à toutes les fonctionnalités de votre ligne téléphonique professionnelle sans être attaché à un téléphone de bureau traditionnel. Que vous soyez en déplacement ou que vous travailliez à distance, Softcall garantit que votre ligne SIP reste aussi mobile et flexible que nécessaire.

**Découvrez comment installer et configurer Softcall sur les plateformes Android, iOS, macOS et Windows.**

## Prérequis

- Disposer d'une [ligne SIP OVHcloud](/links/telecom/telephonie-voip).
- Être connecté à l'[espace client OVHcloud](/links/manager), partie `Télécom`{.action}.
- Rejoindre la [bêta Softcall](https://survey.ovh.com/index.php/361586?lang=fr).
- Une fois Softcall activé, le téléphone OVH lié à la ligne ne pourra plus être utilisé.
- Si votre connexion utilise un pare-feu, vous devez autoriser les adresses IP suivantes : `57.128.38.204/32` et `57.128.38.156/32`.

> [!primary]
> Si Softcall est désactivé et que vous souhaitez réutiliser votre téléphone OVH, vous devez procéder à un dépannage Plug & Phone. Pour les autres types d'appareils, il est nécessaire de réinitialiser le mot de passe SIP et de le renseigner dans la configuration de l'appareil. Pour plus de détails, consultez notre guide « [Dépanner son téléphone OVHcloud](web_cloud/phone_and_fax/voip/troubleshoot-02-fix-control-panel) ».

## En pratique

### Installer Softcall

1. Connectez-vous à votre [espace client OVHcloud](/links/manager) et cliquez sur `Télécom`{.action}.
2. Cliquez sur `Téléphonie`{.action} puis sur le groupe de facturation contenant votre ligne SIP.
3. Cliquez sur la ligne SIP concernée.
4. Après avoir sélectionné l'onglet `Softphone`{.action}, cliquez sur l'interrupteur pour générer un e-mail dans lequel se trouve le logiciel Softcall, disponible pour Windows, macOS, Android et iOS.

![Install Softcall](images/send_mail_manager.png){.thumbnail}

Ouvrez l'e-mail et suivez les instructions pour installer Softcall.

### Configurer Softcall

Cliquez sur l'icône de l'application Softcall. Au premier démarrage, vous êtes dirigé vers l'écran `Assistant`{.action}.

#### Application mobile (Android et IOS)

*Cliquez sur l'onglet correspondant à votre système d'exploitation mobile :*

> [!tabs]
> **Android**
>>
>> ![Install Softcall](images/assistant_ios_android.png){.thumbnail}
>>
> **iOS**
>>
>> ![Install Softcall](images/assistant_ios_android.png){.thumbnail}
>>

Récupérez le code ou le QR CODE pour télécharger votre configuration Softcall. Retrouvez le code et le QR CODE de configuration dans l'e-mail que vous avez reçu après avoir souscrit à l'offre Softcall.

Dans l'écran `Assistant`{.action} de l'application Softcall, entrez le code de configuration ou appuyez sur le bouton QR CODE pour scanner le QR CODE. Cliquez sur `Télécharger et appliquer`{.action} pour valider.

Votre compte Softcall est désormais configuré. Dans le menu principal de Softcall, retrouvez votre numéro de téléphone (au format international) tout en haut du menu.

#### Application de bureau (Windows et MacOS)

*Cliquez sur l'onglet correspondant à votre système d'exploitation :*

> [!tabs]
> **Windows**
>>
>> ![Install Softcall](images/assistant_windows_macos.png){.thumbnail}
>>
> **macOS**
>>
>> ![Install Softcall](images/assistant_windows_macos.png){.thumbnail}
>>

Récupérez le code de configuration (ou token de provisioning) vous permettant de télécharger votre configuration Softcall. Retrouvez le code dans l'e-mail que vous avez reçu après avoir souscrit à l'offre Softcall.

Dans l'écran `Assistant`{.action} de l'application Softcall, entrez le code de configuration puis cliquez sur `Télécharger`{.action}. Un message de confirmation s'affiche.

![Install Softcall](images/confirm_dl_config_windows.png){.thumbnail}

Cliquez sur `Confirmer`{.action} pour redémarrer l'application Softcall afin de prendre en compte la configuration de votre compte Softcall.

Votre compte Softcall est désormais configuré. Dans le menu principal de Softcall, retrouvez votre numéro de téléphone (au format international) tout en haut de l'interface.

### Fonctionnalités de base

#### Passer un appel téléphonique

##### Application mobile (Android et IOS)

Dans le menu principal en bas de l'écran, cliquez sur l'icône représentant un clavier numérique.

> [!tabs]
> **Android**
>>
>> ![Install Softcall](images/bottom_menu_android.jpg){.thumbnail}
>>
> **iOS**
>>
>> ![Install Softcall](images/bottom_menu_ios.png){.thumbnail}
>>

Entrez le numéro de votre contact et cliquez sur l'icône représentant un téléphone pour passer l'appel.

##### Application de bureau (Windows et macOS)

Pour passer un appel téléphonique, entrez le numéro dans le champ en haut de l'interface, ou cliquez sur l'icône représentant un clavier numérique pour taper le numéro. Cliquez sur l'icône représentant un téléphone pour passer l'appel.

![Install Softcall](images/call_number.png){.thumbnail}

Dans le menu principal à gauche de l'interface, cliquez sur l'icône représentant un téléphone pour accéder à votre historique d'appels.

#### Gérer les contacts

Dans le menu principal à gauche de l'interface, cliquez sur l'icône des contacts. Sur l'écran qui s'affiche, vous pouvez :

- Accéder à vos contacts
- Rechercher un contact
- Ajouter des nouveaux contacts
- Modifier et supprimer des contacts

#### Supprimer le compte Softcall sur l'appareil

> [!primary]
> Cette fonctionnalité permet de supprimer votre compte Softcall uniquement sur votre appareil. Votre compte Softcall sera supprimé uniquement en local, et vous pourrez à nouveau le configurer sur votre appareil quand vous le souhaiterez. 
>

Effectuez les actions suivantes pour supprimer votre compte Softcall de votre appareil :

- Dans le menu principal, cliquez sur `Options`{.action}.
- Cliquez sur le numéro du compte Softcall que vous voulez supprimer.
- Cliquez sur `Supprimer le compte`{.action}.
- Un message de confirmation s'affiche : cliquez sur `Supprimer`{.action} pour confirmer la suppression locale de votre compte Softcall.

### Fonctionnalités avancées

#### Application de bureau (Windows et macOS)

##### Effectuer un transfert d'appel à l'aveugle

Lorsque vous transférez un appel téléphonique à l'aveugle, cela signifie que : 

- Le transfert est effectué directement, sans préalablement contacter le nouveau destinataire.
- Votre correspondant en cours n'est pas mis en attente lors du transfert. 

Pour effectuer un transfert d'appel à l'aveugle, suivez ces étapes :

- En haut à gauche de l'interface, cliquez sur l'icône représentant un téléphone.

![Install Softcall](images/call_in_progress_main_interface.png){.thumbnail}

- Juste à droite du numéro de votre correspondant en cours, cliquez sur les trois points (`⋮`{.action}). Dans le menu qui s'affiche, choisissez `Transférer l'appel`{.action}.

![Install Softcall](images/call_in_progress_menu_blind_transfer.png){.thumbnail}

- Sur l'écran qui s'affiche, tapez le numéro du destinataire vers qui vous souhaitez transférer l'appel. Cliquez sur le bouton à droite du numéro (représentant une flèche) pour transférer l'appel.

![Install Softcall](images/blind_call_transfer_form.png){.thumbnail}

- Lorsque le destinataire du transfert décroche, l'appel avec votre correspondant en cours se termine.

![Install Softcall](images/end_of_call.png){.thumbnail}


##### Effectuer un transfert d'appel accompagné

Lorsque vous transférez un appel téléphonique accompagné, cela signifie que : 

- Vous contactez le nouveau destinataire pour obtenir son accord avant de valider le transfert.
- Votre correspondant est mis en attente avant d'effectuer le transfert. 

Pour transférer un appel téléphonique accompagné, suivez ces étapes :

- En haut à gauche de l'interface, cliquez sur l'icône représentant un téléphone.

![Install Softcall](images/call_in_progress_main_interface.png){.thumbnail}

- Juste à droite du numéro de votre correspondant en cours, cliquez sur les trois points (`⋮`{.action}). Dans le menu qui s'affiche, choisissez `Consultation avant transfert`{.action}.

![Install Softcall](images/call_in_progress_menu_attended_transfer.png){.thumbnail}

- Sur l'écran qui s'affiche, tapez le numéro du destinataire vers qui vous souhaitez transférer l'appel. Cliquez sur le bouton à droite du numéro (représentant une flèche) pour l'appeler.

![Install Softcall](images/blind_call_transfer_form.png){.thumbnail}

- Votre correspondant en cours est mis en attente. Lorsque le destinataire du transfert décroche, cliquez sur l'icône représentant un téléphone, en haut à gauche de l'interface. Dans le menu latéral de gauche, les numéros de vos correspondants en attente et en cours s'affichent. Cliquez sur les trois points (`⋮`{.action}) à droite du numéro de votre correspondant en cours, puis choisissez `Valider le transfert`{.action}.

![Install Softcall](images/validate_transfer.png){.thumbnail}

- Une fois le transfert validé, les appels avec vos deux correspondants sont terminés.

![Install Softcall](images/end_of_call.png){.thumbnail}

##### Appeler sa messagerie vocale

Pour appeler votre messagerie vocale, cliquez sur l'icône suivante, en haut à droite de l'interface de Softcall.

![Install Softcall](images/voicemail_button.png){.thumbnail}

##### Utiliser le mode bis

Dans le menu latéral de l'interface de Softcall, cliquez sur l'icône représentant un téléphone.

![Install Softcall](images/call_history_button.png){.thumbnail}

En haut à droite de l'écran, cliquez sur le bouton représentant un téléphone pour appeler le dernier numéro avec lequel vous avez été en contact.

![Install Softcall](images/bis_number.png){.thumbnail}

##### Rapporter un incident à Softcall

Si vous rencontrez un problème avec l'application Softcall (bugs, erreurs, etc.), envoyez un rapport à Softcall en suivant les étapes suivantes :

- En bas à gauche de l'interface de Softcall, cliquez sur l'icône des paramètres (représentée par une roue crantée), puis sur `Préférences`{.action}.
- Sur l'écran qui s'affiche, rendez-vous dans l'onglet `Avancés`{.action}.
- Cliquez sur le bouton `Envoyer les traces`{.action}.
- Un client de messagerie s'ouvre automatiquement avec le destinataire et le lien du rapport de bug pré-remplis.
- Envoyez l'e-mail pour transmettre les traces au support technique de Softcall.

#### Application mobile (Android et IOS)

##### Effectuer un transfert d'appel à l'aveugle

Lorsque vous transférez un appel téléphonique à l'aveugle, cela veut dire que : 

- Le transfert est effectué de manière directe, sans préalablement contacter le nouveau destinataire.
- Votre correspondant en cours n'est pas mis en attente lors du transfert. 

Pour effectuer un transfert d'appel à l'aveugle, suivez ces étapes :

- Lorsque vous êtes en ligne avec votre correspondant, cliquez en bas à droite de l'interface sur les trois points (`...`{.action}).

![Install Softcall](images/mobile_call_in_progress_interface.jpg){.thumbnail}

- Dans le menu qui s'ouvre, cliquez sur `Transférer l'appel`{.action}.

![Install Softcall](images/mobile_transfer_call.jpg){.thumbnail}

- Sur l'écran qui s'affiche, tapez le numéro du destinataire vers qui vous souhaitez transférer l'appel. Cliquez sur le bouton en bas à droite de l'écran (représentant un téléphone) pour transférer l'appel.

![Install Softcall](images/mobile_keyboard_transfer.jpg){.thumbnail}

- Lorsque le destinataire du transfert décroche, l'appel avec votre correspondant en cours se termine.

##### Effectuer un transfert d'appel accompagné

Lorsque vous transférez un appel téléphonique accompagné, cela signifie que : 

- Vous appelez le nouveau destinataire pour lui demander son accord avant la validation du transfert.
- Votre correspondant est mis en attente avant d'effectuer le transfert. 

Pour transférer un appel téléphonique accompagné, suivez ces étapes :

- Lorsque vous êtes en ligne avec votre correspondant, cliquez en bas à droite de l'interface sur les trois points (`...`{.action}).

![Install Softcall](images/mobile_call_in_progress_interface.jpg){.thumbnail}

- Dans le menu qui s'affiche, cliquez sur `Nouvel appel`{.action}.

![Install Softcall](images/mobile_call_in_progress_menu_new_call.jpg){.thumbnail}

- Sur l'écran qui s'affiche, tapez le numéro du destinataire vers qui vous souhaitez transférer l'appel. Cliquez sur le bouton en bas à droite de l'interface (représentant un téléphone) pour l'appeler.

![Install Softcall](images/mobile_keyboard_transfer.jpg){.thumbnail}

- Votre correspondant en cours est mis en attente. Lorsque le destinataire du transfert décroche, cliquez sur les trois points (`...`{.action}) en bas à droite de l'interface. Dans le menu qui s'affiche, cliquez sur `Transfert supervisé`{.action} pour effectuer le transfert.

![Install Softcalls](images/mobile_call_in_progress_attended_transfer.jpg){.thumbnail}

- Une fois le transfert validé, les appels avec vos deux correspondants sont terminés.

##### Appeler sa messagerie vocale

Pour appeler votre messagerie vocale, cliquez sur l'icône suivante, en haut à droite de l'interface de Softcall.

![Install Softcall](images/mobile_voicemail.jpg){.thumbnail}

##### Utiliser le mode bis

Pour appeler le dernier numéro avec lequel vous avez été en contact, suivez les étapes suivantes :

- Cliquez sur l'icône suivante (en bas à droite de l'interface) pour afficher le clavier numérique :

![Install Softcall](images/bottom_menu_android.jpg){.thumbnail}

- Cliquez sur le bouton représentant un téléphone :

![Install Softcall](images/mobile_button_call.jpg){.thumbnail}

- Le dernier numéro appelé s'affiche. Appuyez à nouveau sur le même bouton pour l'appeler.

##### Rapporter un incident à Softcall

Si vous rencontrez un problème dans l'application Softcall (bugs, erreurs, etc.), envoyez un rapport à Softcall en suivant les étapes suivantes :

- Composez le numéro `#1234#`.
- Dans le menu qui s'affiche, cliquez sur `Activer les traces`{.action}.

![Install Softcall](images/mobile_enable_debugging.jpg){.thumbnail}

- Reproduisez les actions qui provoquent l'anomalie.
- Composez à nouveau le numéro `#1234#`.
- Dans le menu qui s'affiche, cliquez sur `Envoyer les traces`{.action}.

![Install Softcall](images/mobile_submit_logs.jpg){.thumbnail}

- Sur l'écran qui s'affiche, choisissez votre client de messagerie. Le destinataire et le lien du rapport de bug sont pré-remplis dans le mail.
- Envoyez le mail pour transmettre les traces au support technique de Softcall.

## Aller plus loin

Échangez avec notre [communauté d'utilisateurs](/links/community).