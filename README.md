# Recruiter Console — Backend Rails API + Frontend React

Cette application est une API **Rails** pour gérer des offres d’emploi (`Job`) avec authentification minimale via **Devise** (`Recruiter`). Le **frontend React** est intégré dans `./front` pour faciliter le test.

## 🛠 Prérequis

- Ruby >= 3.2  
- Rails >= 7.2.1
- Node.js & npm

---

## Installation

1. **Décompresser le projet**

```bash
Dans GitHub -> Code -> Download .zip
unzip recruiter_console.zip
cd recruiter_console

```
2. **Installer les gems**

```
bundle install
```

3. **Créer et migrer la base SQLite**
```
bin/rails db:create
bin/rails db:migrate
```

4. **Seed les data**
```
bin/rails db:seed
```

5. **Démarrer le serveur Rails**
```
bin/rails s
```

6. **Installer le frontend**
```
cd front
npm install
PORT=3001 npm start
```


7. **Connexion**
```
Email : demo@recruiter.com

Mot de passe : passwordCyberSecu1234
```

## Architecture du projet
### Frontend (./front)

J’ai choisi une architecture modulable pour le frontend afin de séparer clairement les responsabilités et de faciliter la maintenance et l’évolution du projet.

- components/ : composants réutilisables

JobCard.tsx et JobFormModal.tsx pour afficher et modifier un job

Jobs.tsx : page principale de gestion des jobs

- pages/ : Pages complètes

Dashboard.tsx, Candidates.tsx, Login.tsx

- api.tsx : centralise les appels à l’API

- types.ts : définitions des objets Job et Candidate


### Backend (Rails)

- Modèles Job et Recruiter

- Authentification via Devise

- Base de données SQLite pour simplifier l’installation et le test

- Routes REST pour CRUD sur les jobs

J'ai gardé l'architecture classique Rails (models, controllers, migrations, routes) pour rester proche des conventions, ce qui rend le projet lisible et facilement compréhensible.

Cette architecture intègre le frontend au backend. Pour un vrai projet, il serait préférable de séparer frontend et backend en deux repos distincts.

## Prochaines étapes

Sécuriser l’application : mot de passe sécurisé, clé secrète Devise...

Ajouter des tests unitaires et d’intégration Front + Back

Ajouter des filtres et recherches avancées pour les jobs

Préparer le déploiement (Heroku / Vercel)

Séparer le frontend et backend pour un vrai projet en production

