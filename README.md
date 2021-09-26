# api_final
API для взаимодействия с социальной сетью [Yatube](https://github.com/Kutaraev/api_yatube.git)

## Описание
Данный проект представляет собой API для проекта [Yatube](https://github.com/Kutaraev/api_yatube.git),
позволяющий выполнять манипуляции и выдающий доступ к следующим объектам:

1. Посты
2. Комментарии
3. Группы
4. Подписчики

Так же API позволяет аутентифицировать пользователей при помощи токенов на основе технологии [Simple JWT](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/).

## Перечень технологий, используемых в проекте

1. Python 3.8.4
2. django 2.2.6
3. djangorestframework
4. djangorestframework-simplejwt
5. Visual Studio Code

## Установка

1. Клонировать репозиторий:
```
    git clone https://github.com/Kutaraev/api_final_yatube.git
```
2. Создать виртуальное окружение:
```
    python -m venv venv
```
3. Активировать виртуальное окружение:
```
    source venv/scripts/activate
```
4. Установить зависимости из requirements.txt
```
pip install -r requirements.txt
```
5. Запустить сервер
```
команда python manage.py runseerver
```

## Примеры

В данном разделе находятся примеры взаимаодействия с API

### Посты

1. Получить список всех публикаций:
```
(GET) http://127.0.0.1:8000/api/v1/posts/
```
2. Создать новую публикацию:
```
(POST) http://127.0.0.1:8000/api/v1/posts/
```
3. Получить публикацию по id:
```
(GET) http://127.0.0.1:8000/api/v1/posts/{id}/
```
4. Обновить публикацию по id:
```
(PUT) http://127.0.0.1:8000/api/v1/posts/{id}/
```
5. Частично обновить публикацию по id:
```
(PATCH) http://127.0.0.1:8000/api/v1/posts/{id}/
```
6. Удалить публикацию по id:
```
 (DELETE) http://127.0.0.1:8000/api/v1/posts/{id}/
```

### Комментарии

1. Получить список всех комментариев публикации:
```
(GET) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
2. Создать новый комментарий для публикации:
```
(POST) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
3. Получить комментарий для публикации по id:
```
(GET) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{comment_id}/
```
4. Обновить комментарий для публикации по id:
```
(PUT) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{comment_id}/
```
5. Частично обновить комментарий для публикации по id:
```
(PATCH) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{comment_id}/
```
6. Удалить комментарий для публикации по id:
```
(DELETE) http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{comment_id}/
```

### Подписки

1. Получить список всех подписчиков:
```
(GET) http://127.0.0.1:8000/api/v1/follow/
```
2. Создать подписку:
```
(POST) http://127.0.0.1:8000/api/v1/follow/
```

### Группы
1. Получить список всех групп:
```
(GET) http://127.0.0.1:8000/api/v1/group/
```
2. Создать новую группу:
```
(POST) http://127.0.0.1:8000/api/v1/group/
```

### Аутентификация
1. Получить JWT-токен:
```
(POST) http://127.0.0.1:8000/api/v1/token/
```
2. Обновить JWT-токен:
```
(POST) http://127.0.0.1:8000/api/v1/token/refresh/
```
