# MGL7130

## Configuration de l'environnement de travail avec Ionic, Git et Github

Placez-vous dans un repertoire de travail puis entrez les commandes suivantes :
$ ionic start Simplyk blank
A la question de la création d'un compte ionic.io répondez non. Vous pouvez le faire plus tard si vous voulez.
$ cd Simplyk
$ cd www
$ git init .
$ git remote add -t \* -f origin https://github.com/Warlot-PQ/MGL7130.git
$ rm -Rf css/ img/ js/ index.html
$ git checkout master

L'environnement ionic est prêt et le lien avec GitHub est établi.

## Configuration du live reload

Placez-vous dans le repertoire Simplyk.

Ajouter un watcher au fichier ionic.project pour que le live reload soit actif sur d'autres fichiers que sur index.html.

Exemple ionic.project :
{
  "name": "Simplyk",
  "app_id": "",
  "watchPatterns": [
    "www/js/*",
    "!www/css/**/*"
  ]
}

Lancer le serveur simulant les appareils android et IOS :

$ ionic serve --lab

## Déploiement sur téléphone par l'application Ionic View

$ ionic login
$ ionic upload
