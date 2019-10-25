°Consultation de l'historique et des modification

°git log

Afficher les commits sans pagination: $git --no-pager log --oneline

Afficher 3 commits: $git --no-pager log -3 --oneline

Afficher les 2 derniers commits: $git log --oneline -2

Afficher les commits d'un auteur en particuliers: $git log --author "Antoine07"

Afficher l'historique d'une certaine date ou d'un jour: $git log --since=1.day
$git log --before="2019-09-01"

Afficher l'historique d'un fichier: $git log nom_du_fichier.txt

Afficher les modifications d'un fichier ou d'un ensemble d'un fichier: $git log -p nom_du_fichier.txt

Dans l'ensemble des commits: $git log -p

Ou pour les 2 derniers commits: $git log -2 -p


Rechercher dans les logs: $git log -E -i --grep='Pizza'

Afficher la personne qui a fair les modifications: $git blame nom_du_fichier.txt

Pour visualiser une modification avant de l'indexé: $git diff

Afficher les différence entre le dernire commit et l'index: $git diff --cached

Afficher les modifications d'un commit en arrière: $git diff HEAD~1

Afficher entre deux positions du HEAD: $git diff HEAD~3 HEAD

Afficher les modification entre deux commits donnés: - Récupérer les haches des deux derniers commits: $git log --oneline
-Afficher les logs entre deux commits : $git log f5541d6 b058c4f

Faire des stats sur les différences opérées dans les fichiers: $git diff --stat

Annuler les modification dans l'espace de travail et remettre le dépôt dans l'état dans lequel il se trouvait: $git restore nom_du_fichier

Par contre si on refait la modification et que l'on ajoute le fichier dans l'index il faut taper: $git restore --staged

°Modififer un message de commit:

On peut modifier un message de commit sous deux conditions:

1- Qu'il n'y a pas eu d'autre commit entre temps.

2 - Qu'on a pas "publié" le commit en question sur une branche distante

$git commit "un message" --amend --no-edit


°Git reset HEAD~1

Annule le dernier commit et met tout dans le WD sans perte: $git reset HEAD~1   

Annule le dernier commit et met dans la staging area sans perte: $git reset --soft HEAD~1

Annuler plusieurs commit en revenant en arrière dans l'historique: $git reset 8ef0ef2
 ce qui supprimera tout ce qui est après ce commit

Annuler le dernier commit et supprime les modifications (A eviter):$git reset --hard HEAD~1


Remettre un fichier dans son état init: $git checkout

Annule un commit en créant un commit d'annulation: $git revert (numéro du log)