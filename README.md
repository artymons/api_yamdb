### Описание проекта:

YAMDB - это каталог произведений совмещённый с обширной базой публикаций о них и возможностью оставлять свои отзывы обо всём на свете.
Для возможности самостоятельного расширения каталога реализована возможность скрытого внедерения тайтлов пользователями, а для админов даны широкие права и обязанности распределённые по ролям. Присоединяйтесь или оставьте свои комментарии на века.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/artymons/api_yamdb.git
```

```
cd api_yamdb.git
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

### Примеры запросов к api:

Создание пользователя
Запрос:
/api/v1/auth/signup/
Ответ:
{
  "email": "string",
  "username": "string"
}

Получение информации о произведении
Запрос:
/api/v1/titles/{titles_id}/
Ответ:
{
  "id": 0,
  "name": "string",
  "year": 0,
  "rating": 0,
  "description": "string",
  "genre": [
    {
      "name": "string",
      "slug": "string"
    }
  ],
  "category": {
    "name": "string",
    "slug": "string"
  }
}

Получение списка всех отзывов
Запрос:
/api/v1/titles/{title_id}/reviews/
Ответ:
[
  {
    "count": 0,
    "next": "string",
    "previous": "string",
    "results": [
      {
        "id": 0,
        "text": "string",
        "author": "string",
        "score": 1,
        "pub_date": "2019-08-24T14:15:22Z"
      }
    ]
  }
]

Более подробное описание api можно найти в документации:
http://127.0.0.1:8000/redoc/
