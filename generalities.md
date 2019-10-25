°Configuration de Git

*Enregistrer dans .gitconfig de notre compte user

$git config --global user.name Chloe

$git config --global user.email chloe.merck@ynov.com

*Choisir un éditeur pour écire le texte du commit

$git config --global core.editor vim

*Pour faire un dêpot en particulier, dans le fichier config du dossier .git/

$git config --local user.name Alan
$git config --local user.email alan@alan.fr



°Zone de travail de Git

Ajouter à l'Index: $git add mon_fichier

Ajouter un emsemble de fichier/dossiers ou modifier: $git add . ou $git add -A



Remarque: Tant que le fichier n'est pas ajouter dans l'index Git, Git ne connaîtra pas le fichier et il ne sera pas suivi en version. Une fois dans l'index il sera suivi en version


Dépôt: git commit -m "une feature"

°Règles messages de commit

- un titre de 49 caractères max
- pour un texte plus long, répondre à la question du pourquoi de votre texte
- on peut commiter avec un titre uniquement option -m

Exemple : $git commit -m "étudiant/tp: si terminé, attribuer note"

$ git commit : pour ouvrir l'éditeur et mettre un titre et texte plus long



°git init

Initialiser un projet Git: git init

Pour vérifier l'état de votre dépot: git status


°Pour voir les différents commit:

$git log

$git log --oneline

$git shortlog


°Commandes pour gérer un dépôt Git

$git status
$git help [nom de la commande]
$git log
$ git log --oneline # voir les commit en une ligne
$ git log master..origin/master # voir les différences entre deux branches
$ git log -5 # 5 derniers commits
$ git log -p -5 # log avec différence pour chaque commit sur les 5 derniers
$ git log --stat # stat sur les modifs par commits
$ git log --since=2.weeks # depuis deux semaines, --until existe également


°Blame pour voir qui a fait les modifications

$ git blame -L 40,60 readme.md # rechercher qui a fait les modifs par ligne -L
$ git blame --since=3.weeks -- readme.md # depuis 3 semaines avec auteurs des modifications
$ git blame -L "/^### /" readme.md # recherche avec expression régulière


°Renommer un fichier

$git mv mon_ancien_fichier mon_nouveau_fichier

°Supprimer un fichier

$git rm mon_fichier

Attention ne pas oublier d'ajouter $git add nom_fichier pour confirmer la suppression

°Ne plus suivre un fichier

$git rm --cached images/incredients.jpg

Voir les fichiers suivis:

$git ls-files


