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
