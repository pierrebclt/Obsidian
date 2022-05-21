
## Résolution de problèmes de conflits

https://komodor.com/learn/how-to-fix-fatal-refusing-to-merge-unrelated-histories-error/


## Utilisation de git

Lancer Git bash

Initier un git

git init

AJOUT DE FICHIER, COMMIT, PUSH

Ajouter des fichiers

git add index.html style.css

Faire un premier commit

git commit -m “Ajout des fichiers html et css de base”

Renommer notre branche master en main

git branch -M main

Réaliser un premier push vers github

git  remote add origin [https://github.com/EtudiantOC/OpenclassroomsProject.git](https://github.com/EtudiantOC/OpenclassroomsProject.git)

git push -u origin main

Second commit et push

git add index.html

git commit -m "Modification du fichier"

git push origin main

Status pour voir les fichiers modifié qui ne sont pas encore commit

git status

BRANCHES

Pour voir la liste des branches que l'on a

git branch

Création d'une nouvelle branche cagnotte et la sélectionner

git branch cagnotte

git checkout cagnotte

Fusion de branche (depuis la branche qui va recevoir l'autre branche) - exemple: etre sur main pour recevoir cagnotte:

git checkout main

git merge cagnotte

Pour supprimer une branche

git branch -d cagnotte

CLONER DOSSIER GITHUB, PULL, et MERGE REQUEST ET APPROVAL SUR LE SITE GITHUB

Pour cloner un fichier de github pour le ramener en local, se mettre dans le bon dossier puis :

git clone [https://github.com/pierrebclt/OpenclassroomTest.git](https://github.com/pierrebclt/OpenclassroomTest.git)

Donner un nom court au dépôt à distance (mais dans le cas du clone précédent il faut faire un cd pour aller dans le dossier qui contient le .git):

git remote add MonProjet [https://github.com/pierrebclt/OpenclassroomTest.git](https://github.com/pierrebclt/OpenclassroomTest.git)

Faire un pull pour ramener les dernières modifs

git pull MonProjet main

MODIFICATION DE FICHIER EN LOCAL

On suppose que l'on a modifié un fichier et faire un git add (donc le git status n'est pas clean)

Faire un stash pour revenir à une branche propre et créons une nouvelle branche.

git stash

git status (pour vérifier que c'est clean et que la modif a été sauvegardée temporairement)

git branch branche1

git checkout branche1

git stash list (pour voir les stash dispo)

git stash apply stash{1}

Liste des modifcations apportées récemment dans les commit et suppression d'un commit

git log

git reset --hard HEAD^ (pour supprimer le dernier commit)

Ou git reset --hard ca83a6df (les 8 premiers caracactères du hash sont suffisants)

Modifier le message du dernier commit

git commit --amend -m "Votre nouveau message de commit"

Si on a oublié un fichier dans le dernier commit

git add FichierOublie.txt

git commit --amend --no-edit

MODIFICATION DE FICHIER PUBLIC

Modifier le dernier commit sur un fichier pushé par erreur

git revert HEAD^

MODIFICATION GIT RESET

3 types de git reset

git reset notreCommitCible --hard

git reset notreCommitCible --mixed

git reset notreCommitCible --soft

CORRECTION DE COMMIT RATE

Avoir l'historique de ce qui s'est passé (plus puissant que git log)

git reflog

git checkout e789e7c (pour revenir à un commit antérieur)

Pour étudier toutes les modifs sur un fichier

git blame monfichier.txt

Récupérer quel quelques commit à incorporer dans une branche

git cherry-pick d356940 de966d4

Utilisation de git: on passe par pycharm pour faire des commits



## Conseils de symbioz

Source: [https://www.synbioz.com/blog/tech/git-adopter-un-modele-de-versionnement-efficace](https://www.synbioz.com/blog/tech/git-adopter-un-modele-de-versionnement-efficace)

Comme vous le savez peut-être, chez [Synbioz](https://www.synbioz.com), nous versionnons le code de nos projets à l’aide du [DSCM](http://en.wikipedia.org/wiki/Distributed_revision_control) [Git](http://git-scm.com/) dans le cadre de nos sessions de [développement agile](http://fr.wikipedia.org/wiki/M%C3%A9thode_agile).

J’ai au départ été très critique vis-à-vis de Git, de sa relative complexité d’utilisation et de sa courbe d’apprentissage plutôt ardue dès qu’il s’agit de faire des choses un peu évoluées. En effet, je viens du monde de [Mercurial](http://mercurial.selenic.com/) que j’utilise depuis plusieurs années et que je trouve beaucoup plus simple d’accès et d’utilisation.

Je me suit donc beaucoup documenté à propos de Git, fais des essais, parcouru les manuels pour comprendre les commandes et leurs utilités puis j’ai cherché à trouver un modèle de travail en équipe satisfaisant, propre et surtout simple à suivre.

Effectivement, si votre équipe ne suis pas une méthodologie de travail pré-déterminée, on se retrouve rapidement avec un historique fouillis, des merges inutiles, …

Récemment, nous avons découvert une méthodologie particulièrement adaptée à notre façon de travailler et qui tire parti des points forts de Git. Pour ne rien gâcher, cette méthologie est accompagnée d’un ensemble de scripts qui étend Git et permettent de respecter facilement les guidelines de cette méthodologie.

Avant de passer à la présentation de cette méthodologie, j’aimerai resituer le contexte. Nous travaillons à plusieurs, sur des projets qui peuvent durer plusieurs mois, voir plusieurs années. Des intervenants externes peuvent eux aussi contribuer au code. Nous avons besoin pour chaque projet d’une version de production, d’une version de développement et éventuellement de branches dédiées à de nouvelles fonctionnalités complexes qui doivent être isolées du reste du développement.

Il faut donc qu’aucun développeur ne fasse l’erreur de travailler dans master qui est considéré comme un reflet du code en production, il faut également que chaque développeur gère correctement ses branches pour ne pas polluer la branche de développement. Si toute l’équipe respecte ces règles, on se retrouve avec un dépôt propre, un historique lisible et cohérent et donc un processus simplifié pour le déploiement en production ou la maintenance d’un serveur de pré-production tout en gardant la possibilité de faire évoluer le code très vite et dans diverses directions sans polluer le code stable.

Le modèle adopté

Nos recherches nous ont mené à [cet article](http://nvie.com/posts/a-successful-git-branching-model/) qui décrit tout à fait la situation dans laquelle nous sommes et propose un workflow robuste.

Première constatation, le choix de Git n’est pas anodin puisqu’il est particulièrement adapté à un modèle à base de branches. Tout notre worflow se reposera donc sur un système de branches.

Lorsque nous commençons un projet, nous mettons toujours en place un dépôt central qui fait office de référence. Bien que Git soit un outil décentralisé, la mise en place d’un dépôt “maître” s’avère indispensable si vous travaillez à plusieurs. Chaque participant au projet va donc cloner le projet à partir de ce dépôt et c’est également sur ce dépôt que seront envoyées les modifications faîtes.

Une branche de production saine et cloisonnée

Sur notre dépôt, nous avons besoin de pouvoir gérer le code en production ainsi que les développements en cours.

Il est donc pertinent de considérer que la branche “master” représente l’état du code en production.

Il nous suffit maintenant de créer une branche supplémentaire “develop” qui permet de gérer les développements pour les versions à venir, c’est ce qu’on appelle souvent la branche d’intégration :

$git branch develop  
$git checkout develop

On peut donc dès maintenant contribuer au code et le commiter dans la branche “develop” sans que cela impacte notre code de production, voilà qui permet d’avancer en toute sérénité sans craindre que quelqu’un déploie du code non-testé ou validé.

Une branche pour développer les fonctionnalités futures

Dans “develop” nous allons donc faire de multiples commits pour agrémenter notre logiciel de nouvelles fonctionnalités. Cette branche peut d’ailleurs être utilisée en pré-production pour que vos testeurs et clients puissent profiter des avancements du projet et vous faire des retours.

Mais attention, “develop” n’est pas un fourre-tout et ne devrait être utilisé que pour les petites modifications simples ayant peu d’impact et ne demandant pas plus de 30 min de travail. En effet si vous travaillez directement sur “develop” pour une fonctionnalité estimée à 1 mois de développement, il y a fort à parier que vous aller ennuyer vos collégues avec vos commits qui s’incrustent entre 2 commits légitimes sans pour autant apporter une fonctionnalité finalisée.

Si vous êtes dans ce cas de figure, il vous faut créer une branche dédiée au développement de votre fonctionnalité.

Des branches spécifiques pour les développements lourds

Ces branches de développement (feature) permettent de travailler de manière détachée du reste de l’équipe en onant vos modifications ce qui permet de ne les appliquer sur “develop” qu’une fois satisfait et par la même occasion de ne pas polluer les collègues.

On peut vouloir commencer à développer une fonctionnalité qui ne sera appliquée qu’à la release N+1, la branche de feature est donc dans ce cas l’unique solution puisque tout ce qui est dans develop est considéré comme faisant partie intégrante de la prochaine release.

Une branche de développement est créée à partir de “develop” et sera, une fois terminée, mergée dans “develop”. Ce type de branche reste généralement locale à la machine du développeur qui fini par la merger dans “develop” le moment voulu. Il reste toutefois des cas où ces branches de feature sont partagées sur le dépôt central pour une revue par les autres développeurs.

Voici comment procéder :

$git checkout -b feature/foo develop

On a donc notre nouvelle branche “feature/foo” basée sur l’état actuel de “develop”. Nous pouvons donc coder et commiter autant de fois que nécessaire. Une fois fini, il faut intégrer cette branche dans “develop” :

$git checkout develop  
Switched to branch 'develop'$git merge --no-ff feature/foo  
Updating ea1b82a..05e9557(Summary of changes)$git branch -d feature/foo  
Deleted branch myfeature (was 05e9557).$git push origin develop

On est donc retourné dans la branche “develop” dans laquelle on demande à git de merger notre branche de feature. L’option --no-ff permet de forcer la création d’un commit même si les changements peuvent être intégrés en fast-forward. Ceci permet de garder une trace dans l’historique du développement dans une branche dédiée. Une fois mergée, nous supprimons la branche de feature devenue inutile et on push les modifications sur le serveur central.

Passage en production

Lorsque “develop” atteint un état satisfaisant pour créer un nouvelle release et déployer, il faut merger “develop” dans “master”, bumper la version, ajouter un tag de version, mettre à jour un README, … Enfin le code peut être déployé en production.

On pourrait imaginer qu’à chaque commit dans “master”, un hook soit déclenché pour déployer en production.

Nous allons donc, lors d’une release, créer une branche de support à la release. Les releases sont créées sur la base de la branche “develop” et doivent être mergées dans “master” et “develop”.

Cette branche ne servira qu’à faire des modifications mineures liées à la création de la release :

$git checkout -b release/v1.2 develop  
Switched to a new branch "release/v1.2"

On peut maintenant bumper la version, mettre à jour le changelog, etc

$git commit -a -m "Bumped version number to 1.2"[release/v1.1.2 74d9424] Bumped version number to 1.21 files changed, 1 insertions(+), 1 deletions(-)

Il ne nous reste plus qu’à merger cette release dans master pour qu’elle prenne effet :

$git checkout master  
Switched to branch 'master'$git merge --no-ff release/v1.2  
Merge made by recursive.(Summary of changes)$git tag -a v1.2

On souhaite également récupérer ces informations de release dans “develop” :

$git checkout develop  
Switched to branch 'develop'$git merge --no-ff release/v1.2  
Merge made by recursive.(Summary of changes)

Notre release est donc intégrée en production (master) et en intégration (develop), on peut supprimer la branche :

$git branch -d release/v1.2  
Deleted branch release/v1.2 (was ff452fe).

Dépanner les bugs critiques en production

Il vous arrivera certainement de faire face à un bug critique passé en production. Que faire dans ce cas ? Comment est-il géré dans le workflow ? Vous pensez peut-être qu’on doit nécessairement passer par une nouvelle release mais ce n’est pas le cas, ce n’est d’ailleurs même pas souhaitable puisque vous intégreriez au passage des fonctionnalités dans “develop” qui ne sont pas encore prête pour la production.

Dans ce cas de figure, il s’agit de faire ce qu’on appelle un “hotfix”. Un hotfix est un patch qui va s’appliquer directement à la branche de production (master) et qui sera ensuite également appliqué sur la branche d’intégration (develop). On peut maintenant déployer la version de production corrigée mais aussi jouir de ces corrections dans “develop”.

Pour se faire, comme toujours nous passerons par l’utilisation d’une branche pour avoir un historique sain :

$git checkout -b hotfix/v1.2.1 master  
Switched to a new branch "hotfix-1.2.1"

On crée une branche basée sur master et on bump la version du projet :

$git commit -a -m "Bumped version number to 1.2.1"[hotfix/v1.2.1 41e61bb] Bumped version number to 1.2.11 files changed, 1 insertions(+), 1 deletions(-)

On peut maintenant corriger le bug :

$git commit -m "Fix huge production bug"[hotfix/v1.2.1 abbe5d6] Fix huge production bug5 files changed, 32 insertions(+), 17 deletions(-)

Et intégrer la correction en production :

$git checkout master  
Switched to branch 'master'$git merge --no-ff hotfix/v1.2.1  
Merge made by recursive.(Summary of changes)$git tag -a v1.2.1

mais également en intégration pour ne pas perdre le fix au passage :

$git checkout develop  
Switched to branch 'develop'$git merge --no-ff hotfix/v1.2.1  
Merge made by recursive.(Summary of changes)

Le patch étant intégré en production et en développement, on peut supprimer la branche de hotfix devenue inutile :

$git branch -d hotfix/v1.2.1  
Deleted branch hotfix/v1.2.1 (was abbe5d6).

Tous les cas d’usages typiques ont été couverts et on voit qu’en suivant ce workflow, on peut maintenir un dépôt sain avec un historique clair et parfaitement adapté à la manipulation si d’aventure on devait revenir en arrière ou faire sauter une fonctionnalité.

C’est propre et carré mais assez fastidieux n’est-ce pas ? Suivre ce modèle au quotidien demande concentration et discipline, pour tous les développeurs. Heureusement, une bonne âme nous simplifie le travail grâce à un ensemble d’extensions pour Git qui permettent de simplifier l’application de ce workflow.

Git-flow

[Git-flow](https://github.com/nvie/gitflow) est un ensemble d’extensions pour Git livré sous forme de shell-scripts très simples d’accès.

Git-flow va permettre de suivre le workflow présenté précédemment sans avoir à tout retenir, surtout si comme moi vous êtes un peu perdu avec toutes les commandes et options de Git.

Initialisation

$git flow init

va permettre de paramétrer votre dépôt pour une utilisation via git-flow. Notez que tout ceci est local ce qui veut dire que vous pouvez très bien utiliser git-flow alors que vos collègues ne l’utilisent pas.

Des questions sur la nomenclature vous seront posées, je vous conseille vivement d’utiliser les valeurs par défaut qui sont quasiment des conventions.

Une fois terminé, vous êtes automatiquement positionné sur la branche “develop”, vous pouvez commencer à travailler.

Créer une branche de feature

$git flow feature start foo

Vous êtes désormais dans la branche “feature/foo” dans laquelle vous pouvez développer tranquillement votre fonctionnalité. Vous pouvez bien évidemment repartir dans d’autres branches, créer plusieurs branches de feature en parallèle, etc.

Une fois vos modifications terminées et prêtent à être intégrées dans “develop”, vous pouvez finaliser cette branche :

$git flow feature finish foo

Votre branche “feature/foo” va être mergée dans “develop” puis effacée et vous vous retrouverez à nouveau sur la branche “develop”.

Mise en production

Lorsque “develop” représente l’état souhaité en production, vous pouvez passer à la release :

$git flow release start v1.0.0

Une branche “release/v1.0.0” est créée, vous pouvez donc bumper la version de l’appli et faire les dernières modifications avant release. Une fois paré, vous pouvez finaliser la release :

$git flow release finish v1.0.0

Ceci aura pour effet de merger “develop” dans “master”, de taguer la release, puis de back-merger ces modifications dans “develop”. La branche de release sera ensuite supprimée et vous retournerez sur la branche “develop”.

Hotfix

Si vous avez besoin de patcher urgemment la production, vous utiliserez la commande dédiée aux hotfixes :

$git flow hotfix start typo

Une branche “hotfix/typo” est créée et vous pouvez commencer à patcher. Une fois fini, il suffira de finaliser la branche :

$git flow hotfix finish typo

Ceci aura pour effet d’appliquer votre fix sur master et develop, d’ajouter un tag puis de supprimer la branche de hotfix. À ce propos, n’oubliez pas de bumper la version avant de finaliser le hotfix.

J’espère avoir pu vous éclairer un peu sur la façon dont nous gérons le code source dans nos équipes et que celà vous donnera envie d’essayer ce worflow qui selon moi devrait permettre à vos dépôts de rester cohérents, de pouvoir gérer indépendamment les avancées fonctionnelles, les patchs et releases sans finir la journée avec un mal de tête !

L’équipe Synbioz.

Libres d’être ensemble.