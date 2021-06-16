# Django Custom User
For a real-world project, the official Django documentation highly recommends using a custom user model instead. This provides far more flexibility down the line so, as a general rule, always use a custom user model for all new Django projects.

### Setup
To start, create a new Django project from the command line. We need to do several things:
- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called config
- make a new app accounts
- start the local web server to make sure everything working fine

### AbstractUser vs AbstractBaseUser
There are two modern ways to create a custom user model in Django: `AbstractUser` and `AbstractBaseUser`.
> `AbstractBaseUser` requires much, much more work. Seriously, don't mess with it unless you really know what you're doing
So we'll use `AbstractUser` which actually subclasses `AbstractBaseUser` but provides more default configuration.

# Django X

DjangoX can be installed via Pip, Pipenv, or Docker depending upon your setup. To start, clone the repo to your local computer and change into the proper directory.

    $ git clone https://github.com/wsvincent/djangox.git
    $ cd djangox

installing using pip:

Pip:

    $ python3 -m venv djangox
    $ source djangox/bin/activate
    (djangox) $ pip install -r requirements.txt
    (djangox) $ python manage.py migrate
    (djangox) $ python manage.py createsuperuser
    (djangox) $ python manage.py runserver
    # Load the site at http://127.0.0.1:8000