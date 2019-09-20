# django-docker

**Docker containers for django and python using djongo as a database driver.**

To build the containers you should navigate to root directory of the project and build with:

    docker build .

After that the docker containers should be builded and ready to use.
To start services execute:

    docker-compose up

Mongo database is automatically created, to access mongo-express (database ui) navigate to

    localhost:8081

And to access django project you should navigate to:

    localhost:8000

The application is already connected with created mongo db!

If you wish to start a new application you can do it with the following command, also ran in root directory:

    docker-compose run web sh -c "django-admin.py startapp nameofapp"

To create migrations run:

    docker-compose run web sh -c "python manage.py makemigrations"

And to migrate run:

    docker-compose run web sh -c "python manage.py migrate"
