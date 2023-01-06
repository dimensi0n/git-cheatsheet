# Git Cheat Sheet - ESGI

## Configuration des outils

- `git config` : Cette commande permet de configurer les paramètres de Git à différents niveaux (système, utilisateur ou local au niveau d'un dépôt). Elle peut être utilisée pour définir votre nom d'utilisateur et votre adresse électronique, qui seront utilisés pour les opérations de commit. Par exemple : git config --global user.name "Mon Nom"

- `git init` : Cette commande permet de créer un nouveau dépôt Git local. Elle doit être utilisée dans le répertoire qui doit être suivi par Git.

- `git clone` : Cette commande permet de créer une copie locale d'un dépôt Git existant. Elle est souvent utilisée pour travailler sur un projet en collaboration avec d'autres personnes, car elle permet de télécharger tout le contenu du dépôt ainsi que l'historique complet des commits. Par exemple : `git clone https://github.com/user/repo.git`

- `git remote` : Cette commande permet de gérer les connexions à d'autres dépôts distants. Elle peut être utilisée pour ajouter un dépôt distant à votre dépôt local en utilisant la sous-commande add, comme dans l'exemple suivant : `:wq
git remote add origin https://github.com/user/repo.git`

## Qu'est-ce qu'un commit ?

Un commit Git (ou simplement commit) est une sauvegarde de l'état actuel du dépôt dans l'historique. En d'autres termes, un commit permet de conserver une version de tous les fichiers du dépôt à un moment donné. Lorsque vous effectuez un commit, vous spécifiez un message de commit qui décrit les modifications apportées au dépôt depuis le dernier commit. Cela peut être utile pour comprendre les changements apportés au dépôt au fil du temps et pour revenir à une version précédente du dépôt si nécessaire.

Les commits forment une chaîne dans l'historique du dépôt, chaque commit faisant référence au commit précédent. Cela permet de suivre l'évolution du dépôt au fil du temps et de naviguer dans l'historique des commits.

En utilisant des commits de manière régulière, vous pouvez maintenir un historique clair et organisé de votre travail et faciliter la collaboration avec d'autres personnes sur un projet.

## Consulter les modifications et effectuer des commits

- `git status` : Cette commande permet de voir les fichiers modifiés et ceux qui sont en attente de commit. Elle est souvent utilisée pour savoir où en est l'état du dépôt local par rapport au dernier commit.

- `git diff` : Cette commande permet de voir les différences entre les fichiers modifiés et ceux du dernier commit. Elle est souvent utilisée pour voir les détails des modifications apportées aux fichiers.

- `git add` : Cette commande permet de mettre des fichiers en attente de commit. Elle est souvent utilisée pour ajouter des fichiers modifiés ou nouvellement créés au prochain commit. Par exemple : `git add path/to/file.txt`

- `git commi`t : Cette commande permet de créer un commit, c'est-à-dire de sauvegarder l'état actuel du dépôt dans l'historique. Elle doit être utilisée avec un message de commit qui décrit les modifications apportées. Par exemple : `git commit -m "Ajout d'une nouvelle fonctionnalité"`

> Voici un exemple de workflow courant avec ces commandes :
> 
> 1. Modifiez un ou plusieurs fichiers dans votre dépôt local.
> 2. Utilisez git status pour voir quels fichiers ont été modifiés.
> 3. Utilisez git diff pour voir les détails des modifications apportées aux fichiers.
> 4. Utilisez git add pour mettre en attente les fichiers modifiés que vous souhaitez inclure dans le prochain commit.
> 6. Utilisez git commit avec un message de commit pour enregistrer les modifications dans l'historique du dépôt.

## Nommer une série de commits et les combiner entre eux

- `git tag` : Cette commande permet de créer, lister et supprimer des tags dans Git. Un tag est un nom qui peut être associé à un commit spécifique dans l'historique du dépôt. Les tags sont souvent utilisés pour marquer des versions stables ou importantes du dépôt, par exemple une version de production ou une version de développement en cours. Par exemple, pour créer un nouveau tag nommé v1.0 qui pointe sur le dernier commit, vous pouvez utiliser la commande suivante : `git tag v1.0`

- `git branch` : Cette commande permet de gérer les branches dans Git. Une branche est une série de commits qui évolue indépendamment des autres branches. Les branches sont souvent utilisées pour développer de nouvelles fonctionnalités ou corriger des bogues, tout en maintenant une version stable du dépôt sur la branche principale (appelée "master"). Par exemple, pour créer une nouvelle branche nommée new-feature, vous pouvez utiliser la commande suivante : `git branch new-feature`

- `git merge` : Cette commande permet de combiner les commits d'une branche dans une autre. Elle est souvent utilisée pour fusionner les modifications apportées sur une branche de développement dans la branche principale une fois que le travail est terminé. Par exemple, pour fusionner les commits de la branche new-feature dans la branche master, vous pouvez utiliser la commande suivante : `git merge new-feature`

- `git cherry-pick` : Cette commande permet de sélectionner un commit spécifique et de l'appliquer à la branche courante. Elle est souvent utilisée pour sélectionner individuellement des commits d'une branche et les appliquer à une autre, au lieu de fusionner tous les commits d'une branche avec git merge. Par exemple, pour appliquer le commit avec l'ID abcdefg à la branche courante, vous pouvez utiliser la commande suivante : `git cherry-pick abcdefg``

## Exclure des modifications et des fichiers du dépôt

Un fichier .gitignore est un fichier de configuration qui permet de définir une liste de fichiers et de dossiers à ignorer par Git. Lorsque vous ajoutez un fichier ou un dossier à ce fichier, Git ne suivra pas les modifications apportées à ces éléments et ne les inclura pas dans les commits.

Voici comment utiliser un fichier .gitignore pour exclure des fichiers et des chemins temporaires :

1. Créez un fichier .gitignore dans le répertoire racine de votre dépôt Git.
2. Ajoutez la liste des fichiers et dossiers à ignorer, un par ligne. Vous pouvez utiliser des caractères génériques comme * et ? pour ignorer plusieurs fichiers similaires. Par exemple, pour ignorer tous les fichiers terminant par .tmp, vous pouvez ajouter la ligne suivante au fichier .gitignore : *.tmp
3. Enregistrez le fichier .gitignore. Git commencera à ignorer les fichiers et dossiers spécifiés dans ce fichier lors de l'exécution de la commande git add.

> Notez que si vous avez déjà ajouté des fichiers ou dossiers à Git avant de les ajouter au fichier .gitignore, ils resteront suivis par Git et inclu dans les commits futurs. Vous pouvez utiliser la commande git rm --cached pour arrêter de suivre ces fichiers et les exclure des commits futurs.

