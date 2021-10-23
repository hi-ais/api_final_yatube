# API для блога Yatube
## Задача проекта:
Создание API для упрощенной версии блога Yatube
## Описание проекта:
API реализован для всех моделей приложения posts

__Доступные эндпоинты__

| Эндпоинт | Метод | Описание|
|:---:|:----:|:----------:|
| /api/v1/jwt/create/ | POST| получение JWT-токена|
| /api/v1/jwt/refresh | POST|обновление JWT-токена|
|/api/v1/jwt/verify/|POST|Проверка JWT-токена|
|/api/v1/posts/|POST/GET| Добавление новой записи/Просмотр всех записей|
|/api/v1/posts/{id}/|GET/PUT/PATCH/DELETE|получение/обновление/частичное обновление/удаление записи|
|/api/v1/posts/{post_id}/comments/|GET/POST|Получение всех комметариев/Добавление нового комментария к посту|
|/api/v1/posts/{post_id}/comments/{comment_id}/|GET/PUT/PATCH/DELETE|получение/обновление/частичное обновление/удаление комментария|
|/api/v1/follow/|GET/POST|Получение списка всех своих подписок/ Новая подписка |
| /api/v1/group/|GET|Получение списка всех групп|
|/api/v1/group/{group_id}|GET|получение информации о группе|

## Установка проекта:
Клонировать репозиторий и перейти в него в командной строке:

`git clone https://github.com/hi-ais/api_final_yatube.git`

`cd api_final_yatube`

Cоздать и активировать виртуальное окружение:

`python -m venv env`

`source env/bin/activate`

Установить зависимости из файла requirements.txt:

`python -m pip install --upgrade pip`

`pip install -r requirements.txt`

Выполнить миграции:

`python manage.py migrate`

Запустить проект:

`python manage.py runserver`

## Примеры запросов к API 
1. Добавление новой публикации в коллекцию публикаций.

```
{
  "text": "string",
  "group": 0
}
```
2. Получение комментария к публикации по id.

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```
Полная спецификация API будет доступна после запуска проекта по адресу http://localhost:8000/redoc/.
