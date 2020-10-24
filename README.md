# POC pour gérer plusieurs dépôts git

Le principe de cette recherche et de trouver un outil qui permet de gérer de multiples dépôts git entre eux. Aussi bien pour les équipes de dev que les équipes d'intégration pour la phase de build.

## Besoins
Chaque équipe à plusieurs besoins :
- Pour les intégrateurs, le besoin principal est de connaitre la structure des dépôts Git pour pouvoir cloner correctement tous les dépôts nécessaires pour générer le produit. Cela est très utile pour l'intégration continue.
- Pour les développeurs, ils ont eux aussi le besoin de cloner leur espace de travail au départ. Mais ils ont comme besoin de pouvoir faire les mêmes actions sur plusieurs dépôts git. Ex : dans le cas du développement d'une fonctionnalité qui impacte plusieurs dépôts, ils doivent avoir la possibilité de rapidement créer un groupe de dépôts contenant seulement les dépôts modifiés pour pouvoir créer une branche de feature sur chacun des dépôts et pouvoir commit les modifications.

## Outils existants

J'ai pu lire ou tester 3 outils qui semblait prometteur.

|Informations  |repo  |mu-repo  |gr  |
|---------|---------|---------|---------|
|Site |[https://gerrit.googlesource.com/git-repo/](https://gerrit.googlesource.com/git-repo/) |[http://fabioz.github.io/mu-repo/](http://fabioz.github.io/mu-repo/) |[http://mixu.net/gr](http://mixu.net/gr) |
|Licence     | Apache-2.0 | GPL 3 | Aucune |
|Langage     | Python 3.6 | Python 3.6 | nodeJS |
|Maintenu | Oui et par google | oui mais petite communauté | Non depuis 2017 |
|Prix     | Gratuit | Gratuit | Gratuit |
|Cloner des dépôts     | Système avancé à partir d'un fichier xml dans un dépôt git | Système limitée à partir du .gitconfig | Non |
|Créer des groupes de dépôts partagés | Oui | Non | Non |
|Créer des groupes de dépôts en local | Oui mais ne semble pas simple | Oui | Oui et facilement |
|Complexité | *** | ** | * |
|Commande sur un ensemble de dépôts | Oui | Oui | Oui |

## Repo