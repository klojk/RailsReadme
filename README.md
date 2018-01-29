# RailsReadme

#Ruby on Rails

##Sommaire
Définition
Utilisation
La différence entre un site statique et un site dynamique
Le MVC
Les routes
Les bases de données
Le concept de migration
GET / POST
Les relations entre les modèles et les BDD
Les fonctions du CRUD

###Définition

Ruby on Rails est un framework construit sur le langage Ruby, qui a été créé par Yukihiro “Matz” Matsumoto en 1995. Ruby on Rails a été créé en 2004 par David Heinemeier Hansson.
Il permet de développer des appli web dynamiques, utilisant le concept de Model View Controller.
Il propose une structure permettant de développer des sites web à parti de zéro rapidement sans avoir à écrire tous les éléments de code soi-même.
2 principes :
DRY Dont Repeat Yourself : utiliser autant que possible des éléments de l’application qu’à un seul endroit
Convention plutôt que configuration : préciser seulement les éléments de configuration qui ne respectent pas les conventions établies (en référence aux comportements par défaut proposés)


### Différences entre un site statique et site dynamique
Pour un site statique, chaque utilisateur a droit au même contenu qui ne varie pas. La page est identique pour tout le monde. Un visiteur demande une page statique, le serveur lui envoie la page demandée.
Pour développer ce type de site statique, on n’a pas besoin de coder.

En opposition avec le site dynamique qui s’adapte à ses utilisateurs. Il y a une interaction avec une base de données et le serveur. On peut prendre l’exemple d’un site d’e-commerce dynamique puisqu il demande à chaque utilisateur son login, sa sélection pour son panier, son module de recherches.
Dans ce cas, le site doit être être codé de bout en bout.

###Modèle-vue-contrôleur ou MVC
C’est un motif d’architecture logicielle destinée aux interfaces graphiqes pour les applis web. Il y a 3 types de modules aux responsabilités différentes : les modèles, les vues, les contrôleurs
-	Un modèle ( model) contenant les données à afficher
Classes assurant la gestion de données. Elles sont déterminées automatiquement par Rails, les relations entre les tables sont spécifiquement spécifiées.

-	Une vue (view) contenant la présentation de l’interface graphique, des informations à afficher pour l’utilisateur. C’est une combinaison de code HTML et Ruby dans des fichiers .html.erb.


-	Un contrôleur (controller) contenant la logique concernant les actions effectuées par l’utilisateur. Ils vont chercher les données et les mettent à disposition des vues.
« En interagissant avec une application Rails, un navigateur envoie une requête, qui est reçue par un serveur web et passée à un contrôleur Rails, qui lui-même prend en charge la suite des opérations. Ainsi le contrôleur rendra un « vue », qui est un modèle converti en HTML et renvoyé au navigateur . »
http://french.railstutorial.org/chapters/a-demo-app#sec:mvc_in_action


###Les routes
Les routes permettent d’interpréter les URL et d’orienter vers les bonnes actions des controleurs. La configuration se trouve dans le fichier config/routes.rb
« Les bases de l’option RESTful
Par défaut, les routes Rails utilisent un format décrivant le type de ressource suivi d’une action et d’un éventuel identifiant. Les verbes HTTP permettent de distinguer les comportements concernant une ressource précise :
– créer (GET/POST)
– afficher via l’ID (GET)
– modifier via l’ID (GET/PATCH)
– supprimer via l’ID (DELETE)
– lister (GET) »
###Les bases de données
Pour stocker les données , il est nécessaire d’utiliser un base de données. Elle peut être MySQL, PostgreSQL, MongoDB.
Il faut savoir que  Ruby on Rails utilise un ORM, un système transformant les tables de la base de données en version orientée objet, appelé Active Record ;Rails va simplifier le code et traduire le code pour que les requêtes se fassent sur la base de données.



###Le concept de migration
Dans une migration, on liste les tables et colonnes à créer (ou supprimer). Pour notre application, voici ce que nous devons ajouter à ce fichier :

