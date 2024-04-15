Application de Gestion de Contacts
Cette application web développée en Spring Boot permet de gérer un carnet d'adresses. Elle offre la possibilité d'ajouter, de lister, de modifier et de supprimer des contacts à travers une interface web simple.

Fonctionnalités
Ajouter un contact : Permet d'insérer les informations d'un nouveau contact dans la base de données.
Afficher la liste des contacts : Tous les contacts sont listés avec leurs informations détaillées.
Supprimer un contact : Permet de retirer un contact de la base de données.
Technologies Utilisées
Spring Boot : Pour le framework de l'application.
Thymeleaf : Pour le moteur de template HTML.
Spring Data JPA : Pour la persistance des données.
H2 Database : Base de données en mémoire utilisée pour le développement et les tests.
Configuration Requise
Java 11 ou supérieur.
Maven 3.6 ou supérieur.
Installation
Cloner le dépôt

bash
Copy code
git clone https://github.com/votreUsername/nomDuDepot.git
cd nomDuDepot
Compiler le projet

bash
Copy code
mvn clean install
Exécuter l'application

bash
Copy code
mvn spring-boot:run
L'application sera accessible à l'adresse http://localhost:8080/.

Intégration avec Jenkins
Prérequis pour Jenkins
Jenkins 2.x avec les plugins suivants installés :
Maven Integration plugin
Git plugin
Configuration de Jenkins
Créer un nouveau job

Allez dans Jenkins Dashboard.
Cliquez sur "Nouveau Item".
Sélectionnez "Freestyle project" et entrez un nom pour votre projet.
Cliquez sur "OK".
Configurer le source code management

Sélectionnez "Git".
Entrez l'URL du dépôt Git.
Configurez les credentials si nécessaire.
Configurer la construction

Dans la section "Build", cliquez sur "Ajouter une étape de build".
Sélectionnez "Invoke top-level Maven targets".
Dans "Goals", entrez clean install.
Exécuter l'application après le build

Ajoutez une nouvelle étape de build.
Sélectionnez "Execute shell".
Tapez mvn spring-boot:run.
Sauvegarder et exécuter le build

Cliquez sur "Save".
Cliquez sur "Build Now" pour démarrer le processus de build.
Visualisation des résultats
Console Output : Vous pouvez visualiser la sortie de console pour vérifier le déroulement du build.
Rapports de test : Si configuré, Jenkins peut générer et afficher les rapports des résultats des tests.
