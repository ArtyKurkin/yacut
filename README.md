# Сервис YaCut
[![Python](https://img.shields.io/badge/-Python-464646?style=flat&logo=Python&logoColor=ffffff&color=043A6B)](https://www.python.org/)
[![SQLAlchemy](https://img.shields.io/badge/-SQLAlchemy-464646?style=flat&logo=SQLAlchemy&logoColor=ffffff&color=043A6B)](https://www.postgresql.org/)
[![Flask](https://img.shields.io/badge/-Flask-464646?style=flat&logo=Flask&logoColor=ffffff&color=043A6B)](https://www.djangoproject.com/)
[![REST](https://img.shields.io/badge/-REST-464646?style=flat&logo=REST&logoColor=ffffff&color=043A6B)](https://www.django-rest-framework.org/)


## Описание:
#### Проект YaCut позволяет с помощью WEB-интерфейса и REST API ассоциировать длинную пользовательскую ссылку с короткой, которую предлагает сам пользователь или предоставляет сервис.

### Ключевые возможности сервиса:

- генерация коротких ссылок и связь их с исходными длинными ссылками,

- переадресация на исходный адрес при обращении к коротким ссылкам.

### Автор проекта:

[Артем Куркин](https://github.com/ArtyKurkin)

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/ArtyKurkin/yacut.git
```

```
cd yacut
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

* Если у вас Linux/macOS:

    ```
    source venv/bin/activate
    ```

* Если у вас windows:

    ```
    source venv/scripts/activate
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
flask db upgrade
```

Запустить проект:

```
flask run
```

### Примеры запросов:

* `api/id/` - POST-запрос на создание новой короткой ссылки;
```
{
  "url": "string",
  "custom_id": "string"
}
```
* `api/id/<short_id>/` — GET-запрос на получение оригинальной ссылки по указанному короткому идентификатору.
```
{
  "url": "string",
  "short_link": "string"
}
```
