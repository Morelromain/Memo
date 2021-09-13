# MEMO

[1 : Environnement virtuel](#Env)  
[2 : Git/Git Hub](#Git)  
[3 : Tests Python](#Test)  
[4 : Django](#Django)  
[5 : SQL](#SQL)  
[6 : Docker](#Docker)  
[7 : Heroku](#Heroku)  
[8 : React](#React)  
[Documentation](#Liens)

---
<a name="Env"></a>

## 1 : Environnement virtuel

### Creer un env avec venv et pip

creation : `python -m venv env`  
activation : `env\Scripts\activate.bat`  
desactivation : `deactivate`  
  
installation package : `pip install package`  
voir les packages installés : `pip freeze`  
transferer les packages : `pip freeze > requirements.txt`  
[Doc Venv](https://docs.python.org/fr/3/library/venv.html)

### Creer un env avec pipenv

pipenv shell *A completer*

---
<a name="Git"></a>

## 2 : Git/Git Hub

### Installation
initialiser : `git init`  
creer connection : `git remote add <nom> <url_du_projet.git>`  
cloner dossier : `git clone <url_du_projet.git>`  
(rentré dans dossier ensuite)

### Gestion branche
voir les branches : `git branch`  
creer branche : `git branch <nom>`  

changer de branche : `git checkout <nom>`  
récupérer donnés d'une autre branche : `git merge <nom>`  
supprimer branche : `git branch -d <nom>`

### Mettre à jour
maj : `git add fichier` ou : `git add .`  
enregistrement maj : `git commit -m "<commentaire>"`  
voir info maj : `git reflog` 
retore fichier : `git checkout e789e7c`

### Gestion github
creer sa branche sur github : `git push --set-upstream origin <nom>`  
envoyer sur github : `git push -u origin`  
[Doc Git](https://git-scm.com/docs)

---
<a name="Test"></a>

## 3 : Tests Python

lancer pytest complet : `pytest <dossier_test> -vvv`  
lancer locust : `locust -f <dossier_test>/locustfile.py`  
intaller covtest : `pip install pytest-cov`  
lancer covtest : `pytest --cov=. --cov-report html tests\test_server.py`    
test django : `python manage.py test`  
[Doc Pytest](https://docs.pytest.org/en/6.2.x/contents.html)

---
<a name="Django"></a>

## 4 : Django

install django : `pip install django`  
créer projet : `django-admin startproject <nom_projet>`  
lancer : `python manage.py runserver`

créer appli : `python manage.py startapp <nom_app>`  
créer superuser : `python manage.py createsuperuser`  
créer migration BDD : `python manage.py makemigrations`   
migrer BDD : `python manage.py migrate`

install django-postgreSQL : `pipenv install psycopg2`   
postgresSQL : `psql -u postgres`  
supprimer les pycaches : *Bash* `find . -type d -name __pycache__ -exec rm -r {} \+`  
enregistrer les données DB : `manage.py dumpdata > save_data.json`  
charger les données DB : `manage.py loaddata save_data.json`  
[Doc Django](https://docs.djangoproject.com/fr/3.1/)  
[Doc Django-Rest-Framework](https://www.django-rest-framework.org/)  

---
<a name="SQL"></a>

## 5 : SQL

afficher SQL : `\l`  
créer database : `CREATE DATABASE nom;`  
supprimer database : `DROP DATABASE nom;`  
[Doc SQL](https://sql.sh/)

---
<a name="Docker"></a>

## 6 : Docker
### Local

se connecter : `docker login`  
créer image : `docker build -t <nom_log>/<nom_image> .`  
lancer image : `docker run -p 8000:8000 -i -t <nom_log>/<nom_image>`  

### Docker Hub
créer image avec tag : `docker build -t <nom_log>/<nom_image>:<tag> .`  
envoyer image sur HUB : `docker push <nom_log>/<nom_image>:<tag>`  
récuperer image sur HUB : `docker pull <nom_log>/<nom_image>:<tag>`  
[Doc Docker](https://docs.docker.com/)

---
<a name="Heroku"></a>

## 7 : Heroku

se connecter : `heroku login` `heroku container:login`  
recupéré token d'auth : `heroku auth:token`  
envoyer sur Heroku : `heroku container:push web --app <nom_app>` 
envoyer sur Heroku2 : `git push heroku main`
lancer sur Heroku : `heroku container:release  web --app <nom_app>`  
[Doc Heroku](https://devcenter.heroku.com/categories/reference#command-line)

---
<a name="React"></a>

## 7 : React

vérifier node et npm sont installé: `node -v` `npm -v`  
creer projet : `npx create-react-app <nom_projet>`  
lancer projet : `npm start`  
reprendre projet : `npm i`  
compiler projet : `npm run build`  
bibliothèque : `npm i -s router react-router-dom node-sass`  
[Doc React](https://fr.reactjs.org/)

---
<a name="Liens"></a>

## Documentation

 | [Aide Python](https://docs.python.org/fr/3/) | 
[Aide javascript](https://javascript.info/) | 

 | [Docker](https://docs.docker.com/) | 
[Heroku](https://devcenter.heroku.com/categories/reference#command-line) | 
[SQL](https://sql.sh/) | 
[Git](https://git-scm.com/docs) | 
[Pytest](https://docs.pytest.org/en/6.2.x/contents.html) | 
[Venv](https://docs.python.org/fr/3/library/venv.html) | 
[Django](https://docs.djangoproject.com/fr/3.1/) | 
[DRF](https://www.django-rest-framework.org/) | 


