# YATUBE_API
## Учебный демонстрационный проект

Данный репозиторий содержит API для другого учебного проекта YATUBE.
YATUBE - это платформа для блогов и публикации текстов в сообществах.

### Примеры эндпоинтов:
Получение и создание публикаций [ GET, POST }:
```
http://127.0.0.1:8000/api/v1/posts/
```
Получение публикации по id [ GET, PUT, PATCH, DEL ]:
```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Получение всех комментариев к публикации [ GET, POST ]:
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
Получение комментария к публикации по id [ GET, PUT, PATCH, DEL ]: 
```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
```
Получение списка доступных сообществ [ GET ]:
```
http://127.0.0.1:8000/api/v1/groups/
```
Получение информации о сообществе по id [ GET ]:
```
http://127.0.0.1:8000/api/v1/groups/{id}/
```
Возвращает все подписки пользователя, сделавшего запрос. Анонимные запросы запрещены [ GET, POST }:
```
http://127.0.0.1:8000/api/v1/groups/{id}/
```
Для аутентификации используется библиотека djoser. Документация и эндпоинты тут:
https://djoser.readthedocs.io/en/latest/getting_started.html
### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:v4lerdon/api_final_yatube.git
```

```
cd kittygram2plus
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

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
