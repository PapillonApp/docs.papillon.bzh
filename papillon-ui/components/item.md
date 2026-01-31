---
icon: circle-info
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

# Item

Item est un élément conçu pour être placé dans une [`List`](list.md) ou dans une [`TableFlatList`](layouts/tableflatlist.md). Il permet de concevoir facilement des interfaces sectionnées. **Il remplace l'ancien `<NativeItem />`.**

<figure><picture><source srcset="../.gitbook/assets/image (7).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (36).png" alt=""></picture><figcaption></figcaption></figure>

## Fonctionnement

Item est un élément **dynamique et intelligent**. Il adapte automatiquement le placement de son contenu selon son type, ce qui lui permet d'être utile pour construire rapidement des interfaces complètes.

{% hint style="info" %}
Lors des exemples suivants, les Item seront wrappés dans une List, comme ils doivent être utilisés.
{% endhint %}

### Texte

Pour commencer un Item, on ajoute habituellement un titre et un sous-titre. Pour cela, on va utiliser `<Typography/>` et ses variantes conçues pour Item.

{% columns %}
{% column width="50%" %}
<pre class="language-tsx" data-title="example.tsx" data-line-numbers><code class="lang-tsx">&#x3C;List>
  &#x3C;Item>
<strong>    &#x3C;Typography variant="title">
</strong><strong>      Salut tout le monde !
</strong><strong>    &#x3C;/Typography>
</strong><strong>    &#x3C;Typography variant="caption">
</strong><strong>      Comment ça va ?
</strong><strong>    &#x3C;/Typography>
</strong>  &#x3C;/Item>
&#x3C;List>
</code></pre>
{% endcolumn %}

{% column width="50%" %}
<figure><picture><source srcset="../.gitbook/assets/image (39).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (38).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

### Icône

Pour ajouter une icône, on va faire appel a l'élément `<Icon />`.

{% columns %}
{% column width="50%" %}
<pre class="language-tsx" data-title="example.tsx" data-line-numbers><code class="lang-tsx">&#x3C;List>
  &#x3C;Item>
<strong>    &#x3C;Icon papicon>
</strong><strong>      &#x3C;Papicons.Student />
</strong><strong>    &#x3C;/Icon>
</strong>
    &#x3C;Typography variant="title">
      Salut tout le monde !
    &#x3C;/Typography>
    &#x3C;Typography variant="caption">
      Comment ça va ?
    &#x3C;/Typography>
  &#x3C;/Item>
&#x3C;/List>
</code></pre>
{% endcolumn %}

{% column width="50%" %}
<figure><picture><source srcset="../.gitbook/assets/image (41).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (40).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

### Trailing

`Trailing` est un élément placé en fin d'Item, il peut contenir n'importe quel composant React.

{% hint style="success" %}
Papillon UI le place et l'espace automatiquement, peu importe sa position dans le code.
{% endhint %}

{% columns %}
{% column width="50%" %}
<pre class="language-tsx" data-title="example.tsx" data-line-numbers><code class="lang-tsx">&#x3C;List>
  &#x3C;Item>
    {/* Reste du code */}
    
<strong>    &#x3C;Trailing>
</strong><strong>      &#x3C;Button
</strong><strong>        title="Bouton"
</strong><strong>        size="small"
</strong><strong>        inline
</strong><strong>      />
</strong><strong>    &#x3C;/Trailing>
</strong>  &#x3C;/Item>
&#x3C;/List>
</code></pre>
{% endcolumn %}

{% column width="50%" %}
<figure><picture><source srcset="../.gitbook/assets/image (43).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (42).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

### Leading

`Leading` est un élément placé en début d'Item, il peut contenir n'importe quel composant React.

{% hint style="success" %}
Papillon UI le place et l'espace automatiquement, peu importe sa position dans le code.
{% endhint %}

{% columns %}
{% column width="50%" %}
<pre class="language-tsx" data-title="example.tsx" data-line-numbers><code class="lang-tsx">&#x3C;List>
  &#x3C;Item>
<strong>    &#x3C;Leading>
</strong><strong>      &#x3C;Image source={require('@/assets/images/icon.png')} style={{ width: 40, height: 40, borderRadius: 10 }} />
</strong><strong>    &#x3C;/Leading>
</strong>
    {/* Reste du code */}
  &#x3C;/Item>
&#x3C;/List>
</code></pre>
{% endcolumn %}

{% column width="50%" %}
<figure><picture><source srcset="../.gitbook/assets/image (10).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (44).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

## Propriétés

### `onPress`

Appelé lorsqu'un appui est enregistré sur l'`Item`

| Type                                |
| ----------------------------------- |
| ({nativeEvent: PressEvent}) => void |
