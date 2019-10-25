Une branche dans Git est un pointeur mobile léger vers un de ces commit

Git créer automatiquement la branche master

On peut créer autant de branche qu'on veut car git n'est qu'un simple ficher de 40 caractère

Créer une branche: $git branch nom_de_la_branche

Afficher l'ensemble des branches:$git branch

Pour se déplacer sur une autre branche : $git checkout nom_de_la_branche

Le pointeur HEAD se déplacera de la branch master au nom_de_la_branche

Pour revenir à la branche master qui déplacera aussi le Head: $git checkout master

Créer et se déplacer sur une nouvelle branche: $git checkout -b feature_header

°Branche diverge

Parfois une branche peut être plus avancée par rapport à une autre on appelle ça l'historique qui diverge.

Il risque d'avoir un conflit dans un même fichier quand on va merger la branche master(qui est plus avncée) avec une autre branche moins avancée. Git propose un système de gestion des conflits

Supprimer une branche: $git branch -d [nom_de_la_branche]
Forcer la suppression d'une branche: $git branch -D [nom_de_la_branche]

Merger(mélanger deux branches) sans divergence: être sur la branche master et taper $git merge dev

git merge dev --no-ff
En réalité lorsque la branche master n’avance pas par rapport à la branche dev
par exemple, Git est en mesure de linéariser l’historique des commits. Et donc il
ne crée pas de commit supplémentaire. Créez un commit de merge dans cette
situation vous permettra de revenir éventuellement plus facilement sur ce dernier
et de savoir qu’il y a une branche de faite à ce moment là précisément.
M1 -- -- -- -- M2
\               /
    D1 - D2 - D3


Lister toutes les branches non mergées :$git branch --no-merged

Gestion de conflits:

Il faudra choisir la version du fichier désirée et l'appliquer. Supprimer les branches features qui ne sont plus utiles
Le remisage: on peut quitter une branche abec un esapce de travail propre pour aller sur une autre branche.

Mettre un code de côtée dans une branche: $git stash

Lister les stash sur une branche: $git stash list

Récupérer et appliquer: $git stash apply

Supprimer une remise: $git stash drop

Pour mettre dans l'index: $git stash apply --index

Il peut avoir plusieur stash, il faut juste faire afficher la liste des stash, prendre le numéro et faire la commande: $git stash apply stash@{numéro du stash désiré}


°Tag:

Il existe deux types de tags : les tags annotés ou les tags légers. On les utilise
pour marquer un état important du logiciel.
14
• Un tag léger est similaire à une branche, mais contrairement à une branche,
un tag n’est pas mobile. Il est associé à un commit.
• Un tag annoté est un objet dans Git, il pointe également sur un commit
donné et n’est donc pas mobile. Il possède une somme de contrôle et
contient le nom l’email de l’auteur, la date, un message et peut être signé
et vérifié (GPG).

Tag annoté: $ git tag -a v1.0 -m "version 1 de l'application"

Tag léger peu utilisé: $ git tag v1

Etiquetter après coup sur un commit donné: $ git tag -a v1.0.1 -m "version 1.0.1" 9fceb2


Lister les tags: $git tag

Rechercher des tags particuliers: $git tag -1 'v8.*'

Voir tag annoté: $git show v8.2

°Branches distantes

-Sur le bureau:
$ cd GitServer
$ mkdir my_lessons_server.git
$ cd my_lessons_server.git

-Création du server Git:
$ git --bare init

Puis on va dans le dossier my_lessons:
$ git init
$ echo "# Lessons" > README.md
$ git add .
$ git commit -m 'first commit'

Indiquer un chemin absolu pour indiquer où se trouve votre serveur. La commande est : $git remote add origin C:\Labs\my_lessons_server.git

puis push la branche master dans le dépôt dans le serveur origin: $git push origin master




