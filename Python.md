## Créer un projet en python

Structure d'un projet "yahtzee":

-   yahtzee

-   model/ #pour les fichiers des model
-   controler/ #dossier pour mettre les fichiers controler
-   views/ #dossier qui contient les vues
-   tests/ #pour les fichiers de tests unitaires
-   doc/ #dossier sur les
-   ipynb/ #pour les fichiers jupyters
-   venv/ #environnement virtuel
-   .git/ #le dossier de git
-   app.py #le fichier principal
-   .gitignore #le git ignore
-   requirements.txt #le fichier des requirements
-   README.md #le readme qui est vide

Aller dans le dossier où l'on veut créer le modules (ex: Perso / Projets) et créer un module appelé "yahtzee":

-   cd Perso/Projets
-   mkdir yatzee
-   type NUL > app.py # pour créer un fichier app.py qui est vide
-   type NUL > .gitignore
-   Virtualenv (pour les projets majeurs) :

-   virtualenv -p python3 venv # Creation d'un environnement virtualenv dans un dossier venv
-   .\venv\Scripts\activate # Pour activer le virtualenv (deactivate pour en sortir)
-   Pip install pandas
-   Pip install numpy
-   pip install jupyterlab
-   pip freeze > requirements.txt # Pour créer un fichier de requirements

-   Git :

-   Créer un repositary dans github (ex:yatzee)
-   git init # Pour initier un git
-   git add app.py
-   git commit -m "first commit"
-   git branch -M main # renommer la branche master en main
-   git remote add origin [https://github.com/pierrebclt/yahtzee.git](https://github.com/pierrebclt/thermodynamique.git)
-   git push -u origin main # pousser le contenu

-   dossier model/:

-   mkdir model
-   cd model
-   type NUL >  __init__.py

-   dossier tests/:

-   mkdir tests
-   cd tests
-   type NUL >  __init__.py

-   type NUL > setup.py # fichier que l'on laisse vide (pour les gros projets ?)
-   type NUL > README.md #  (pour les gros projets ?)

-   dossier doc/: # pour mettre de la documentation au besoin

## Explication très claire sur les classes :

[https://pynative.com/python-class-method/](https://pynative.com/python-class-method/)

## Very nice cheatsheet python 3 (en particulier sur les classes):

[https://programmingwithmosh.com/python/python-3-cheat-sheet/](https://programmingwithmosh.com/python/python-3-cheat-sheet/)

## Execution d'un projet déjà créé

Exemple : monprojet-git

Dans invite de commande (cmd), taper cd et l'adresse pour aller jusqu'au dossier du projet

.\venv\Scripts\activate # Pour activer le virtualenv (deactivate pour en sortir)

jupyterl ab # pour lancer jupyter si projet de type jupyter

## Bonnes pratiques python

Sources : [Openclassroom/Perfectionnez-vous en Python](https://openclassrooms.com/fr/courses/4425111-perfectionnez-vous-en-python/4463200-organisez-un-script)

      [https://docs.python.org/fr/3/library/__main__.html](https://docs.python.org/fr/3/library/__main__.html)  
      [https://dev.to/codemouse92/dead-simple-python-project-structure-and-imports-38c6](https://dev.to/codemouse92/dead-simple-python-project-structure-and-imports-38c6)

En haut du script:

#! /usr/bin/env python3

# coding: utf-8

Mettre le script dans main():

def main():

    #du code

if__name__=="__main__":

    main()

Structure d'un projet (ex: projet enigme)

-   enigme-project

-   requirements.txt
-   .gitignore
-   venv
-   setup.py (fichier vide à créer)

-   enigme

-   __init__.py

-   __main__.py

-   model

-   __init__.py
-   classe1.py
-   classe2.py

-   tests

-   __init__.py
-   tests_unitaires.py

-   enigme-git (c'est testé et c'est moins bien)

-   requirements.txt
-   .gitignore
-   venv
-   setup.py (fichier vide à créer)
-   __init__.py
-   app.py
-   model

-   __init__.py
-   classe1.py
-   classe2.py

-   tests

-   __init__.py
-   tests_unitaires.py

Pour appeler une classe :

from model.classe1 import Classe1

Pour executer le code principal (qui se trouve dans __main__.py) depuis cd../enigme-git> :

python app.py

Pour lancer les tests unitaires depuis cd../enigme-git>:

python tests.tests_unitaires.py -v #Note: le -v permet d'afficher tous les tests effectués

## Python - dates

- [[Python - dates]]

## Python - pathlib
- [[Python - pathlib]]
- 