# API для Yatube

API для использования возможностей блога с возможностью публикации текстовых постов, их комментирования и подписки на любимых авторов - Yatube.

---

## Технологический стек

- Python
- Django
- Django REST Framework
- SimpleJWT
- SQLite

---

## Запуск проекта

```
git clone https://github.com/ArtemStudenn/api-for-yatube

cd api-for-yatube/

python -m venv venv

source venv/Scripts/activate  # Windows
source venv/bin/activate  # MacOS/Linux

pip install -r requirements.txt

python manage.py migrate

python manage.py runserver
```

### Примеры запросов:

Получение токена для аутентификации:
```
POST api/v1/jwt/create/
```
```
{
  "username": "username",
  "password": "password"
}
```

Публикация поста:
```
POST /api/v1/posts/
```
```
{
  "text": "Текст поста",
  "group": 1
}
```

Публикация комментария:
```
POST api/v1/posts/{post_id}/comments/
```
```
{
  "text": "Текст комментария"
}
```

Подписка на пользователя:
```
POST api/v1/follow/
```
```
{
  "following": "username автора"
}
```

### Подробная документация с примерами: [http://127.0.0.1:8000/redoc/](http://127.0.0.1:8000/redoc/)

---

## Автор

[Студенников Артем](https://github.com/ArtemStudenn)
