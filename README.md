# django-docker
Python and django docker setup

To build navigate to django-docker path and build with
docker build .

After that the docker containers should be builded.

To run the containers execute

docker-compose up

Mongo db is automatically created, to access mongo express navigate to

localhost:8081

To access django project navigate to

localhost:8000

The application is already connected with created mongo db.

To start a new app do it with
docker-compose run web sh -c "django-admin.py startapp nameofapp"

To create migrations
docker-compose run web sh -c "python manage.py makemigrations"

To migrate
docker-compose run web sh -c "python manage.py migrate"
