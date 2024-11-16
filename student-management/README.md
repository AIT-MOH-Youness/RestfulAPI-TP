# Gestion des étudiants avec Spring Boot

Ce projet Spring Boot fournit une API REST pour gérer les informations des étudiants. Il utilise Spring Data JPA pour interagir avec une base de données MySQL, Spring Web pour exposer les endpoints REST, et est livré avec des tests unitaires utilisant JUnit et Mockito.  La documentation de l'API est générée automatiquement avec Swagger UI.

## Fonctionnalités

L'API offre les fonctionnalités suivantes :

* **Ajouter un étudiant :** POST `/students/save`
* **Supprimer un étudiant :** DELETE `/students/delete/{id}`
* **Récupérer tous les étudiants :** GET `/students/all`
* **Compter le nombre total d'étudiants :** GET `/students/count`
* **Compter le nombre d'étudiants par année de naissance :** GET `/students/byYear`

## Technologies utilisées

* **Spring Boot:** Framework pour simplifier le développement d'applications Spring.
* **Spring Data JPA:** Simplifie l'interaction avec la base de données en utilisant JPA.
* **MySQL:** Système de gestion de base de données relationnelle.
* **Spring Web:**  Pour créer des applications web et RESTful.
* **Spring Boot DevTools:**  Facilite le redémarrage à chaud et le rechargement du code pendant le développement.
* **Spring Validation:** Pour valider les données d'entrée.
* **Spring Data REST:** Expose automatiquement les repositories Spring Data JPA en tant qu'endpoints REST.
* **JUnit 5:** Framework pour les tests unitaires.
* **Mockito:** Framework pour le moquage d'objets lors des tests.
* **Swagger UI:** Documentation interactive de l'API.

## Configuration

* Les paramètres de connexion à la base de données MySQL (URL, nom d'utilisateur, mot de passe) sont configurés dans le fichier `application.properties`.  Assurez-vous de créer une base de données nommée `studentdb` avant de lancer l'application.
* Le fichier `application.properties` est situé dans le répertoire `src/main/resources`.

## Exécution du projet

1. **Cloner le projet :** `git clone https://github.com/AIT-MOH-Youness/RestfulAPI-TP.git`
2. **Changer le répertoire :** `cd student-management`
3. **Compiler et exécuter :** `mvn spring-boot:run`

## Accès à la documentation Swagger UI

Après avoir démarré l'application, accédez à Swagger UI pour explorer et tester l'API :

`http://localhost:8080/swagger-ui.html`

## Tests unitaires

Des tests unitaires pour le contrôleur `StudentController` sont inclus dans le projet. Ils utilisent Mockito pour simuler le comportement du service `StudentService`.  Pour exécuter les tests, utilisez la commande Maven suivante :

`mvn test`

## Structure du projet

* **`com.example.student_management.entities`:** Contient les entités JPA (Student).
* **`com.example.student_management.repositories`:** Contient les interfaces de dépôt (StudentRepository).
* **`com.example.student_management.services`:** Contient la logique métier (StudentService).
* **`com.example.student_management.controllers`:** Contient les contrôleurs REST (StudentController).
* **`StudentManagementApplication.java`:** Classe principale de l'application.
* **`src/test/java`:** Contient les tests unitaires.


## Améliorations possibles

* **Gestion des erreurs plus robuste :** Implémenter une gestion des erreurs plus spécifique avec des codes d'erreur et des messages personnalisés.
* **Validation des données :**  Ajouter des annotations de validation (e.g., `@NotNull`, `@Size`, `@Email`) aux champs de l'entité `Student`.
* **Sécurité :**  Sécuriser l'API avec une authentification et une autorisation appropriées.
* **Pagination :**  Implémenter la pagination pour les requêtes qui retournent une grande quantité de données.


## Démostration

https://github.com/user-attachments/assets/5a7e3a18-a7cc-4dfa-9e60-fa50f349955e
