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
