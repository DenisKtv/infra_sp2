# Проект API YaMDb

Проект YaMDb собирает отзывы пользователей на произведения. 

_Благодаря этому проекту можно:_
- оставлять к произведениям текстовые отзывы 
- ставить произведению оценку
- комментировать отзывы других пользователей
- получить список всех произведений, категорий, жанров, комментариев, отзывов

***
### Технологии

API Yatube использует open-source технологии:
- [Python 3.7 ](https://www.python.org/downloads/release/python-379/)
- [Django REST framework 3.12](https://www.django-rest-framework.org/community/3.12-announcement/)
- [Simple JWT-аутентификация с реализацией через код подтверждения](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/)
- [Posgres](https://www.postgresql.org/docs/)
- [Docker](https://www.postgresql.org/docs/)

### Установка

- Клонируйте проект
```
git clone <ссылка>
``` 
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с файлом manage.py выполните команду:
```
python manage.py runserver
```
### Запуск приложения в контейнерах

- Из папки 'infra/' соберем образ при помощи docker-compose

```
$ docker-compose up -d --build
```

- Выполняем миграции:

```
$ docker-compose exec web python manage.py migrate
```

- Создаем суперпользователя:

```
$ docker-compose exec web python manage.py createsuperuser
```

- Собираем статику:

```
$ docker-compose exec web python manage.py collectstatic --no-input
```

### Автор

Студент Я.Практикум - _Denis Kostiv_
