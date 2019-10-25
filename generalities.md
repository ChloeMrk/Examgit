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

Index: *git add mon_fichier

Dépôt: git commit -m "une feature"

Remarque: Tant que le fichier n'est pas ajouter dans l'index Git, Git ne connaîtra pas le fichier et il ne sera pas suivi en version. Une fois dans l'index il sera suivi en version

°git init

Initialiser un projet Git: git init

Pour vérifier l'état du fichier indexée: git status