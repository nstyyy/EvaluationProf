# API Integration (Connexion avec une API externe)

## Objectif
Connecter l’application à un service externe.

## Étapes
- Configurer les clés d’API dans un fichier sécurisé (.env)
- Créer un service d’appel API
- Récupérer et afficher les données dans l’interface

## Commandes Git utilisées
- `git checkout -b feature/api-integration`
- `git add docs/API_INTEGRATION.md`
- `git commit -m "docs: ajout doc intégration API"`
- `git push -u origin feature/api-integration`

## Bonnes pratiques
- Ne pas exposer les clés d’API dans le code
- Gérer les erreurs réseau
- Limiter le nombre d’appels API
