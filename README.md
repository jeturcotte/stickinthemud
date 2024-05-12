# stickinthemud

Just a little project exploiting django's lovely administration prowess for the entry of various things like objects or spells found in various games, inspired by mud.arctic.org, but potentially extensible to adjustable to others.

## assumptions

- my docker compose is set up in an environment where a previously existing database is already on a local docker network
- if you are instantiation everything fresh across the board, you would define your database inline instead

## initialiation

- docker compose run stick django-admin startproject stick .
- docker compose run stick python manage.py migrate
- docker compose run stick python manage.py createsuperuser
- docker compose run stick django-admin startapp item
- go about setting up your models
- docker compose run stick python manage.py makemigrations
- docker compose run stick python manage.py migrate