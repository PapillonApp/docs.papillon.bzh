# 👋 Démarrage rapide

## À savoir

Papillon est développé en [**React Native**](https://reactnative.dev/docs/getting-started). C'est un framework JavaScript (c'est-à-dire que vous développerez avec du code JavaScript). Il vous faut donc un minimum de connaissances dans ce langage de programmation.

### Quelques particularités

* Papillon utilise TypeScript, c'est-à-dire que les objets JavaScript présents dans le code doivent être **typés**. Si votre IDE est configuré correctement, il vous en notifiera.
* Papillon utilise Expo mais pas **Expo Go**. Un processus de build sera nécessaire pour voir vos changements sur l'app en temps réel (cela sera expliqué plus tard).

## Pré-requis

Commençons par préparer votre ordinateur pour contribuer à Papillon ! Pour cela, il faut un certain nombre d'outils.

{% hint style="warning" %}
**macOS est nécessaire pour développer Papillon sous iOS**. Si vous n'avez pas de Mac ou d'appareil éxecutant macOS, vous serez limité au développement Android.
{% endhint %}

{% tabs %}
{% tab title="Sur macOS" %}
{% hint style="success" %}
Les commandes d'installation seront indiquées ici. **En les éxecutant dans l'ordre**, votre Mac sera prêt pour le développement de Papillon.
{% endhint %}

#### Homebrew

Pour rendre l'installation plus facile, il est conseillé d'installer [Homebrew](https://brew.sh/), un gestionnaire de logiciels en ligne de commande.

Vous pouvez l'installer avec la commande suivante :

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

{% hint style="info" %}
Les commandes `brew` nécessitent cette étape. Il est fortement recommandé d'installer Homebrew pour la suite de ce tutoriel.
{% endhint %}

#### NodeJS

[Node](https://nodejs.org/fr) est un environnement JavaScript conçu pour exécuter localement du code JavaScript, en dehors d'un navigateur. C'est ce qu'utilise Papillon (via React Native) pour fonctionner.

```shellscript
brew install node@22
```

#### Git

[Git](https://git-scm.com/) est un outil qui vous sera nécessaire pour télécharger le code de Papillon, le tenir à jour, et publier des modifications.

```shellscript
brew install git
```

#### Watchman

[Watchman](https://facebook.github.io/watchman/) est un outil qui vous permettra de voir les mises à jour de votre code en temps réel, sans avoir à redémarrer l'application.

```shellscript
brew install watchman
```
{% endtab %}

{% tab title="Sur Windows" %}
{% hint style="success" %}
Les commandes d'installation seront indiquées ici. **En les éxecutant dans l'ordre**, votre Mac sera prêt pour le développement de Papillon.
{% endhint %}

{% hint style="warning" %}
Pour l'ensemble des commandes présentées, merci d'utiliser le PowerShell en tant qu'administrateur **(Menu Démarrer > "PowerShell" > Éxécuter en tant qu'administateur)**
{% endhint %}

#### Chocolatey

[Chocolatey](https://chocolatey.org/) est un gestionnaire de logiciels pour Windows. Pour rendre l'installation des pré-requis plus facile, il est recommandé de l'installer.

{% hint style="info" %}
Les commandes `choco` nécessitent cette étape. Il est fortement recommandé d'installer Chocolatey pour la suite de ce tutoriel.
{% endhint %}

```powershell
powershell -c "irm https://community.chocolatey.org/install.ps1|iex"
```

> Si la commande ne fonctionne pas, référez-vous au tutoriel officiel : [https://chocolatey.org/install#individual](https://chocolatey.org/install#individual)

#### NodeJS

[Node](https://nodejs.org/fr) est un environnement JavaScript conçu pour exécuter localement du code JavaScript, en dehors d'un navigateur. C'est ce qu'utilise Papillon (via React Native) pour fonctionner.

```shellscript
choco install nodejs --version="22.22.0"
```

#### Git

[Git](https://git-scm.com/) est un outil qui vous sera nécessaire pour télécharger le code de Papillon, le tenir à jour, et publier des modifications.

```shellscript
choco install git
```

#### Watchman

[Watchman](https://facebook.github.io/watchman/) est un outil qui vous permettra de voir les mises à jour de votre code en temps réel, sans avoir à redémarrer l'application.

```shellscript
choco install watchman
```
{% endtab %}
{% endtabs %}

## Environnement de développement

Une fois que tout est installé, il faut mettre en place votre environnement de développement.

{% tabs %}
{% tab title="iOS (macOS)" %}
{% hint style="danger" %}
**macOS est nécessaire pour développer Papillon sous iOS**. Si vous n'avez pas de Mac ou d'appareil éxecutant macOS, vous serez limité au développement Android.
{% endhint %}

#### Cocoapods

Cocoapods est le gestionnaire de dépendance pour les applications iOS, il est nécessaire au build de l'application.

{% hint style="info" %}
Il n'est pas nécessaire pour développer sur Android, mais il reste conseillé de l'installer.
{% endhint %}

```shellscript
sudo gem install cocoapods
```

#### Xcode

[Xcode](https://developer.apple.com/xcode/) est le logiciel d'Apple permettant le développement sous macOS. Il est téléchargeable via l'App Store.

Une fois Xcode installé, il faudra installer les outils en ligne de commande :&#x20;

```shellscript
xcode-select --install 
```
{% endtab %}

{% tab title="Android (Windows ou macOS)" %}
#### Android Studio

[Android Studio](https://developer.android.com/studio?hl=fr) est le logiciel de développement officiel pour Android. Celui-ci est recommandé pour développer sous Android.

Téléchargez-le [depuis le site officiel](https://developer.android.com/studio?hl=fr) et procédez à l'installation.
{% endtab %}
{% endtabs %}

## Clonage

Une fois que vous avez créé un fork de Papillon, vous allez pouvoir le télécharger localement afin d'y apporter des modifications via votre éditeur de code, pour cloner le fork, vous allez devoir utiliser l'outil Git :

Pour cela, ouvrez un terminal dans le dossier de votre choix et exécutez la commande suivante :

```bash
git clone https://github.com/PapillonApp/Papillon.git
```

## Préparation au développement

Pour développer plus facilement, il est recommandé d'utiliser un éditeur de code tel que [Visual Studio Code](https://code.visualstudio.com/), [Zed](https://zed.dev/) ou [WebStorm](https://www.jetbrains.com/fr-fr/webstorm/).

Ouvrez le projet `papillon` dans l'éditeur en question et exécutez les commandes d'initialisation suivantes :&#x20;

```bash
npm install
```

#### Pré-build

Pour démarrer l'application, il faut la pré-builder. C'est-à-dire compiler une version spécifique utile au développement.

{% hint style="info" %}
Il faut procéder à cette étape à **CHAQUE ajout ou mise à jour de modules npm demandant du code natif**. Sinon, l'app peut crash ou se comporter incorrectement.
{% endhint %}

Pour cela, éxecutez la commande suivante **à chaque fois que vous installez des nouvelles dépendances**.

```shellscript
npx expo prebuild
```

Si vous développez pour iOS, il faut également mettre à jour les Cocoapods

```bash
cd ios && pods install && cd ..
```

## Commencez à développer !

Pour démarrer l'app, exécutez la commande correspondante :&#x20;

{% hint style="danger" %}
Cette commande peut prendre **5 à 10 minutes** lorsqu'elle est exécutée à froid (c'est à dire pour la première fois). C'est **normal**, c'est un processus lourd et énergivore.
{% endhint %}

{% tabs %}
{% tab title="iOS (macOS)" %}
```shellscript
npx expo run ios
```
{% endtab %}

{% tab title="Android (macOS et Windows)" %}
```shellscript
npx expo run android
```
{% endtab %}
{% endtabs %}

## Problèmes fréquents

<details>

<summary><span data-gb-custom-inline data-tag="emoji" data-code="26a0">⚠️</span> L'application crash sans raison ou le build ou le pré-build ne fonctionne pas</summary>

Si l'erreur n'affiche pas de raison claire, tentez de réinitialiser la partie native de votre projet :&#x20;

{% code title="(sous macOS)" %}
```shellscript
rm -rf node_modules
npm i
npx expo prebuild
cd ios
pod install
cd ..
```
{% endcode %}

</details>

## Effectuer sa première Pull Request <a href="#effectuer-sa-premiere-pull-request" id="effectuer-sa-premiere-pull-request"></a>

Une fois que tu as fait les modifications que tu voulais, tu peux créer une nouvelle branche à l'aide de la commande `git checkout -b feature/super-cool`, chez Papillon, nous respectons la spécification [Conventional Branch](https://conventional-branch.github.io/) afin de se repérer dans nos branches.

Ensuite, il te suffit d'ajouter tous les fichiers que tu souhaites pousser avec la commande `git add [fichier]` puis d'effectuer un commit avec `git commit -m [titre de ton commit] -m [description]`, il n'est pas obligatoire de mettre une description, mais tu dois respecter la spécification [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

Une fois que tout ça est fait, tu peux enfin pousser les modifications vers ton fork à l'aide de la commande `git push origin [nom de ta branche`, et tu peux ensuite, en allant dans l'onglet **Pull Requests** du dépôt GitHub de Papillon, ouvrir ta **Pull Request**.

## Et ensuite ? <a href="#et-ensuite" id="et-ensuite"></a>

Elle sera analysée en premier temps par un robot qui s'assurera de sa conformité avec les règles de contributions, si elle n'est pas conforme, elle obtiendra le label Invalide le temps que tu corriges ce qui ne va pas, ne t'inquiète pas, tout est expliqué par le robot sous ta Pull Request.

Après cette première analyse, nous analyserons manuellement ta Pull Request, nous pouvons à ce stade, soit valider, soit demander des changements, une fois que tout sera bon, elle sera fusionnée avec le code principal !
