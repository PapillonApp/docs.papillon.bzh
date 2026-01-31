# 📂 Structure

{% hint style="danger" %}
Afin de **ne pas surcharger** cette page, seuls les fichiers considérés comme **utiles au développement** y sont **répertoriés**.
{% endhint %}

```
├── app
│   ├── (new)          # Fondation de l'application, il n'est généralement pas utile de modifier son contenu
│   ├── (settings)     # Dossier relatif à la page des paramètres
│   └── (tabs)         
│        └── calendar  # Dossier relatif à l'onglet "Emploi du temps"
│        └── grades    # Dossier relatif à l'onglet "Notes"
│        └── index     # Dossier relatif à l'onglet principal
│        └── profile   # Dossier relatif à l'onglet "Profil"
│        └── tasks     # Dossier relatif à l'onglet "Tâches"
├── assets             # Contient les ressources utiles à l'application
├── ios                # Dossier généré automatiquement par Expo, sert à compiler l'application pour iOS
├── android            # Dossier généré automatiquement par Expo, sert à compiler l'application pour Android
├── components
├── database           # Tout ce qui est relatif à l'intégration de WatermelonDB
│   ├── mappers        # Fonctions utilitaires pour transformer le retour de WatermelonDB en données compatibles avec le Manager
│   ├── models         # Modèles nécessaires au fonctionnement de WatermelonDB
│   ├── index.ts       # Déclaration du schéma et des modèles
│   ├── schema.ts      # Schéma servant au fonctionnement de WatermelonDB ; sa version doit être incrémentée à chaque mise à jour
│   └── use[...].ts    # Contient les fonctions utiles à l'ajout/l'obtention dans la base de données
├── locales            # Dossier contenant les traductions dans les différentes langues supportées par Papillon
│   ├── [lang].json    # Fichier spécifique à chaque langue supportée par Papillon 
├── services
│   ├── ecoledirecte   # Dossier contenant toutes les fonctions utiles à l'intégration d'ÉcoleDirecte
│   ├── pronote        # Dossier contenant toutes les fonctions utiles à l'intégration de Pronote
│   ├── shared         # Dossier centralisant les classes et interfaces utilisées par les différents services
│   └── skolengo       # Dossier contenant toutes les fonctions utiles à l'intégration de Skolengo
├── stores             # Tout ce qui est relatif à l'intégration de MMKV
│   ├── account        # Contient le stockage des comptes
│   ├── flags          # Contient le stockage des flags, nécessaire pour activer certaines fonctionnalités
│   ├── global       
│   └── logs
├── ui                 # Tout ce qui est relatif à Papillon UI : composants et utilitaires
│   ├── components
│   └── utils
├── utils
│   ├── grades
│       └── algorithms # Algorithmes utilisés pour calculer une approximation des moyennes
│   ├── logger
│   ├── subjects       # Gestion de la personnalisation des matières et de la classification par Kora
│   ├── theme          # Gestion du mode sombre/clair
│   ├── adjustColor.ts
│   └── generateId.ts  # Certains IDs sont dynamiques ; les IDs finaux sont générés ici
└────── i18n.ts        # Fichier contenant les traductions de Papillon
```
