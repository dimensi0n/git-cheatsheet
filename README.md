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
- Cela facilite également la collaboration et sert à resoudre facilement les conflits.

I- systemme de gestion de version
NB:  Dans le git on ne met que le code source, pas le compilé ni tout ce qui tourne autour

 on distingue ainsi plusieurs types de systèmes :
 
 - le systeme centralisé : tout part du serveur qui gere les historiques en local sur notre ordinateur qui lui est allimenté par les fichers qu'on peut stocker 
 - le système distribué : git est un systeme distribué mais quand meme centralisé et fonctionne de la façon suivante
   une copie de l'historique des versions est disponible localement
   possibilité de travailler sans latence et hors ligne
   possibilte de modifier le local avant de le lancer sur le server
   distribué mais pas centralisé
   server populaire : git hub et git lab
   on eut eglement utiliser github desktop comme interface graphique
 
  Cas pratiques
- git clone : permet de cloner un dépôt Git existant sur votre ordinateur.

- git add : permet d'ajouter des fichiers à l'index (ou staging area) de Git, cest une unité de travaille.

- git commit : permet de créer un commit, c'est-à-dire de sauvegarder les modifications apportées aux fichiers dans l'index.

- git push : permet d'envoyer vos commits vers un dépôt distant, comme GitHub.

- git pull : permet de récupérer les derniers commits d'un dépôt distant et de  les fusionner avec votre dépôt local.

- git branch : permet de gérer les branches de votre dépôt.

- git merge : permet de fusionner des branches.

- git status : permet de voir l'état de votre dépôt, c'est-à-dire quels fichiers ont été modifiés ou ajoutés et sont prêts à être commités.

- git init : initaliser un depot pour notre projet

- git log : permet d'afficher l'historique des commits de votre dépôt.

- git show : permet d'afficher les détails d'un commit spécifique, comme les modifications apportées aux fichiers et les informations sur l'auteur du commit.

- git diff : permet d'afficher les différences entre les fichiers dans votre dépôt et l'index de Git.

- git stash : permet de mettre de côté temporairement les modifications apportées à vos fichiers, afin de pouvoir basculer vers une autre branche ou travailler sur quelque chose de différent sans perdre vos changements.

- git tag : permet de marquer un commit spécifique avec une étiquette, qui peut être utilisée pour se référer facilement à ce commit plus tard.

- git reset : permet de réinitialiser votre dépôt à un commit précédent, annulant ainsi tous les commits suivants fusionner avec votre dépôt local.

- git rebase : permet de fusionner des commits en les "rebasant" sur un commit précédent, ce qui peut être utile pour simplifier l'historique des commits d'un dépôt.

- git cherry-pick permet de sélectionner un commit spécifique et de l'appliquer à votre dépôt.

- git clean : permet de supprimer les fichiers non suivis de votre dépôt, c'est-à-dire les fichiers qui ne sont pas dans l'index de Git.

- git gc (garbage collection) permet d'optimiser votre dépôt en supprimant les commits inutiles et en regroupant les données de manière plus efficace.

- git mv : permet de déplacer ou de renommer des fichiers dans votre dépôt, tout en conservant l'historique des modifications apportées à ces fichiers. 
 
  
 le fichier .gitignore permet de garder la trace du code souce uniquement
 lorsqu'on ouvre un fichier
  head = la version chargée sur mon ordinateur
 
 

- git config -- :  pour configurer un element( global, list ...
- git checkout(  main = charger dans mon disque dur mes commits)
le nom d'une branche n'est qu'un allias vers le commit le plus recent de la branche 

- git stash :  pour eviter de faire un commit ( pour mettre un travail en reserve  et le retrouver apres)
- une tete detaché : est une tete qui ne pointe pas vers une tete de branche mais un vieux commit

- Pour retrouve les commit qui concerne notre fichier renommé avec son ancien nom faire : git log --follow


- git reset <id> : revenir en arrier dans les git (on eleve des commit) 

- git reset --hard : (on abondonne tout le travail, a la fois les commits et tous les fichiers à l'interieure)

-pull request : demande l'autorisation pour merger une branche


Parcours des fichiers

 working directory[a la creation du fichier]=> [lorqu'on utilise la commande add]stage(index)=>[lorsqu'on utilise le comit]history

 Ps : - à chaque fois qu'on ajoute un commit la tete de lecture bouge dans l'historique.

       - l'identifiant des objets de commit est un hash
        une branche est un pointeur vers un commit
         
         - ne jamais vraiment modifier un commit dans le git
         - la fusion de deux branches peut causer un conflit
