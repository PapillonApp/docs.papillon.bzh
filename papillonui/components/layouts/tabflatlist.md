---
icon: objects-column
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

# TabFlatList



{% hint style="danger" %}
**Déprécié depuis la v8.3**

TabFlatList est déprécié en faveur de TabHeader sur l'appli Papillon. Il ne sera plus maintenu ou mis à jour
{% endhint %}

`<TabFlatList />` est un composant [Layout](./) utilisé pour concevoir des onglets complexes **avec un header repliant animé**. Il est notamment utilisé sur l'onglet des Notes, des Tâches et du Profil.

<figure><picture><source srcset="../../.gitbook/assets/image (34).png" media="(prefers-color-scheme: dark)"><img src="../../.gitbook/assets/image (28).png" alt=""></picture><figcaption></figcaption></figure>

{% hint style="success" %}
**Il étend les propriétés et le fonctionnement de** [**FlatList**](https://reactnative.dev/docs/flatlist) tout en ayant la capacité d'utiliser comme composant étendu [FlashList](https://shopify.github.io/flash-list/) et [LegendList](https://legendapp.com/open-source/list/api/gettingstarted/) si nécessaire.
{% endhint %}

Celui-ci est utilisé principalement pour afficher des grandes listes de données similaires ou des interfaces complèxes accompagné d'un header mobile tout en privilégiant un haut niveau de performances au render et au scroll.

## Propriétés

TabFlatList étend les propriétés de [FlatList](https://reactnative.dev/docs/flatlist).&#x20;

{% hint style="warning" %}
Il est **obligatoire** d'indiquer un **`renderItem`** et des **`data`.**
{% endhint %}

<details>

<summary>Éléments obligatoires inhérents à FlatList (<code>renderItem</code> et <code>data</code>)</summary>

### <mark style="color:$danger;">`renderItem`</mark> <sub><mark style="color:$danger;">(FlatList)<mark style="color:$danger;"></sub>

Prend un item de data et le rend à l'intérieur de la liste. Ajoute également des propriétes telles que `index` au rendu.

| Type     |
| -------- |
| Fonction |

### <mark style="color:$danger;">`data`</mark> <sub><mark style="color:$danger;">(FlatList)<mark style="color:$danger;"></sub>

Une array (liste) d'éléments à rendre

| Type  |
| ----- |
| Liste |

</details>

### `engine`

Composant FlatList wrappé et utilisé pour le rendu de la liste. 3 options disponibles.

* [FlatList](https://reactnative.dev/docs/flatlist)
  * Composant de liste par défaut de React Native
* [FlashList](https://shopify.github.io/flash-list/) (expérimental)
  * Plus performant que FlatList
  * Maintenu et très documenté
  * **Ne fonctionne pas pour le moment avec TabFlatList et le background**
* [LegendList](https://github.com/LegendApp/legend-list)
  * Beaucoup plus performant que les deux autres
  * Instable avec des layouts complexes

| Type   | Valeur par défaut |
| ------ | ----------------- |
| String | FlatList          |

### `header`

Render le composant React a placer dans la partie supérieure animée. L'animation réduit l'échelle du component en fonction du scroll.

Ce component est rendu **en dehors et au dessus** de la FlatList d'engine.

{% hint style="danger" %}
La hauteur du header est définie par la propriété [`height`](tabflatlist.md#height) et non par le composant lui-même.
{% endhint %}

{% columns fullWidth="true" %}
{% column width="58.333333333333336%" %}
<pre class="language-tsx" data-title="example.tsx" data-full-width="true"><code class="lang-tsx">&#x3C;TabFlatList
<strong>  header={
</strong><strong>    &#x3C;View>
</strong><strong>      &#x3C;Text>Coucou !&#x3C;/Text>
</strong><strong>    &#x3C;/View>
</strong>  }
/>
</code></pre>


{% endcolumn %}

{% column width="41.666666666666664%" %}
<figure><picture><source srcset="../../.gitbook/assets/image (14).png" media="(prefers-color-scheme: dark)"><img src="../../.gitbook/assets/image (32).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

| Type            |
| --------------- |
| React.ReactNode |

### `height`

Hauteur du composant parent de [`header`](tabflatlist.md#header). Cette height sera repliée avec le scroll de la vue.

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Number | 120               |

### `padding`

Espace (padding) autour des éléments rendus (renderItem) dans la vue scrollable.

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Number | 16                |

### `gap`

Espace entre les éléments rendus (renderItem) dans la vue scrollable.

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Number | 0                 |

### `radius`

Bordure arrondie de la carte contenant la vue scrollable.

{% hint style="success" %}
**Privilégiez un** [**radius concentrique**](https://stackoverflow.com/questions/50096684/calculating-outer-corner-radius-for-concentric-rounded-corners-of-a-border) **avec vos élements UI** si ceux-ci commencent directement dans la liste pour un confort visuel et le respect des guides d'interface Papillon.
{% endhint %}

| Type   | Valeur par défaut |
| ------ | ----------------- |
| Number | 28                |

### `backgroundColor`

Couleur de fond de la vue

| Type          | Valeur par défaut                                                                     |
| ------------- | ------------------------------------------------------------------------------------- |
| Couleur (HEX) | <img src="../../.gitbook/assets/image (21).png" alt="" data-size="original">  #F7E8F5 |

### `foregroundColor`

Couleur du [`pattern`](tabflatlist.md#pattern) (si utilisé) de la vue

| Type          | Valeur par défaut                                    |
| ------------- | ---------------------------------------------------- |
| Couleur (HEX) | ![](<../../.gitbook/assets/image (22).png>)  #29947A |

### `translucent`

Supprime l'arrière plan de la carte inférieure

| Type    | Valeur par défaut |
| ------- | ----------------- |
| Booléen | false             |

### `pattern`

Motif utilisé dans le fond de la vue. Fonctionne uniquement avec les motifs prédéfinis :

* `dots`
* `checks`
* `grades`

| Type   |
| ------ |
| String |

### `onFullyScrolled`

Callback qui sera appelé lorsque le header sera entièrement replié.

| Type                                   |
| -------------------------------------- |
| `({isFullyScrolled: boolean}) => void` |
