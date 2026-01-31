---
icon: apple
---

# Compiler pour iOS

{% hint style="danger" %}
Pour compiler Papillon pour iOS, vous devez être sous MacOS et avoir installé Xcode.

**Xcode 26 est nécessaire pour compiler Papillon v8 et ultérieur.**
{% endhint %}

{% stepper %}
{% step %}
### Prébuild du projet

Dans la racine du projet, éxecutez l'une de ces commandes :

{% tabs %}
{% tab title="npm" %}
```sh
npm prebuild
```
{% endtab %}

{% tab title="pnpm" %}
```sh
pnpm prebuild
```
{% endtab %}

{% tab title="yarn" %}
```sh
yarn prebuild
```
{% endtab %}

{% tab title="bun" %}
```sh
bun prebuild
```
{% endtab %}
{% endtabs %}
{% endstep %}

{% step %}
### Ouverture d'Xcode

Ouvrir `Papillon.xcworkspace` avec xCode (**TRÈS IMPORTANT**)

> Il se trouve dans le dossier `/ios` du projet&#x20;
{% endstep %}

{% step %}
### Configuration de Signing (optionnel)

{% hint style="info" %}
Cette étape n'est utile que si vous souhaitez lancer Papillon sur un appareil physique ou créer une build pour distribuer l'app
{% endhint %}

Double-cliquez sur Papillon dans le menu de gauche du projet puis allez dans **Signing & Capabilities**

Ajoutez ici votre compte Apple Developer pour pouvoir signer vos builds.

Si vous n'avez pas de compte payant Apple Developer: changer les teams pour le signing et enlever les "Assiocated Domains"
{% endstep %}

{% step %}
### Selection du scheme et de la target

#### Pour développer

Sélectionner `Papillon (debug)`au niveau des schemes et votre target (physique ou simulateur)

#### Pour distribuer ou tester en production

Sélectionner `Papillon (release)`au niveau des schemes et votre target (physique ou simulateur)
{% endstep %}

{% step %}
### Builder

{% tabs %}
{% tab title="Pour développer (debug)" %}
Appuyez sur l'icône <i class="fa-play">:play:</i> Debug pour démarrer l'appli sur l'appareil ou le simulateur sélectionné. Cela va compiler l'app puis la démarrer.

**Il faut un serveur de développement Expo ouvert sur votre machine pour que l'app se lance par la suite.**
{% endtab %}

{% tab title="Pour distribuer (release)" %}
Sélectionnez **Any iOS device** comme appareil de target

Ouvrez le menu **`Product > Archive`** pour démarrer la compilation.

> Par la suite, **l'Organizer** s'ouvre pour permettre de distribuer l'app ou de l'empaqueter au format `*.ipa`
{% endtab %}
{% endtabs %}
{% endstep %}
{% endstepper %}
