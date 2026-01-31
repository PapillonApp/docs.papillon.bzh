---
icon: list-radio
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

# TableFlatList

`<TableFlatList />` est un composant [Layout](./) utilisé pour concevoir des onglets **comportant principalement d'une liste avec sections**. Il est notamment utilisé dans les paramètres.

<figure><picture><source srcset="../../.gitbook/assets/image (35).png" media="(prefers-color-scheme: dark)"><img src="../../.gitbook/assets/image (29).png" alt=""></picture><figcaption></figcaption></figure>

{% hint style="success" %}
**Il étend les propriétés et le fonctionnement de** [**FlatList**](https://reactnative.dev/docs/flatlist) tout en ayant la capacité d'utiliser comme composant étendu [FlashList](https://shopify.github.io/flash-list/) et [LegendList](https://legendapp.com/open-source/list/api/gettingstarted/) si nécessaire.
{% endhint %}

Celui-ci est utilisé principalement pour afficher un grand nombre de données dans des List tout en privilégiant les performances. Il faut impérativement l'utiliser si un écran se compose principalement de List avec beaucoup de données ou des informations chargées depuis un environnement externe.

## Exemple

Cet exemple affiche 3 élements dans une section.

{% columns %}
{% column width="50%" %}
{% code title="example.tsx" %}
```tsx
<TableFlatList
  sections={[
    {
      title: "Première section",
      items: [
        {
          title: "Je suis un Item",
          description: "Je décris un item"
        },
        {
          title: "Je suis un autre Item",
          description: "Je décris cet autre item"
        },
        {
          papicon: <Papicons.Butterfly />,
          title: "Je suis mieux que vous",
          description: "Pourquoi ? J'ai une icône géniale !"
        }
      ]
    }
  ]}
/>
```
{% endcode %}
{% endcolumn %}

{% column width="50%" %}
<figure><picture><source srcset="../../.gitbook/assets/image (13).png" media="(prefers-color-scheme: dark)"><img src="../../.gitbook/assets/image (33).png" alt=""></picture><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

## Propriétés

TableFlatList étend les propriétés de [FlatList](https://reactnative.dev/docs/flatlist).&#x20;

{% hint style="danger" %}
Il n'est **pas possible** d'indiquer un **`renderItem`** et des **`data`.**

**Ces propriétés sont automatiquement managées par Papillon UI et les déclarer casse le fonctionnement et l'utilité de la TableFlatList.**
{% endhint %}

### `sections` <sup><sub><mark style="color:$danger;">(\*)<mark style="color:$danger;"><sub></sup>

Éléments a afficher dans la liste

| Type            |
| --------------- |
| Array\<Section> |

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

## Types

### `Section`

Une section contient un header avec son titre et une icône, ainsi que le contenu (des [SectionItem](tableflatlist.md#sectionitem)).

| Propriété                                                                                 | Type                                               | Usage                                                 |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------------- |
| items <sup><sub><mark style="color:$danger;">(\*)<mark style="color:$danger;"><sub></sup> | Array<[SectionItem](tableflatlist.md#sectionitem)> | Array contenant les items                             |
| title                                                                                     | String                                             | Titre de la section (affiché au dessus de celle-ci)   |
| icon                                                                                      | React.ReactNode                                    | Élément React utilisé comme icône                     |
| papicon                                                                                   | React.ReactNode                                    | Élément issu des Papicons utilisé à la place d'`icon` |
| hideTitle                                                                                 | Booléen                                            | Masquer le header de la section                       |

### `SectionItem`

Un item retourne un \<Item /> conçu pour apparaître dynamiquement dans une section.

| Propriété   | Type            | Usage                                              |
| ----------- | --------------- | -------------------------------------------------- |
| leading     | React.ReactNode | Élément placé en amont du contenu                  |
| trailing    | React.ReactNode | Élément placé en aval du contenu                   |
| icon        | React.ReactNode | Icône affichée à la place du Leading               |
| papicon     | React.ReactNode | Icône Papicons affichée a la place d'`icon`        |
| content     | React.ReactNode | Élément React custom contenu dans l'Item           |
| title       | String          | Affiche un Typography type `title` dans l'item     |
| description | String          | Affiche un Typography type `caption` dans l'item   |
| tags        | Array\<String>  | Affiche une liste de tags après la description     |
| onPress     | () => void      | Fonction appelée à l'appui                         |
| itemProps   | PressableProps  | Propriétés supplémentaires passées à l'item wrappé |
