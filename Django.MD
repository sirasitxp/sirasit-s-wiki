## Create Virtual Environment
virtualenv --python=/usr/bin/python3.8 .

## Activate 
source bin/activate

## Deactivate
deactivate

## Pip freeze for checking installed libraries
pip freeze

## Install Django
pip install django==[version]


## Create new project
django-admin startproject [project_name] .

## Run project
python manage.py runserver

## Settings.py
import OS -> So that it works in every Operating System.    
BASE_DIR -> It gives direction to where manage.py is  

## Apply changes to modules
python manage.py migrate

## Create admin 
python manage.py createsuperuser

## App Components
It's a smaller part of your web app

## Creating app component
python manage.py startapp
