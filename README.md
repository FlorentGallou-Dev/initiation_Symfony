# Rendu des exercice d'Initiation au framework Symfony
-----
> Semaine 18 de ma formation de Développeur d'application Web et web modile, j'ai la semaine pour m'initier aux principes de bases du Framework Symfony en utilisant la documentation fourni sur le site symfony.com, cette mise en situation intervient après la session passée sur le développement POO en PHP natif qui m'a appri à comprendre le nécessaire à l'utilisation du Framework Symfony.
-----

## Déploiement
-----
> 1. L'environnement :
> > 1. Installer Apache2 - sudo apt-get install apache2
> > 2. Installer PHP minimum 7.2 - sudo apt-get install php7.4
> > 3. Installer Apache2 - sudo apt-get install libapache2-mod-php
> > 4. Installer le lien PHP / Mysql - sudo apt-get install php-mysql
> > 5. Installer Mysql serveur - sudo apt-get install mysql-server
> > 6. Sécuriser Mysql - mysql_secure_installation -> initialiser le mot de passe du root et sécuriser les accès
> > > 1. Encoder le mot de passe de root :
> > > > 1. Démarrer mysql - sudo mysql
> > > > 2. Lancer la commande sql pour chiffre le mot de passe : - ALTER USER 'root'@'localhost' IDENTIFIED WITH chaching_sha2_password BY 'motdepasse'; <- Mot de passe doit respecter le niveau de sécurité choisi lors de l'initialisation de mysql_secure_installation
> > > 2. Elever les droits de root :
> > > > 1. Démarrer mysql - mysql -u root -p <- utiliser le nouveau mot de passe fraichement encodé
> > > > 2. lancer la commande sql pour élever les droit de root : - GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' WITH GRANT OPTION;
> > 7. Créer un base de données pour la connecter au projet Symfony :
> > > > 1. Démarrer mysql - mysql -u root -p
> > > > 2. lancer la commande sql pour créer une base de données : - CREATE DATABASE nombasededonnees CHARACTER SET 'utf8';
> > 8. Installer Composer ATTENTION LA VERSION 2 MINIMUM EST NECESSAIRE POUR UTILISER ANNOTATIONS :
> > > > 1. php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
> > > > 2. php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
> > > > 3. php composer-setup.php --version2.1.3
> > > > 4. php -r "unlink('composer-setup.php');"
> 2. Installation du framework Symfony : 
> > 1. Installer les binary de symfony - sudo wget https://get.symfony.com/cli/installer -O - | bash
> > 2. Vérifier que l'environnement est prèt pour symfony - symfony check:requirements
> > 3. Déployer symfony dans un nouveau projet (dans le dossier des projets) - sudo symfony new nom_de_projet <- L'installation de symfony simple sans plugin superflu
> > 4. Démarrer Symfony - symfony server:start
-----