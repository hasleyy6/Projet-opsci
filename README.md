projet_opsci\
├── BINONECH\
│   ├── Dockerfile\
│   ├── docker-compose.yml\
│   ├── .env (ce fichier est dans le gitignore pour des raisons de sécurité)\
│   └── ... (remaining strapi app files)\
└── opsci-strapi-frontend\
    ├── Dockerfile\
    └── ... (remaining front end files)\
## Instructions pour lancer le projet :

Plusieurs méthodes sont possibles :

### Méthode 1 : La plus simple ✨Docker✨

Une fois que vous avez cloné le projet sur votre machine, vous pouvez suivre ces étapes :

1. Naviguez vers le dossier BINONECH en utilisant la commande :
cd BINONECH

2. Ensuite, lancez la commande :
docker-compose up --build

Cela démarrera tous les services définis dans le fichier `docker-compose.yml`.
Cela peut prendre un peu de temps pour que tout s'exécute.

3. Une fois que c'est terminé, vous devriez voir un affichage similaire à celui-ci :
>><img width="857" alt="rdm" src="https://github.com/hasleyy6/Projet-opsci/assets/141744710/2475a0a3-b470-4a36-8a7b-9d612d97ce93">
