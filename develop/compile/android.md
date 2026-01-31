---
icon: android
---

# Compiler pour Android

## Via la ligne de commande

Dans un terminal de commande qui est dans le dossier GitHub Papillon, exécutez ces lignes :

{% tabs %}
{% tab title="Release" %}
```sh
git clone git@github.com:PapillonApp/Papillon.git
cd Papillon
npm install
npx expo prebuild -p android
cd .\android\
./gradlew ":app:assembleRelease"
```
{% endtab %}

{% tab title="Debug" %}
```sh
git clone git@github.com:PapillonApp/Papillon.git
cd Papillon
npm install
npx expo prebuild -p android
cd .\android\
./gradlew ":app:assembleDebug"
```
{% endtab %}
{% endtabs %}

L'APK est disponible ici

```shell
cd app/build/outputs/apk/release 
```
