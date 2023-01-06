# git-cheatsheet
Cours de l'ESGI

# Github

GitHub est un service en ligne qui permet à des développeurs de stocker et de suivre les versions de leur code source. C'est un outil très utile pour le travail en équipe sur un projet de développement de logiciel, car il permet à plusieurs personnes de travailler sur le même code en même temps et de suivre les changements apportés au fil du temps.

GitHub utilise Git, un logiciel de contrôle de version, pour gérer le suivi des changements apportés au code. Chaque fois qu'un développeur modifie le code, il peut utiliser Git pour enregistrer ces changements (ce que l'on appelle "committer" les changements). Les développeurs peuvent également "pusher" leurs changements sur GitHub, ce qui permet de les partager avec d'autres membres de l'équipe.

GitHub offre également de nombreuses autres fonctionnalités, telles que la gestion des tâches, la documentation du projet, et l'intégration avec d'autres services populaires. C'est devenu une plateforme de développement de logiciel incontournable pour de nombreuses équipes à travers le monde.

# Les commandes de base

Voici quelques commandes de base de Git que vous pouvez utiliser dans votre terminal ou invite de commandes:
```
git init: initialise un nouveau dépôt Git dans le répertoire courant
git clone : permet de cloner un dépôt Git sur votre ordinateur. Exemple : git clone https://github.com/user/repo.git
git status : permet de voir l'état des fichiers dans le dépôt, c'est-à-dire les fichiers modifiés, ajoutés mais non commités, etc. Exemple : git status
git add : permet d'ajouter des fichiers à l'index de Git. Exemple : git add file.txt
git commit : permet de faire un commit des changements ajoutés à l'index. Exemple : git commit -m "Ajout d'un fichier texte"
git push : permet d'envoyer les commits vers le dépôt distant. Exemple : git push origin main
git pull : permet de récupérer les derniers changements du dépôt distant et de les fusionner avec votre dépôt local. Exemple : git pull origin main
git merge: fusionne les branches dans votre dépôt
git status : permet de voir l'état des fichiers dans le dépôt, c'est-à-dire les fichiers modifiés, ajoutés mais non commités, etc. Exemple : git status
git show: affiche les modifications apportées à un fichier
git fork: crée une copie de votre dépôt sur votre propre compte GitHub
```

Voici quelques commandes de GitHub que vous pouvez utiliser sur la plateforme en ligne:

```
git branch : permet de gérer les branches dans un dépôt Git. Vous pouvez créer une nouvelle branche avec git branch nouvelle-branche, changer de branche avec git checkout nouvelle-branche, ou afficher la liste des branches avec git branch.

git branch _d <nom>: supprime une branche dans votre dépôt (sur GitHub)

git merge : permet de fusionner une branche dans une autre. Par exemple, pour fusionner la branche nouvelle-fonctionnalite dans la branche main, vous pouvez utiliser la commande git merge nouvelle-fonctionnalite.

git checkout: bascule entre les branches dans votre dépôt (sur GitHub)

git reset <id>: annule les modifications apportées à un fichier
git revert <id>: annule les modifications apportées à un fichier
git rebase: fusionne les modifications d'une autre branche dans votre branche active

```
