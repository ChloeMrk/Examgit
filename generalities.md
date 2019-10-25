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
