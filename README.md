# API для Yatube

API для использования возможностей блога

### Описание:

Yatube - блог с возможностью публикации текстовых постов, их комментирования и подписки на любимых авторов.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке.

```
git clone https://github.com/ArtemStudenn/api-final-yatube
```

```
cd api-final-yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

### Как запустить проект:

Получение токена для аутентификации:
POST api/v1/jwt/create/
{
  "username": "username",
  "password": "password"
}

Публикация поста:
POST /api/v1/posts/
{
  "text": "Текст поста",
  "group": 1
}

Публикация комментария:
POST api/v1/posts/{post_id}/comments/
{
  "text": "Текст комментария"
}

Подписка на пользователя:
POST api/v1/follow/
{
  "following": "username автора"
}
