# 📈 Moyennes générales

Chez Papillon, **on sait que ta moyenne est super importante.** Mais comment on la calcule ? C'est un peu un jeu de détective ! Le problème ? Chaque école a sa propre "recette" pour faire les moyennes.

Notre solution ? On fait de notre mieux pour l'estimer. Mais c'est pas toujours parfait.

À noter que lorsque la moyenne nous est fournie par l'établissement, celle-ci est affichée et l'interface vous l'indique également.

***

{% columns fullWidth="false" %}
{% column %}
<figure><picture><source srcset="../.gitbook/assets/image (2) (1).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (2).png" alt=""></picture><figcaption></figcaption></figure>

#### **Affichage lorsque la moyenne est fournie par l'établissement**

Le chiffre affiché est exactement le même que celui de votre service (Pronote, ÉcoleDirecte, etc.)
{% endcolumn %}

{% column %}
<figure><picture><source srcset="../.gitbook/assets/image (3).png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/image (1) (1).png" alt=""></picture><figcaption></figcaption></figure>

#### **Affichage lorsque la moyenne n'est pas fournie par l'établissement**

Le chiffre affiché est **estimé**. La date affiche le moment du calcul : à la note sélectionnée ou à la plus récente.
{% endcolumn %}
{% endcolumns %}

***

### Comment estime-t-on les moyennes ?

Dans l'application, tu as le choix entre plusieurs algorithmes de calcul. Vous pouvez tous les retrouver [sur le dépôt Git du projet](https://github.com/PapillonApp/Papillon/tree/main/utils/grades/algorithms).

{% tabs %}
{% tab title="Moyenne des matières" %}
> La moyenne des matières est utilisée par défaut car celle ci est utilisée en majorité par les établissements scolaires. **Celle ci calcule la moyenne de chaque matière puis en fait une moyenne générale**.

{% hint style="success" %}
**C'est la méthode par défaut utilisée par Papillon**. C'est généralement la plus fiable et la plus proche de ta vraie moyenne générale. Cependant, il peut y avoir un écart entre 0.1 pt et un demi-point dans le pire des cas.
{% endhint %}

D'abord, elle calcule la moyenne de chaque matière. Pour cela, elle convertit toutes les notes sur une base de /20 (par exemple, un 12/15 devient un 16/20) et les multiplie par leur coefficient pour donner plus de poids aux notes importantes.

Elle gère également les notes bonus (qui ajoutent des points d'avance) et les notes facultatives (qui sont ignorées si elles font baisser ta moyenne), puis il applique la formule classique :

$$
\text{Moyenne} = \left(\frac{\text{Total des points obtenus}}{\text{Total des points possibles}}\right) \times 20
$$

Enfin, il prend toutes les moyennes de matière obtenues et en fait la moyenne arithmétique pour donner ta note générale:&#x20;

$$
\text{Moyenne Générale} = \frac{\text{Moyenne Maths} + \text{Moyenne Français} + \dots}{\text{Nombre de Matières}}
$$
{% endtab %}

{% tab title="Moyenne pondérée" %}
Contrairement à la **moyenne des matières**, la moyenne pondérée ne sépare pas les notes en matières avant d'en calculer la moyenne. Elle calcule l'ensemble des notes indépendamment de leur appartenance à une matière. Ça peut s'apparenter à une **moyenne de notes**.\
\
Il s'agit donc d'une moyenne pondérée classique sur l'ensemble des points :

$$
\text{Moyenne} = \left(\frac{\text{Total des points obtenus pondérés}}{\text{Total des points possibles pondérés}}\right) \times 20
$$
{% endtab %}

{% tab title="Médiane des matières" %}
> La médiane est une autre façon de regarder tes résultats. Contrairement à la moyenne qui peut être complètement faussée par une seule très bonne ou très mauvaise note, **la médiane coupe ton ensemble de notes en deux parties égales**.

{% hint style="info" %}
La médiane te permet de savoir où tu te situes "au milieu" de tes notes. **Elle peut être bien plus haute ou plus basse que ta moyenne, mais ne reflète pas la moyenne de ton bulletin : c'est un outil pour voir le millieu des notes que tu as eu le plus souvent.**
{% endhint %}

Pour la calculer, l'application prend toutes tes notes converties sur 20, les trie de la plus petite à la plus grande, et prend la note qui se trouve pile au centre.

* Si tu as un nombre impair de notes, c'est la note du milieu : $$\text{Position} = \frac{n + 1}{2}$$
* Si tu as un nombre pair de notes, elle fait la moyenne des deux notes centrales : $$\text{Position} = \frac{n}{2} \text{ et } \frac{n}{2} + 1$$

C'est un excellent outil pour voir ta vraie régularité, sans qu'un accident (un 02/20) ou un exploit (un 20/20) ne vienne masquer le reste de tes efforts !
{% endtab %}
{% endtabs %}

### Pourquoi ma moyenne n'est pas la bonne ?

On ne connaît malheureusement pas votre moyenne exacte. Si nous sommes en capacité de vous la donner, cela sera affiché juste en dessous de votre moyenne avec la mention "fournie par l'établissement". Sinon, nous faisons de notre mieux pour avoir la note la plus précise possible.
