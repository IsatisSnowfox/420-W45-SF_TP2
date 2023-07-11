# 420-W45-SF_TP2

**Date :** 2023-07-11

**Adresse du dépôt :** [Depot TP2](https://github.com/IsatisSnowfox/420-W45-SF_TP2)

Installation d'un système de containers selon une description.
- l'installation d'un système de conteneur en respectant la procédure et les recommandations du manufacturier au besoin;
- configurer le système de conteneurs en fonction d’une utilisation sécuritaire;
- vérifier que les éléments installés fonctionnent comme prévu;
- configurer des règles de gestions des accès sécuritaires.

## Section 1 : Vérification et conteneur

### Étape 1 : Vérification de l'installation

- Docker Engine et Docker compose sont installés [Confirmation de l'installation docker et docker compose](img/docker-version.png) 

### Étape 2 : création de conteneurs

docker network create mon_reseau

docker container run --name apache --network mon_reseau -p 8080:80 -d httpd:alpine

docker container run--name mongodb --network mon_reseau -v mongodb -d -e MONGO_INITDB_ROOT_USERNAME=adminmongo -e MONGO_INITDB_ROOT_PASSWORD=EncoreUneAutreBD mongo:latest

docker network inspect mon_reseau [Vérification du lien des conteneurs au réseau](img/docker-network-inspect.png)

docker logs mongodb | grep mongoadmin [Création de l'utilisateur mongoadmin dans les logs](img/mongoadmin-creation-logs.png)

## Partie Bootstrap
[Bootstrap installé](img/bootstrap-working.png)