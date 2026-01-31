---
description: >-
  Papicons est un wrapper conçu pour contenir une icône du set d'icône Papillon.
  Celle-ci permet de se protéger des dépréciations ou d'afficher une icône
  temporaire en attendant une mises à jour.
icon: icons
---

# Papicons

<figure><picture><source srcset="../.gitbook/assets/image (3).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (2).png" alt=""></picture><figcaption></figcaption></figure>

## Fonctionnement

```tsx
import { Papicons } from "@getpapillon/papicons"

<Papicons name={"Ghost"} />
```

## Propriétés

{% hint style="info" %}
Les icones hérite des propriétés de [SvgProps](https://github.com/software-mansion/react-native-svg/blob/main/src/elements/Svg.tsx#L39).
{% endhint %}

### `name` <mark style="color:orange;">\*</mark>

Nom de l'icône à utiliser

| Type   | Valeur en cas d'erreur |
| ------ | ---------------------- |
| String | `Placeholder`          |

### `color`

Couleur de remplissage de l'icône

| Type          | Valeur par défaut                                                  |
| ------------- | ------------------------------------------------------------------ |
| Couleur (HEX) | _Couleur du texte selon le thème clair ou sombre (`currentColor`)_ |

### `size`

Taille de l'icône

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Nombre | 24                |

### `opacity`

Opacité de l'icône

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Nombre | 1                 |
