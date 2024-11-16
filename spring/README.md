# API REST MaBanque avec Spring Boot

Ce projet Spring Boot implémente une API REST pour la gestion de comptes bancaires. Il utilise Spring Data JPA pour la persistance des données avec H2 Database (en mémoire), Spring Web pour exposer les endpoints REST, et Lombok pour simplifier le code. L'API prend en charge les formats JSON et XML et est documentée avec Swagger UI.

## Fonctionnalités

L'API propose les fonctionnalités CRUD suivantes pour la gestion des comptes :

* **Créer un compte:**  POST `/banque/comptes`
* **Lire tous les comptes:** GET `/banque/comptes`
* **Lire un compte par ID:** GET `/banque/comptes/{id}`
* **Mettre à jour un compte:** PUT `/banque/comptes/{id}`
* **Supprimer un compte:** DELETE `/banque/comptes/{id}`


## Technologies utilisées

* **Spring Boot:** Framework pour la création d'applications Spring autonomes.
* **Spring Data JPA:**  Simplifie l'accès aux données avec JPA.
* **H2 Database:** Base de données en mémoire pour le développement.
* **Lombok:**  Réduit le code passe-partout (getters, setters, etc.).
* **Jackson:**  Sérialisation/désérialisation JSON et XML.
* **Springdoc OpenAPI/Swagger UI:** Documentation interactive de l'API.


## Configuration

* La configuration de la base de données H2 et du port du serveur se trouve dans le fichier `application.properties`.
* L'API est configurée pour démarrer sur le port 8082.
* La console H2 est activée et accessible à l'adresse `/h2-console`.

## Exécution du projet

1. **Cloner le projet :** `git clone <URL du projet>`
2. **Compiler et exécuter :** `mvn spring-boot:run`

## Accès à la documentation Swagger UI

Une fois l'application démarrée, accédez à la documentation Swagger UI à l'adresse suivante :

`http://localhost:8082/swagger-ui.html`


## Utilisation de l'API

Vous pouvez utiliser des outils comme Postman, Curl ou SoapUI pour interagir avec l'API.  Les requêtes doivent spécifier le format de données souhaité (JSON ou XML) via les en-têtes `Accept` (pour la réponse) et `Content-Type` (pour la requête).  Des exemples d'utilisation avec Curl sont inclus dans la documentation originale (pages 183-184).


## Structure du projet

Le projet est structuré comme suit :

* **`ma.rest.spring.entities`:** Contient les entités JPA (Compte, TypeCompte).
* **`ma.rest.spring.repositories`:** Contient les interfaces de dépôt JPA (CompteRepository).
* **`ma.rest.spring.controllers`:** Contient les controllers REST (CompteController).
* **`MaBanqueApplication.java`:** Classe principale de l'application.


## Améliorations possibles

* **Gestion des erreurs plus robuste:** Implémenter une gestion des erreurs plus fine avec des codes d'erreur et des messages plus précis.
* **Validation des données:** Ajouter des contraintes de validation aux entités pour garantir l'intégrité des données.
* **Sécurité:**  Sécuriser l'API avec une authentification et une autorisation appropriées.
* **Tests unitaires et d'intégration:** Ajouter des tests pour garantir la qualité du code et la fiabilité de l'API.



## Démonstartion

https://github.com/user-attachments/assets/ca137f19-1aa7-413f-92e0-3d543676895f
