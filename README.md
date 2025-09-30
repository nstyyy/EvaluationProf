# README.md

📘 Documentation Git — Workflow en équipe
👥 Contexte

Nous sommes une équipe de 4 développeurs travaillant sur un même projet collaboratif.
Pour organiser notre travail, nous utilisons un workflow Git inspiré du GitHub Flow et du Feature Branching, combinant simplicité et rigueur :

Développement clair et structuré via des branches spécifiques.

Pull Requests pour la revue et la validation.

Gestion des corrections urgentes et des releases.

🚀 Objectif

Mettre en place un processus de gestion de branches Git :

Clair : chaque développeur sait où coder.

Reproductible : tout le monde suit les mêmes règles.

Adapté au travail en équipe : revue de code, tests, bonne communication.

🗂️ Structure des branches
Branche	Rôle
main	Branche de production (stable, prête à être déployée).
dev	Branche d’intégration (version en cours de développement stable).
feature/*	Branches pour chaque fonctionnalité spécifique (ex: feature/login-system).
hotfix/*	Branches pour les corrections urgentes en production.
release/*	Préparation des versions (stabilisation, QA, etc.).
🔄 Cycle de vie d’une fonctionnalité

Se baser sur la branche develop

git checkout develop
git pull
git checkout -b feature/nom-fonctionnalité


Exemple :

feature/login-api

feature/page-dashboard

Développer la fonctionnalité

Commits clairs et réguliers

Respect des conventions de code

Philosophie : commit early, commit often

Pousser la branche

git push -u origin feature/nom-fonctionnalité


Ouvrir une Pull Request (PR) vers develop

Revue de code par au moins 1 reviewer

Fusion via la plateforme (GitHub/GitLab/Bitbucket), pas de merge local direct

Fusion et cycle de release

Les fonctionnalités validées vont de develop vers main.

Les branches feature peuvent être conservées pour suivi.

🔥 Corrections urgentes (Hotfix)

En cas de bug critique en production :

git checkout main
git pull
git checkout -b hotfix/nom-correction


Une fois corrigé : PR vers main puis merge également dans develop.

📂 Documentation incluse

Bonne_Pratiques.md
Règles de nommage, structure des commits, conventions de code, etc.

Commandes_de_base.md
Liste des commandes utiles pour :

Installer le projet en local.

Créer/naviguer entre les branches.

Effectuer des commits et des push.

✍️ Nomenclature des commits

Format recommandé :

[numéro-de-ticket][ACTION] message clair

Actions disponibles

[CREATE] : création.

[REMOVE] : suppression.

[MODIF] : modification.

Exemples de tickets

[130] [CREATE] Page d’accueil du site

[131] [CREATE] Page "about" (description de l’entreprise)

[132] [CREATE] Page des services proposés

[133] [CREATE] Page de contact

🧭 Exemple visuel
main
 └───┬─────────────┐
     │             │
     │         hotfix/bug-urgent
     │
   develop
    ├─ feature/login
    ├─ feature/dashboard
    └─ feature/api-refacto

📞 Contact / Référent technique

Nom : [à compléter]

Mail : [à compléter]

Slack : #dev-workflow
