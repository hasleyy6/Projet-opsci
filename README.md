# Projet OPSCI - Rendu Projet intermiédaire pour la matière pour l'UE OpsCi 
AIJJOU Bayane 21113693
BENNIS NECHBA Mohamed 28706175

#### Lien de la vidéo de présentation: 
https://youtu.be/SCVjgfgoOw0
### Ce projet vise à créer et déployer une application composée de :

-Un serveur Strapi : servant de backend à notre application\
-PostgreSQL : utilisé comme base de données pour Strapi, afin de stocker les informations\
-Un projet React : servant de frontend à notre application
# Structure du projet :
Projet_opsci\
├── BINONECH\
│   ├── Dockerfile\
│   ├── docker-compose.yml\
│   ├── .env (ce fichier est dans le gitignore pour des raisons de sécurité)\
│   └── ... (remaining strapi app files)\
└── opsci-strapi-frontend\
    ├── Dockerfile\
    └── ... (remaining front end files)
## Instructions pour lancer le projet :

Plusieurs méthodes sont possibles :

### La méthode la plus simple ✨Docker✨

Une fois que vous avez cloné le projet sur votre machine, vous pouvez suivre ces étapes :

1. Naviguez vers le dossier BINONECH en utilisant la commande :
>>cd BINONECH

2. Ensuite, lancez la commande ci dessous, Cela démarrera tous les services définis dans le fichier `docker-compose.yml`.
Ce qui peut prendre un peu de temps pour que tout s'exécute.
>>docker-compose up --build


3. Une fois que c'est terminé, vous devriez voir un affichage similaire à celui-ci :
>><img width="857" alt="rdm" src="https://github.com/hasleyy6/Projet-opsci/assets/141744710/2475a0a3-b470-4a36-8a7b-9d612d97ce93">

4.Vous accédez finalement à l'application React à l'adresse http://localhost:5173, comme défini via le champ EXPOSE dans le Dockerfile

5. Vous avez aussi accès au pannel administrateur à l'adresse http://localhost:1337/admin, les produits que vous créerez seront visible au front end.

### Arrêt
>>Docker-compose down

## Containers used in this project:
#### Strapi:
-Container name : Strapi
-DATABASE_NAME: strapi-pg
-DATABASE_USERNAME: strapi
-DATABASE_PASSWORD: safepassword
-ports: 1337:1337
-networks:strapi
depends_on:- strapiDB

#### StrapiDB
-container_name: strapiDB
-ports:5432:5432
-networks:strapi
-POSTGRES_USER: strapi
-POSTGRES_PASSWORD: safepassword
-POSTGRES_DB: strapi-pg

#### front end
container_name: frontend
ports:5173:5173
depends_on:strapiDB,strapi,dump
-networks:strapi

# Clap de fin
Voilà, normalement vous avez accès au frontend avec les produits demandés. Merci d'avoir tout suivi!!

