# git-cheatsheet
Cours de l'ESGI 
Le versionning est un projet logiciel qui a pour but final d'ecrire des programmes c'est à dire du texte.
L'idée est de l'idee est de sauvegarder des informations afin de pouvoir s'y referer en cas d'erreurs, beugs ou oublis.

Les principaux avantes sont donc listés comme suite : 
- La sauvegarde de version
- La sauvegarde de l'historique des versions
- L'agnostique vis à vis du langage
- Gerer du texte
- L'aide au passage d'une version à une autre (livraison fluide des modifications sans que ça soit lourd)
- Cela facilite également la collaboration et sert à resoudre facilement les conflits
permet de passer facilement d'une version à une autre à l'aide  de la 

systemme de gestion de versiondans le git on ne met que le code source, pas le compilé ni tout ce qui tourne autour
 on distingue plusieurs
 
 - le systeme centralisé : tout part du serveur qui gere les historique en local sur notre ordinateur qui lui est allimenté par les ficher qu'on peut stocker 
 - git est un systeme distribué mais quand meme centralisé
 une copie de l'historique des versions est disponible localement
 possibilité de travailler sans latence et hors ligne
 possibilte de modifier le local avant de le lancer sur le server
 distribué mais pas centralisé
 server populaire : git hub et git lab
 
 
 on eut eglement utiliser github desktop comme interface graphique
 integration plutard dans l'IDE  visual studio
 
 pratique
 1- initaliser un depot pour notre projet : git init
 git status : affiche les fichiers qui ont changé depuis la dernière version
 git commit prend tous les fichiers dans la zone d'index et les ajoute pour de bon dans le git
 git add <fichier>  : pour ajouter un fichierun commit  est une nouvelle version, cest une unité de travailler
 
 
 
 
 
 working directory[a la creation du fichier]=> [lorqu'on utilise la commande add]stage(index)=>[lorsqu'on utilise le comit]history
 a chaque fois qu'on ajoute un commit la tete de lecture bouge dans l'historique 
 l'identifiant des objet de commit est un (h)ash
 une branche est un pointeur vers un commit
 
 le fichier .gitignore permet de garder la trace du code souce uniquement
 lorsqu'on ouvre un fichier, head = la version chargée sur mon ordinateur
 git diff :  affiche les modification dans l'espace de travil suivis de git (nous permet d'avoir acces à l'invite de commande git  
 
 
git branch 
git push : recoit les commit qu'il a en retard par rapport zu local
git remote add
git show :  permet d'avoir un commit
git log :  change de commit et pointe vers le presedent
git pull -/- par rapport au server
git config -- :  pour configurer un element( global, list ...
git checkout(  main = charger dasn mon disque dur mes commit
le nom d'une branche n'est qu'un allias vers le commit le plus recent de la branche 
fast for war = 
la fusion de deux branches peut causer un conflit
git branch
git merge branch
git stash :  pour eviter de faire un commit ( pour mettre un travail en reserve  et le retrouver apres
une tete detaché : est une tete qui ne pointe pas vers une tete de branche mais un vieux commit

qund on a un nom de variable et qu'on veut voir tous les commits : git lo -p
retrouve les commit qui concerne notre fichier renommé avec son ancien nom :git log --follow
ne jamais vraiment modifier un commit dans le git

git reset <id> : revenir en arrier dans les git (on eleve des commit
git reset --hard  ( on abondonne tout le travail, a la fois les commits et tous les fichiers à l'interrieure

pull request : demande l'autorisation pour merger une branche