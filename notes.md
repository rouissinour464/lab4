1. Quel est le but de l’annotation @Entity et son lien avec les tables de base de données ?
L’annotation @Entity indique que la classe Java correspond à une table dans la base de données. Chaque attribut
de la classe représente une colonne dans cette table. Lors du démarrage de l’application, Spring Boot et Hibernate
détectent les classes marquées avec @Entity et créent automatiquement les tables ou les mettent à jour dans la base de données,
en fonction de la configuration choisie.
2. Que se passe-t-il lorsque Spring Data JPA rencontre une méthode comme findByMajor(String major) ?
Lorsque Spring Data JPA détecte une méthode comme findByMajor, il analyse automatiquement le nom de la méthode pour 
générer la requête SQL correspondante. Il n'est pas nécessaire d'écrire manuellement la requête : Spring comprend que 
l'on veut récupérer les étudiants dont la spécialité correspond à la valeur fournie en paramètre.

3. Comment Spring Boot sait-il comment se connecter à votre base de données PostgreSQL ?
Spring Boot utilise un fichier de configuration appelé application.properties (ou application.yml) 
où sont définis l'URL de la base de données, le nom d'utilisateur et le mot de passe. Lors du démarrage,
Spring lit ces paramètres et configure automatiquement la connexion à la base de données PostgreSQL, sans 
besoin d'intervention supplémentaire de la part du développeur.
4. Quelle est la différence entre spring.jpa.hibernate.ddl-auto=update et spring.jpa.hibernate.ddl-auto=create ?
La configuration update permet de modifier la structure des tables existantes pour s'adapter aux nouvelles entités 
sans effacer les données existantes, ce qui est pratique pour le développement. En revanche, la configuration create 
supprime toutes les tables existantes et les recrée à partir de zéro à chaque démarrage, ce qui entraîne la perte de toutes
les données, mais peut être utile lors de tests ou de réinitialisations de projet.

