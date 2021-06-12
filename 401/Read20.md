# Intro to Django 

## What is Django ? 
- A high level python web frame work that encourages rapid development and clean pragmatic design comes with many useful tools such as ORM (object relational mapping) , URL routing , HTML templating , form handling and unit testing .

Notes:
- Django is not a programming language , it's a web framework built in top of python.
- Django itself is not a web server , it does contain built in web server for convenience during development but it doesn't used outside of this context , it works in tandem with Apache , Ngnix when deployed.

## Get Started with django:
1. install django globally using 

    python -m pip install django or pip install django

2. install it in a virtual environment using poetry

    poetry add django 

steps: 
if you follow the first step you have to activate django server in a virtual environment using:
    -m venv ~/.virtualenvs/djangodev
    source ~/.virtualenvs/djangodev/bin/activate
if you follow step 2 , just type poetry shell to enter virtual environment which has django


### Run Django 
    django-admin startproject name
- this will create a sub directory with your project name containing some files and manage.py file.

        ├── db.sqlite3
        ├── manage.py
        └── mysite
            ├── __init__.py
            ├── asgi.py
            ├── settings.py
            ├── urls.py
            └── wsgi.py

- navigate to outer mysite project 
- python manage.py runserver

you are ready to go ...

Additional steps:
- navigate to manage.py directory and hit:
    python manage.py startapp name

you'll generate sth looks like this:

    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── migrations
    │   └── __init__.py
    ├── models.py
    ├── tests.py
    └── views.py

- add your app to your settings.py in project file name created at first

Notes: distinguish between django app and django project.

# How Django works behind the scenes.

Django’s code is open source and available to all. Django’s organization is managed by a non-profit, the DSF, with a miniscule budget. And Django code is lead by a core team of volunteers, two paid Django Fellows, and a larger group of contributors.

