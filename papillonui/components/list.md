---
icon: table-list
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

# List

List est un élément conçu pour contenir des [`Item`](item.md) en dehors d'une [`TableFlatList`](layouts/tableflatlist.md). Il permet de concevoir facilement des interfaces sectionnées.

<figure><picture><source srcset="../.gitbook/assets/image (12).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (11).png" alt=""></picture><figcaption></figcaption></figure>

{% hint style="danger" %}
Si la vue se compose essentiellement de [`List`](list.md) ou qu'il faut les sectionner, **privilégiez le** [**Layout**](layouts/) [**`TableFlatList`**](layouts/tableflatlist.md)
{% endhint %}

## Usage

Pour utiliser List, il suffit de l'importer et d'y mettre du contenu. List applique automatiquement les séparations et le placement des items à l'intérieur.

{% hint style="warning" %}
List peut contenir autre chose que des Item, **mais cet usage n'est pas recommandé.**
{% endhint %}

{% columns %}
{% column %}
<pre class="language-tsx" data-title="example." data-line-numbers><code class="lang-tsx"><strong>&#x3C;List>
</strong>  {Array.from({ length: 10 }, (_, i) => (
    &#x3C;Item key={i}>
      &#x3C;Typography>
        Je suis l'item {i + 1}
      &#x3C;/Typography>
    &#x3C;/Item>
  ))}
<strong>&#x3C;/List>
</strong></code></pre>
{% endcolumn %}

{% column %}
<figure><picture><source srcset="../.gitbook/assets/image (9).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (8).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

## Propriétés

### `disablePadding`

Supprime le padding appliqué automatiquement aux éléments n'étant pas `<Item />`.

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | false             |

### `radius`

Bordure arrondie de la liste

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Nombre | 20                |

### `marginBottom`

Marge inférieure appliquée au conteneur de la liste

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Nombre | 12                |

### `animated`

Si l'élément doit s'animer automatiquement ou non ([Layout Transitions](https://docs.swmansion.com/react-native-reanimated/docs/layout-animations/layout-transitions))

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | True              |

### `entering`

Animation d'entrée de la liste ([Reanimated.View](https://docs.swmansion.com/react-native-reanimated/docs/layout-animations/entering-exiting-animations/))

| Type                     |
| ------------------------ |
| EntryOrExitAnimationType |

### `exiting`

Animation de sortie de la liste ([Reanimated.View](https://docs.swmansion.com/react-native-reanimated/docs/layout-animations/entering-exiting-animations/))

| Type                     |
| ------------------------ |
| EntryOrExitAnimationType |
