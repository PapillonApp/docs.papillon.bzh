# 📦 Environnement

## Pré-requis

Avant de développer sur Papillon, il est nécessaire d'installer quelques outils, ces outils peuvent varier selon votre système d'exploitation.

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://git-scm.com/">Git</a></td><td><a href="../.gitbook/assets/git.jpg">git.jpg</a></td></tr><tr><td><a href="https://nodejs.org/fr">Node.js</a></td><td><a href="../.gitbook/assets/nodejs.webp">nodejs.webp</a></td></tr><tr><td>Un éditeur de code tel que <a href="https://code.visualstudio.com/">Visual Studio Code</a></td><td><a href="../.gitbook/assets/1705325861037.jpg">1705325861037.jpg</a></td></tr><tr><td><a href="https://github.com/PapillonApp/Papillon/fork">Un Fork de Papillon</a></td><td><a href="../.gitbook/assets/0d4b064a-12cf-45c6-a58e-bc93c31e0b5c.jpg">0d4b064a-12cf-45c6-a58e-bc93c31e0b5c.jpg</a></td></tr><tr><td><a href="https://developer.android.com/studio?hl=fr">Android Studio</a> (conseillé pour développer sur Android)</td><td><a href="../.gitbook/assets/Android Studio - Social.png">Android Studio - Social.png</a></td></tr><tr><td><a href="https://bun.com/">Bun</a> (conseillé)</td><td><a href="../.gitbook/assets/0_pHX0bEaGCavLlQLk.png">0_pHX0bEaGCavLlQLk.png</a></td></tr></tbody></table>

#### Outils spécifiques à macOS

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><a href="https://developer.apple.com/xcode/">XCode</a></td><td><a href="../.gitbook/assets/0_Op_aBoFgTwCnnbdg.jpg">0_Op_aBoFgTwCnnbdg.jpg</a></td></tr><tr><td><a href="https://guides.cocoapods.org/using/getting-started.html">CocoaPods</a></td><td><a href="../.gitbook/assets/cocoapods_custom_script_24539e2b8a_2092ba8197.jpg">cocoapods_custom_script_24539e2b8a_2092ba8197.jpg</a></td></tr><tr><td><a href="https://brew.sh/">Homebrew</a> (conseillé)</td><td><a href="../.gitbook/assets/Apres-15-ans-le-mainteneur-de-Homebrew-envisage-de-gagner.jpg&#x26;si.webp">Apres-15-ans-le-mainteneur-de-Homebrew-envisage-de-gagner.jpg&#x26;si.webp</a></td></tr></tbody></table>

## Clonage du dépôt

Une fois que vous avez créé un fork de Papillon, vous allez pouvoir le télécharger localement afin d'y apporter des modifications via votre éditeur de code, pour cloner le fork, vous allez devoir utiliser l'outil Git, avec la commande suivante :

```bash
$ git clone https://github.com/PapillonApp/Papillon.git
```

Une fois que le dépôt est cloné, vous allez devoir installer ses dépendances, pour ce faire :

{% tabs %}
{% tab title="Windows" %}
```bash
$ cd Papillon
$ npm install
$ npx expo prebuild
```
{% endtab %}

{% tab title="MacOS" %}
Si vous avez déjà Cocoapods, vous pouvez directement effectuer les commandes suivantes:

```bash
$ cd Papillon
$ npm install
$ npx expo prebuild
$ cd ios && pod install && cd ../
```
{% endtab %}
{% endtabs %}

Tu peux ensuite ouvrir le dossier Papillon dans ton éditeur de code et commencer à faire des modifications, pour les tester, rien de plus simple, il suffit d'effectuer la commande spécifique à l'environnement sur lequel tu souhaites essayer :

{% tabs %}
{% tab title="Android" %}
```bash
$ npm run android
```
{% endtab %}

{% tab title="iOS/iPadOS (un Mac est requis)" %}
```bash
$ npm run ios
```
{% endtab %}
{% endtabs %}

## Effectuer sa première Pull Request ! :tada:

Une fois que tu as fait les modifications que tu voulais, tu peux créer une nouvelle branche à l'aide de la commande `git checkout -b feature/super-cool`, chez Papillon, nous respectons la spécification [Conventional Branch](https://conventional-branch.github.io/) afin de se repérer dans nos branches.

Ensuite, il te suffit d'ajouter tous les fichiers que tu souhaites pousser avec la commande `git add [fichier]` puis d'effectuer un commit avec `git commit -m [titre de ton commit] -m [description]`, il n'est pas obligatoire de mettre une description, mais tu dois respecter la spécification [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

Une fois que tout ça est fait, tu peux enfin pousser les modifications vers ton fork à l'aide de la commande `git push origin [nom de ta branche`, et tu peux ensuite, en allant dans l'onglet **Pull Requests** du dépôt GitHub de Papillon, ouvrir ta **Pull Request**.

## Et ensuite ?

Elle sera analysée en premier temps par un robot qui s'assurera de sa conformité avec les règles de contributions, si elle n'est pas conforme, elle obtiendra le label Invalide le temps que tu corriges ce qui ne va pas, ne t'inquiète pas, tout est expliqué par le robot sous ta Pull Request.&#x20;

Après cette première analyse, nous analyserons manuellement ta Pull Request, nous pouvons à ce stade, soit valider, soit demander des changements, une fois que tout sera bon, elle sera fusionnée avec le code principal !
