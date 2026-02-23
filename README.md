# TP 3 : Lier Salle–Réservation–Utilisateur, ajouter Équipement (ManyToMany), expérimenter cascade et suppression orpheline

Ce projet implémente un système de gestion de réservations de salles. L'objectif était de mettre en pratique la persistance de données en Java via l'API JPA et l'implémentation Hibernate.

##  Travail Réalisé

### 1. Modélisation des Entités (ORM)
J'ai conçu quatre entités principales avec leurs annotations JPA :
- **Utilisateur** : Gestion des informations personnelles et lien avec les réservations.
- **Salle** : Caractéristiques des espaces disponibles.
- **Reservation** : Entité pivot gérant les dates et les motifs.
- **Equipement** : Matériel associé aux salles.

### 2. Gestion des Relations
Le TP m'a permis de configurer différents types de relations :
- **OneToMany / ManyToOne** : Entre l'Utilisateur et ses Réservations.
- **ManyToMany** : Entre les Salles et les Équipements (via une table de jointure).
- **Opérations en Cascade** : Utilisation de `CascadeType.ALL` pour simplifier la persistance des objets liés.
- **Orphan Removal** : Suppression automatique des réservations détachées.

### 3. Configuration & Persistance
- Utilisation de la base de données **H2** (en mémoire).
- Configuration via le fichier `persistence.xml` (Dialecte H2, Driver, et stratégie `create-drop`).

---

##  Résultats et Captures d'écran

### ✅ Structure du Projet
L'organisation du code suit les standards Maven avec une séparation claire entre les modèles et la logique applicative.

<img width="313" height="363" alt="structuredeproject" src="https://github.com/user-attachments/assets/263ce173-faa9-4da5-9f28-53ebf5a16eb2" />


### ✅ Exécution des tests
Voici le résultat obtenu dans la console lors de l'exécution de la classe `App.java`. On y voit la création des tables et le succès des opérations de persistance :


<img width="697" height="251" alt="1" src="https://github.com/user-attachments/assets/513d9c97-4815-4c4e-8d0a-ec6bbfd7809f" />

<img width="1588" height="604" alt="image" src="https://github.com/user-attachments/assets/129c0d7d-a7b9-4c75-9ca7-2525f2fdc829" />

<img width="1128" height="532" alt="image" src="https://github.com/user-attachments/assets/fed7760b-f345-4bea-a0fb-97d9eec8ca24" />

<img width="1212" height="443" alt="image" src="https://github.com/user-attachments/assets/249716c0-32fb-42d6-9d58-6b2ba6d1e1ef" />

<img width="1499" height="556" alt="image" src="https://github.com/user-attachments/assets/28ab7677-acdd-4d53-9d43-8c7c29f23935" />

<img width="1006" height="322" alt="image" src="https://github.com/user-attachments/assets/281ebcd4-b1b5-4bbd-8d24-8282d9c8fa21" />

<img width="1405" height="513" alt="image" src="https://github.com/user-attachments/assets/e6e8d4a4-bbfe-4bf8-a02a-6e0c8efe260e" />


<img width="1295" height="593" alt="image" src="https://github.com/user-attachments/assets/435a2b30-454b-4a40-931e-960968f7d5a6" />

<img width="1308" height="602" alt="image" src="https://github.com/user-attachments/assets/eaa0b889-6410-4d0f-87ae-595af0588578" />

<img width="1202" height="546" alt="image" src="https://github.com/user-attachments/assets/7f696fa1-e759-4c99-8d2f-e73b49055c2b" />

<img width="982" height="465" alt="image" src="https://github.com/user-attachments/assets/c8318d2f-b73b-468d-add9-01e8bdd746bc" />

<img width="1069" height="510" alt="image" src="https://github.com/user-attachments/assets/6fe3e78a-b55a-453a-926e-124c699c1507" />

<img width="1027" height="576" alt="image" src="https://github.com/user-attachments/assets/3667576b-05cd-422b-a1fb-35d3c2a5893d" />

<img width="1175" height="596" alt="image" src="https://github.com/user-attachments/assets/6500e053-8150-4cff-b81f-fe499c63f640" />

<img width="1278" height="615" alt="image" src="https://github.com/user-attachments/assets/5b570a8b-2b04-449f-a30f-639237cd8f98" />

<img width="1257" height="529" alt="image" src="https://github.com/user-attachments/assets/9f9eba3e-a7af-4f00-8d0c-7893deae8c8d" />

Process finished with exit code 0.





















