# api_final_yatube

### Описание

Проект добавляет возможность социальной сети Yatube  
быть интегрированной в сторонние приложения благодаря сервису REST API.

### Установка

Скопируйте проект на свой компьютер:

```
git clone https://github.com/Klyucherov/api_final_yatube.git
```

Cоздайте и активируйте виртуальное окружение для этого проекта:

```
python -m venv venv
```

```
source env/bin/activate
```

Установите зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Перейдите в директорию проекта:

```
cd yatube_api
```

Выполните миграции:

```
python manage.py migrate
```

Запустите проект:

```
python manage.py runserver
```

### Примеры

Пользователь аутентифицируется посредвстом JWTAuthentication.  
Получите токен.  
Отправьте POST запрос на URL:

```
http://127.0.0.1:8000/api/v1/auth/jwt/create/
```

Получение публикаций GET запрос:

```
http://127.0.0.1:8000/api/v1/posts/
```

Создание публикации POST запрос:

```
http://127.0.0.1:8000/api/v1/posts/
```

```
{
"text": "string"
}
```

Получение одной публикации GET запрос:

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

Обновление публикации PUT запрос:

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

```
{
"text": "string"
}
```

Частичное обновление публикации PATHС запрос:

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

```
{
"group": 0
}
```

Удаление публикации DELETE запрос:

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

### В проекте использованы технологии:

- Python
- Django
- Django REST Framework
- JWT + Djoser
