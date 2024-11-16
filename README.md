# RestfulAPI-TP
# Projets Spring Boot : MaBanque et Gestion des étudiants

Ce README décrit deux projets Spring Boot distincts : MaBanque, une API REST pour la gestion de comptes bancaires, et un système de gestion des étudiants.

## Projet 1 : MaBanque - API REST pour la gestion de comptes

Ce projet fournit une API REST pour gérer les comptes bancaires, utilisant une base de données H2 en mémoire pour le développement.

**Fonctionnalités:**

* **Créer un compte :** `POST /banque/comptes`  (Corps de la requête : JSON/XML représentant l'objet Compte)
* **Lire tous les comptes :** `GET /banque/comptes` (Accepte : application/json ou application/xml)
* **Lire un compte par ID :** `GET /banque/comptes/{id}` (Accepte : application/json ou application/xml)
* **Mettre à jour un compte :** `PUT /banque/comptes/{id}` (Corps de la requête : JSON/XML représentant les modifications)
* **Supprimer un compte :** `DELETE /banque/comptes/{id}`


**Structure du projet:**

* `ma.rest.spring.entities`: Contient les entités JPA (`Compte`, `TypeCompte`).
* `ma.rest.spring.repositories`: Contient l'interface du repository JPA (`CompteRepository`).
* `ma.rest.spring.controllers`: Contient le contrôleur REST (`CompteController`).
* `MaBanqueApplication.java`: Classe principale de l'application.

**Configuration:**

* Le fichier `application.properties` configure la source de données H2, le port du serveur (8082) et active la console H2 (`/h2-console`).
* L'annotation `@RestController` combine `@Controller` et `@ResponseBody` pour simplifier le développement REST.
*  L'annotation `@RequestMapping("/banque")` définit le chemin de base pour tous les endpoints.

**Exécution:**

1. `mvn spring-boot:run`
2. Accéder à Swagger UI : `http://localhost:8082/swagger-ui.html`
3. Accéder à la console H2 : `http://localhost:8082/h2-console`


### Premiere demonstartion

https://github.com/user-attachments/assets/ca137f19-1aa7-413f-92e0-3d543676895f



## Projet 2 : Gestion des étudiants

Ce projet fournit une API REST pour gérer les informations des étudiants, utilisant une base de données MySQL.

**Fonctionnalités:**

* **Ajouter un étudiant :** `POST /students/save` (Corps de la requête : JSON représentant l'objet Student)
* **Supprimer un étudiant :** `DELETE /students/delete/{id}`
* **Récupérer tous les étudiants :** `GET /students/all`
* **Compter le nombre total d'étudiants :** `GET /students/count`
* **Compter le nombre d'étudiants par année de naissance :** `GET /students/byYear`

**Structure du projet:**

* `com.example.student_management.entities`: Contient l'entité JPA (`Student`).
* `com.example.student_management.repositories`: Contient l'interface du repository (`StudentRepository`).
* `com.example.student_management.services`: Contient la logique métier (`StudentService`).
* `com.example.student_management.controllers`: Contient le contrôleur REST (`StudentController`).
* `StudentManagementApplication.java`: Classe principale de l'application.
* `src/test/java`: Contient les tests unitaires pour `StudentController`.

**Configuration:**

* Le fichier `application.properties` configure la connexion à la base de données MySQL.  Il est crucial de créer la base de données `studentdb` et de configurer l'URL, le nom d'utilisateur et le mot de passe correctement.
*  L'annotation `@Repository` sur `StudentRepository` active la gestion des exceptions Spring pour les opérations de base de données.


**Exécution:**

1. Créer la base de données MySQL `studentdb`.
2. Configurer la connexion à la base de données dans `src/main/resources/application.properties`.
3. `mvn spring-boot:run`
4. Accéder à Swagger UI : `http://localhost:8080/swagger-ui.html`

**Tests unitaires:**

`mvn test`


### Deuxieme démonstartion

https://github.com/user-attachments/assets/5a7e3a18-a7cc-4dfa-9e60-fa50f349955e


Ce README combiné fournit une vue d'ensemble des deux projets. Reportez-vous aux fichiers README individuels de chaque projet pour des informations plus détaillées.
