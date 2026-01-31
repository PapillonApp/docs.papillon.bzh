---
icon: text-size
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

# Typography

Typography est un remplacement de [Text](https://reactnative.dev/docs/text) qui applique automatiquement le thème et les règles d'interface de Papillon UI sur l'ensemble de l'UI Kit.

<figure><picture><source srcset="../.gitbook/assets/image (48).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (47).png" alt=""></picture><figcaption></figcaption></figure>

## Exemple

Cet exemple affiche un titre de la couleur principale.

{% columns %}
{% column width="58.333333333333336%" %}
<pre class="language-tsx" data-title="example.tsx" data-overflow="wrap" data-line-numbers><code class="lang-tsx">&#x3C;Typography
<strong>  variant="h1"
</strong><strong>  color="primary"
</strong>>
  Lorem ipsum
&#x3C;/Typography>
</code></pre>
{% endcolumn %}

{% column width="41.666666666666664%" %}
<figure><picture><source srcset="../.gitbook/assets/image (50).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (49).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

<details>

<summary>Note sur les polices pré-installées</summary>

En plus des polices préinstallées dans l'OS, Papillon importe [SN Pro](https://supernotes.app/open-source/sn-pro/) sous les noms suivants :

* light
* regular
* medium
* semibold
* bold

</details>

## Propriétés

{% hint style="success" %}
Typography étend [Text](https://reactnative.dev/docs/text) et dispose de toutes ses propriétés
{% endhint %}

### `variant`

Style du texte (parmi les variantes disponibles)

<details>

<summary>Variantes disponibles</summary>

* Corps de texte
  * `body1`
  * `body2`
* Titres
  * `h1`
  * `h2`
  * `h3`
  * `h4`
  * `h5`
  * `h6`
* UI
  * `title`
  * `caption`
  * `button`
  * `navigation`

</details>

| Type   | Valeur par défaut |
| ------ | ----------------- |
| String | body1             |

### `color`

Couleur du texte (parmi les couleurs par défaut ou custom)

<details>

<summary>Couleurs de base</summary>

* `primary`
* `text`
* `secondary`
* `light`
* `danger`

</details>

| Type                    | Valeur par défaut |
| ----------------------- | ----------------- |
| Couleur (HEX) ou String | text              |

### `align`

Alignement du texte :

* `left`
* `center`
* `right`

| Type   | Valeur par défaut |
| ------ | ----------------- |
| String | left              |

### `inline`

Indique si le texte ne doit PAS prendre toute la largeur

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | false             |

### `nowrap`

Empêche le texte de passer sur plusieurs lignes

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | false             |

### `weight`

Police d'écriture (et non l'épaisseur puisqu'elle ne fonctionne pas sur les fonts custom)

| Type   |
| ------ |
| String |
