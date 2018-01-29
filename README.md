# RailsReadme

#Ruby on Rails


##Introduction

Ruby on Rails est un framework construit sur le langage Ruby, qui a été créé par Yukihiro “Matz” Matsumoto en 1995. Ruby on Rails a été créé en 2004 par David Heinemeier Hansson.
Il permet de développer des appli web dynamiques, utilisant le concept de Model View Controller.
Il propose une structure permettant de développer des sites web à parti de zéro rapidement sans avoir à écrire tous les éléments de code soi-même.
2 principes :
DRY Dont Repeat Yourself : utiliser autant que possible des éléments de l’application qu’à un seul endroit
Convention plutôt que configuration : préciser seulement les éléments de configuration qui ne respectent pas les conventions établies (en référence aux comportements par défaut proposés)
### Différences entre un site statique et site dynamique
Pour un site statique, chaque utilisateur a droit au même contenu qui ne varie pas. La page est identique pour tout le monde. Un visiteur demande une page statique, le serveur lui envoie la page demandée.
Pour développer ce type de site statique, on n’a pas besoin de coder.

En opposition avec le site dynamique qui s’adapte à ses utilisateurs. Il y a une interaction avec une base de données et le serveur. On peut prendre l’exemple d’un site d’e-commerce dynamique puisqu’il demande à chaque utilisateur son login, sa sélection pour son panier, son module de recherches.
Dans ce cas, le site doit être codé de bout en bout.

###Modèle-vue-contrôleur ou MVC
C’est un motif d’architecture logicielle destinée aux interfaces graphiqes pour les applis web. Il y a 3 types de modules aux responsabilités différentes : les modèles, les vues, les contrôleurs
-	Un modèle (model) contenant les données à afficher
Classes assurant la gestion de données. Elles sont déterminées automatiquement par Rails, les relations entre les tables sont spécifiquement spécifiées.

-	Une vue (view) contenant la présentation de l’interface graphique, des informations à afficher pour l’utilisateur. C’est une combinaison de code HTML et Ruby dans des fichiers .html.erb.


-	Un contrôleur (controller) contenant la logique concernant les actions effectuées par l’utilisateur. Ils vont chercher les données et les mettent à disposition des vues.
« En interagissant avec une application Rails, un navigateur envoie une requête, qui est reçue par un serveur web et passée à un contrôleur Rails, qui lui-même prend en charge la suite des opérations. Ainsi le contrôleur rendra un « vue », qui est un modèle converti en HTML et renvoyé au navigateur . »
http://french.railstutorial.org/chapters/a-demo-app#sec:mvc_in_action


###Les routes
Les routes permettent d’interpréter les URL et d’orienter vers les bonnes actions des contrôleurs. La configuration se trouve dans le fichier config/routes.rb


###Les bases de données
Pour stocker les données , il est nécessaire d’utiliser un base de données. Elle peut être MySQL, PostgreSQL, MongoDB.
Il faut savoir que  Ruby on Rails utilise un ORM, un système transformant les tables de la base de données en version orientée objet, appelé Active Record ;Rails va simplifier le code et traduire le code pour que les requêtes se fassent sur la base de données.



###Le concept de migration
Comment exécuter une migration ?
La commande bin/rails generate model créée un fichier de migration de base de données dans le répertoire db/migrate. Les migrations sont des classes Ruby conçues pour faciliter la création et la modification de tables de base de données. Rails utilise des commandes rake pour exécuter des migrations, et il est possible d'annuler une migration après qu'elle a été appliquée à votre base de données. Les noms de fichiers de migration incluent un horodatage pour s'assurer qu'ils sont traités dans l'ordre dans lequel ils ont été créés.


###GET / POST
Méthode
La méthode, parfois appelée "verbe" ou "action", indique au serveur ce que le client veut qu'il fasse. 

GET -cela permet d’avoir des informations sur l'élément identifié par l'URI. Comme les requêtes GET demandent toutes des informations, elles ne sont pas autorisées à avoir des corps de requête. Vous avez toujours la chaîne de requête URI à votre disposition si vous devez envoyer des données du client au serveur sur une requête GET.

POST – cela permet d'ajouter une entité en tant qu'enfant de l'objet identifié par l'URI. L'entité que le client s'attend à ce que le serveur ajoute soit transmise dans le corps de la demande
L'action POST fonctionne presque de la même manière que la requête GET, à l'exception de la « payload 


###Les relations entre les modèles et les BDD

Qu'est-ce que BDD (Behaviour-Driven Development) BDD étend le développement piloté par les tests en écrivant des cas de test d'une manière compréhensible pour tout le monde. Avec l'aide de BDD, le développement de logiciels est géré à la fois par des intérêts commerciaux et des connaissances techniques. Il concentre et associe les spécifications comportementales à chaque unité de logiciel en développement. 
Il étend les tests TDD en écrivant des cas de test dans un langage naturel que les non-programmeurs peuvent lire. En d'autres termes, c'est comme écrire une histoire. La principale chose à savoir est que BDD est destiné à éliminer les problèmes que TDD pourrait causer. Outils à utiliser: Quelques gemmes populaires sont disponibles pour implémenter BDD dans Rails sont rpsec-rails, factory_girl_rails, 
rpsec-rails, factory_girl_rails, cucumber-rails, guard-cucumber, mocha etc

###Les fonctions du CRUD
Le terme CRUD est étroitement lié avec la gestion des données numériques. Plus précisément, CRUD est un acronyme des noms des quatre opérations de base de la gestion de la persistance des données et applications :
•	Create (créer)
•	Read ou Retrieve (lire)
•	Update (mettre à jour)
•	Delete ou Destroy (supprimer)
Plus simplement, le terme CRUD résume les fonctions qu’un utilisateur a besoin d’utiliser pour créer et gérer des données. Divers processus de gestion des données sont basés sur CRUD, cependant les opérations sont spécifiquement adaptées aux besoins des systèmes et des utilisateurs, que ce soit dans la gestion des bases de données ou pour l’utilisation des applications. Ainsi, les opérations sont des outils d’accès classiques et indispensables avec lesquels les experts, peuvent par exemple vérifier les problèmes de base de données. Tandis que pour un utilisateur, CRUD signifie la création d’un compte (create), l’utilisation à tout moment (read), la mise à jour (update) ou encore la suppression (delete). 



