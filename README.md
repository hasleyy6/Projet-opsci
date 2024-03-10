
projet_opsci/
├── BINONECH/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── .env (ce fichier est dans le gitignore pour des raisons de sécurité)
│   └── ... (remaining strapi app files)
└── opsci-strapi-frontend/
    ├── Dockerfile
    └── ... (remaining front end files)

# Instructions pour lancer le projet :
Plusieurs méthodes sont possible:
## Méthode 1 : La plus simple ✨Docker✨
Une fois que vous ayez pull le projet sur votre machine, il vous suffira de vous mettre dans le dossier BINONECH grâce à la commande:
>>cd BINONECH<<
Ensuite il faut taper la commande:
>>Docker-compose up --build<<
Qui va démarrer tous les services grâce au docker-compose.yml
Ca devrait prendre un peu de temps pour que tout s'exécute.
Une fois que c'est bon, vous devrez avoir un affichage qui ressemble au suivant:
>><img width="857" alt="rdm" src="https://github.com/hasleyy6/Projet-opsci/assets/141744710/2475a0a3-b470-4a36-8a7b-9d612d97ce93">
