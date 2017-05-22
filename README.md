# horseproject
Projet Etudiant Esiee Paris version alpha
Commandes et bonnes pratiques GIT


1. Bonnes pratiques :


Vérifier son code avant de push.
Ne faire de pull(merge sur gitlab) request que si le code concerné fonctionne = ne jamais faire une pull request avec une ou des fonctions non achevées.
La branche master doit TOUJOURS être propre.
Ne JAMAIS merger sa propre pull request, attendre que quelqu’un d’autre la relise et la valide.
Ne jamais tenter d’effectuer des pull request en ligne de commande, toujours le faire sur github(gitlab).
En cas de doute, il vaut mieux demander.


2. Commandes git


$ git branch : indique la branche actuelle.

$ git branch [nom de ma branche] : créé une nouvelle branche.

$ git branch -d [nom de ma branche] : supprime une branche.

$ git branch -D [nom de ma branche] : force suppression branche meme avec commit non push.

$ git checkout [nom de ma branche] : change pour la branche indiquée en paramètre.
 
$ git status: affiche les fichiers modifiés

$ git add [mon fichier] : ajoute un fichier pour commit.

$ git add . : ajoute tous les fichiers modifiés pour commit. /!\ à utiliser avec précaution /!\

$ git commit -m “[dossier modifié] | [modifications apportées]” : commit les fichiers précédement ajoutés.

$ git push origin [nom de ma branche]  : push le ou les commits sur le repo git. /!\ Attention à ne pusher que sur votre branche /!\

$ git fetch --all : fetch la copie du repo pour identifier d’éventuelles modifications.

$ git pull origin [nom de la branche] : récupère les modification du repo sur la copie locale.

 $ git rm . -r --cached : supprime le cache git (peut être utile en cas de souci avec le .gitignore, un git add . est nécessaire pour prendre en compte la suppression des fichiers et dossiers exclus)

$ git merge [nom de la branche] : merge le code de la branche indiquée en paramètre sur la branche actuelle. ATTENTION à ne pas merger votre branche sur master mais bien master sur votre branche.


3. Tips


Pour récupérer le travail qui a été fait en votre absence :

$ git checkout master

puis :
$ git fetch --all 

puis :
$ git pull origin master  

puis :
$ git checkout [ma branche]  

et enfin :
$ git merge master
