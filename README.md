# Kittygram :cat2:
_Kittygram_ — сайт, на котором пользователи могут публиковать своих кошек, их фото и цвет. Есть возможность добавлять достижения своих кошек и просматривать ленту котов на главной странице сайта.

## Содержимое
* [Локальный запуск](#локальный-запуск)
* [Технологии](#технологии)
* [Автор](#автор)


## Локальный запуск:


Клонировать репозиторий и перейти в него в командной строке:

```
git clone 
```

```
cd cat_charity_fund
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

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

Запустить проект в контейнерах через docker compose:

```
docker compose -f docker-compose-kittygram.production.yml up -d
```

```
docker compose -f docker-compose-kittygram.production.yml exec backend python manage.py migrate
```

```
docker compose -f docker-compose-kittygram.production.yml exec backend python manage.py collectstatic
```

```
docker compose -f docker-compose-kittygram.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```

Локально проект вы можете открыть:

```
http://127.0.0.1:9000/
```

## Технологии:
- Python 3.9
- Django 3.2.3
- Pillow 9.0.0
- DRF 3.12.4
- Djoser 2.1.0
- Gunicorn 20.1.0
- PostgreSQL
- Nginx
- Docker compose

## Автор
* [Макаров Пётр](https://github.com/MakarovPetr2004)


