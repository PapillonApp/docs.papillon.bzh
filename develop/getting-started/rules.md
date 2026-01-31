# 🚫 Règles de contribution

## :closed\_lock\_with\_key: Signaler une vulnérabilité

Nous prenons la sécurité **très au sérieux**. Si vous découvrez une **vulnérabilité** dans **Papillon**, merci de suivre notre [**politique de sécurité**](https://github.com/PapillonApp/Papillon/.github/blob/main/SECURITY.md) : **n’ouvrez pas d’issue publique** et signalez-la directement à l’adresse suivante : <mark style="color:$danger;">**support@papillon.bzh**</mark>.

## :outbox\_tray: Soumettre une Pull Request

Nous serions ravis d’intégrer vos modifications à Papillon. Cependant, avant de fusionner avec la branche principale, merci de respecter les règles ci-dessous. En cas de non-respect, votre Pull Request sera considérée comme **invalide** et ne sera pas traitée tant que les corrections nécessaires n’auront pas été apportées.

* [x] Vous ne devez pas soumettre plusieurs fonctionnalités ou corrections de bugs dans une même Pull Request. Chaque modification doit rester isolée afin de faciliter son traitement et, si nécessaire, son éventuel retour.
* [x] Si votre Pull Request concerne des changements majeurs, merci d'ouvrir une Issue pour discuter avec les mainteneurs de la stratégie à adopter pour ne pas faire de gros travaux pour rien.
* [x] Votre Pull Request doit respecter les conventions [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) et [Conventional Branch](https://conventional-branch.github.io/), ainsi que le style de code de l’application.
* [x] Si votre Pull Request modifie une partie documentée, comme la structure, l’architecture ou autre, assurez-vous d’avoir mis à jour la documentation en conséquence.
* [x] J'ai testé mes changements sur iOS et Android et l'application compile correctement.
* [x] J'utilise un langage informel (tutoiement).

#### :question: Comment vérifier le Lint ?

Par défaut, en effectuant la commande ci-dessous, ESLint essayera de résoudre automatiquement les problèmes, s'il n'y arrive pas, vous devrez les corriger manuellement.

```bash
$ npm run lint
```

## :inbox\_tray: Ouvrir une issue

Avant d’ouvrir une issue, assurez-vous d’utiliser la **dernière version** de **Papillon**, testez si le problème persiste après mise à jour, et vérifiez qu’une issue similaire n’a pas **déjà** été ouverte. Une issue bien écrite facilite son traitement et est toujours plus agréable pour nous à lire, afin que le traitement se passe au mieux, voici quelques conseils :

1. **Elle porte un nom explicite**, qui permet d’identifier **immédiatement** son **sujet principal**.
2. **Aucune issue semblable n’existe déjà** : il est inutile d’en créer plusieurs pour le même problème, **cela ne fait que ralentir son traitement**. Si vous êtes concerné par une issue existante, **réagissez** simplement avec un👍
3. **Elle contient une description détaillée**, si c’est une fonctionnalité, elle est **clairement expliquée**, idéalement accompagnée d’une **capture d’écran** ou d’un **design Figma,** s’il s’agit d’un bug, la description précise **le comportement actuel**, **le comportement attendu**, ainsi que **les étapes pour le reproduire**.
4. Si vous rencontrez **le même problème** ou souhaitez **la même fonctionnalité**, privilégiez les **réactions** aux commentaires.
5. **Complétez le modèle fourni lors de la création de votre issue**, il a été rédigé pour vous aider à **structurer votre demande, ne rien oublier d’important et gagner du temps**.
