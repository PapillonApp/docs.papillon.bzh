---
description: Welcome to your team’s developer platform
hidden: true
layout:
  width: default
  title:
    visible: false
  description:
    visible: false
  tableOfContents:
    visible: false
  outline:
    visible: false
  pagination:
    visible: false
  metadata:
    visible: true
---

# Accueil

<figure><picture><source srcset=".gitbook/assets/image (2).png" media="(prefers-color-scheme: dark)"><img src=".gitbook/assets/image (1).png" alt="" width="375"></picture><figcaption></figcaption></figure>

<p align="center">Tout ce dont vous devez savoir sur Papillon, réuni en une seule source de connaissances.</p>

<p align="center"><a href="https://papillon.bzh/download" class="button primary">Obtenir Papillon</a> <a href="https://github.com/PapillonApp/Papillon" class="button secondary">Forker le projet sur GitHub</a></p>

<p align="center"></p>

***

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td><h4><i class="fa-square-terminal">:square-terminal:</i></h4></td><td><strong>Développer</strong></td><td>Commencer à compiler et modifier Papillon</td><td><a href="https://app.gitbook.com/s/Lt8mMBbf7ntjxrd29I4o/">Accueil</a></td><td><a href=".gitbook/assets/dev.png">dev.png</a></td></tr><tr><td><h4><i class="fa-swatchbook">:swatchbook:</i></h4></td><td><strong>Papillon UI</strong></td><td>Une librairie de composants innovante pour React Native</td><td><a href="https://app.gitbook.com/s/CYvYwrd5AG2cytF3fLrG/">Accueil</a></td><td><a href=".gitbook/assets/papillon_ui.png">papillon_ui.png</a></td></tr><tr><td><i class="fa-icons">:icons:</i></td><td><strong>Papicons</strong></td><td>Un set d'icônes conçues pour l'éducation</td><td><a href="https://app.gitbook.com/s/zAXRvshrILO6bQ2aJgMk/">Accueil</a></td><td><a href=".gitbook/assets/papicons.png">papicons.png</a></td></tr></tbody></table>



{% columns %}
{% column width="41.66666666666667%" %}
### Simple comme bonjour

Papillon UI simplifie le développement d'interface pour Papillon avec des composants pensés pour **permettre à tous les développeurs** de créer facilement des fonctionnalités intuitives.

<a href="https://app.gitbook.com/o/SIz7Oa9HbH0pdgTGvFYi/s/CYvYwrd5AG2cytF3fLrG/" class="button secondary" data-icon="rocket-launch">Découvrir Papillon UI</a>&#x20;
{% endcolumn %}

{% column width="58.33333333333333%" %}
{% code title="index.tsx" %}
```tsx
function HelloWorld() {
  return (
    <List>
      <Item>
        <Icon>
          <Papicons name="Butterfly" />
        </Icon>
    
        <Typography variant="title">
          Salut tout le monde !
        </Typography>
      </Item>
    </List>
  )
};
```
{% endcode %}
{% endcolumn %}
{% endcolumns %}

