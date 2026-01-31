---
icon: icons
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Icon

Icon est un wrapper conçu pour contenir une icône [**Lucide**](https://lucide.dev/icons/) ou une [**Papicon**](https://icons.papillon.bzh/). Celle-ci permet d'avoir d'avantage de contrôle sur l'affichage des icônes.

<figure><picture><source srcset="../.gitbook/assets/image (6).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (5).png" alt=""></picture><figcaption></figcaption></figure>

## Fonctionnement

{% tabs %}
{% tab title="Avec une Papicon" %}
<pre class="language-tsx"><code class="lang-tsx">import * as Papicons from "@getpapillon/papicons"
import Icon from "@/ui/components/Icon";

<strong>&#x3C;Icon papicon>
</strong><strong>  &#x3C;Papicons.Ghost />
</strong><strong>&#x3C;/Icon>
</strong></code></pre>
{% endtab %}

{% tab title="Avec une icône Lucide" %}
```tsx
import { Ghost } from "lucide-react-native";
import Icon from "@/ui/components/Icon";

<Icon>
  <Ghost />
</Icon>
```
{% endtab %}

{% tab title="Avec une Vector Icon" %}
```tsx
import { FontAwesome5 } from "@react-native-vector-icons/fontawesome5";
import Icon from "@/ui/components/Icon";

<Icon>
  <FontAwesome5 name="ghost" />
</Icon>
```
{% endtab %}
{% endtabs %}

## Propriétés

### `color`

Couleur de fond de l'icône (Ajoute un padding et un fond)

| Type          |
| ------------- |
| Couleur (HEX) |

### `fill`

Couleur de remplissage de l'icône

| Type          | Valeur par défaut                                 |
| ------------- | ------------------------------------------------- |
| Couleur (HEX) | _Couleur du texte selon le thème clair ou sombre_ |

### `papicon`

A activer si l'icône est une Papicon pour le fonctionnement d'`Icon`

{% hint style="warning" %}
Cette propriété sera inutile dans une future version des Papicons
{% endhint %}

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | false             |

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
