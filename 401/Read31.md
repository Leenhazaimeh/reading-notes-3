# REST Framework & Docker

### Docker
Docker is as Linux containers which are a type of virtualization.
Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

### Containers vs Virtual Environments
Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.
But , virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.
Also we cannot run a production database or other services within virtual environments so compared to Docker containers are far more limited.
### Install Docker
after downloading and installing Once Docker is done installing we can confirm the correct version is running. It should be at least version 19.
```
$ docker --version
Docker version 19.03.5, build 633a0ea
```
Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command 
`sudo pip install docker-compose` after your Docker installation is complete.
To confirm Docker installed correctly we can run our first command `docker run hello-world`
This will download an official image and then run the container.
Want to inspect just the current image?
`docker image ls`

### Images and Containers
When we run hello-world we used an official Docker image. We did not have to create the image ourselves. But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.
A baking analogy we can use here is as follows:
A Dockerfile is the recipe for a cake
- An image is a snapshot of the recipe at a given time
- A docker-compose.yml says how to make the cake
- And the container is the actual, baked 



### Django REST Framework
On the command line type the below.
    ```
    pipenv install djangorestframework~=3.11.0
    ```
Add it to the `INSTALLED_APPS` config in our `settings.py` file. I like to make a distinction between third-party apps and local apps as follows since the number of apps grows quickly in most projects.
    ```
    # config/settings.py
    INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        # 3rd party
        'rest_framework', # new
        # Local
        'books',
    ]
    ```
There are multiple ways we can organize these files however my preferred approach is to create a dedicated api app. That way even if we add more apps in the future, each app can contain the models, views, templates, and urls needed for dedicated webpages, but all API-specific files for the entire project will live in a dedicated api app.
Let’s first create a new api app.
    ```
    python manage.py startapp api
    ```
Then add it to `INSTALLED_APPS`
The api app will not have its own database models so there is no need to create a `migration` file and run migrate to update the database.
- URLs:
First at the project-level we need to `include` the `api` app and configure its URL route,which will be `api/`.
Then create a `urls.py` file within the api app
`touch api/urls.py` And update it as follows:
    ```
    from django.urls import path
    from .views import BookAPIView
    urlpatterns = [
        path('', BookAPIView.as_view()),
    ]
    ```
- Views:
Next up is our views.py file which relies on Django REST Framework’s built-in generic class views. These deliberately mimic traditional Django’s generic class-based views in format, but they are not the same thing.
Within our views.py file, update it to look like the following:
    ```
    from rest_framework import generics
    from books.models import Book
    from .serializers import BookSerializer
    class BookAPIView(generics.ListAPIView):
        queryset = Book.objects.all()
        serializer_class = BookSerializer
    ```
Then we create a BookAPIView that uses ListAPIView to create a read-only endpoint for all book instances. There are many generic views available and we will explore them further in later chapters.
The only two steps required in our view are to specify the queryset which is all available books, and then the serializer_class which will be `BookSerializer`.
