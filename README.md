Déploiement Automatisé d’un Site Web Statique

Description
Ce projet met en place un pipeline CI/CD pour déployer automatiquement un site web statique hébergé sur Amazon S3.
Le code source est versionné sur GitHub, et le déploiement est automatisé grâce à AWS CodeBuild.


 Technologies utilisées
GitHub : hébergement du code source et gestion des versions.

AWS CodeBuild : service de build et d’intégration continue.

Amazon S3 : stockage et hébergement du site web statique.

IAM : gestion des permissions et rôles nécessaires au pipeline.

 Architecture
Le code est poussé sur GitHub.

CodeBuild est déclenché automatiquement (via webhook ou CodePipeline).

Le projet est construit et les fichiers statiques sont générés.

Les fichiers sont déployés dans un bucket S3 configuré pour l’hébergement de site web.

Le site est accessible via l’URL publique du bucket ou via un domaine personnalisé (optionnel avec Route 53 + CloudFront).

 Structure du projet
.
├── buildspec.yml   # Fichier de configuration pour CodeBuild
├── index.html      # Page principale du site
├── assets/         # Images, CSS, JS
└── README.md       # Documentation du projet