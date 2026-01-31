---
icon: house
layout:
  width: default
  title:
    visible: false
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

# Accueil

<figure><picture><source srcset=".gitbook/assets/Logo_Dark.png" media="(prefers-color-scheme: dark)"><img src=".gitbook/assets/Logo_Light.png" alt="" width="202"></picture><figcaption></figcaption></figure>

<p align="center">Un set d’icônes 100 % sur-mesure, conçu pour Papillon et le monde scolaire</p>

<p align="center"><a href="https://github.com/PapillonApp/Papicons" class="button primary">Voir sur GitHub</a> <a href="https://www.npmjs.com/package/@getpapillon/papicons" class="button secondary">Voir sur NPM</a></p>

***

{% columns %}
{% column width="41.66666666666667%" %}
### Simple à intégrer

Papicons propose une bibliothèque d’icônes modernes et harmonisées, spécialement conçues pour le monde de l'éducation. Simples à intégrer, elles permettent aux développeurs de créer des interfaces cohérentes, esthétiques et intuitives en un minimum d’effort.

<a href="components/papicons.md" class="button secondary" data-icon="rocket-launch">Commencer à intégrer</a>&#x20;
{% endcolumn %}

{% column width="58.33333333333333%" %}
{% code title="index.tsx" %}
```tsx
function Bouh() {
  return (
    <List>
      <Item>
        <Icon>
          <Papicons name="Ghost" />
        </Icon>
    
        <Typography variant="title">
          Bouh !
        </Typography>
      </Item>
    </List>
  )
};
```
{% endcode %}
{% endcolumn %}
{% endcolumns %}
