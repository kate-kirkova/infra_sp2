#API_YAMDB
API-коллекция произведений, фильмов и музыки

##Стэк технологий:
Python
Django Rest Framework
Postgres
Docker

##Документация и возможности API:
Для просмотра документации используйте эндпойнт redoc/

##Как работать с проектом:
1. Скопировать репозитрий на локальный компьютер
2. Создайте .env файл в директории infra/, в котором должны содержаться следующие переменные:
DB_ENGINE=django.db.backends.postgresql
DB_NAME= # название БД\ POSTGRES_USER= # ваше имя пользователя
POSTGRES_PASSWORD= # пароль для доступа к БД
DB_HOST=db
DB_PORT=5432\

3. Из папки infra/ соберите образ при помощи docker-compose '''$ docker-compose up -d --build'''
4. Примените миграции '''$ docker-compose exec web python manage.py migrate'''
5. Соберите статику '''$ docker-compose exec web python manage.py collectstatic --no-input'''
6. Для доступа к админке не забудьте создать суперюзера '''$ docker-compose exec web python manage.py createsuperuser'''