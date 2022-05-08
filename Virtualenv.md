## Utilisation de virtualenv

Note: il faut faire tout ce qui est dessous depuis le cmd de windows que l'on amène au bon dossier, ne pas lancer pycharm avant

Apartir de cmd lancé directement dans windows :

pip install virtualenv

Créer un environnement virtuel pour le projet (depuis le path du dossier: cd …) :

virtualenv -p python3 venv

Pour se mettre dans l'environnement virtuel

.\venv\Scripts\activate

Pour sortir de l'environnement virtuel

deactivate

Installer les packages:

pip install pandas (par exemple)

Voir les packages pip installés:

pip freeze

Créer un fichier requirements.txt:

pip freeze > requirements.txt

Si besoin d'installer toutes les librairies indiquées dans requirements.txt:

pip install -r requirements.txt