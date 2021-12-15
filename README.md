# Проект Foodgram

![Workflow](https://github.com/yankovskaya-ktr/foodgram-project-react/actions/workflows/foodgram_workflow.yml/badge.svg)

Дипломный проект курса Python-разработчик от Яндекс.Практикум.

«Продуктовый помощник» — сайт, на котором можно публиковать рецепты и подписываться на публикации других авторов. Понравившиеся рецепты можно добавить в избранное. Сервис «Список покупок» позволяет скачать список продуктов, которые понадобятся для приготовления выбранных блюд.

### Доступ

http://178.154.231.118/
http://praktikum-eyank.tk/

Администратор:
admin@mail.ru
adminadmin


### Технологии
Python 3.8.5, Django 3.0.5, Django REST framework 3.12.4

### Инфраструктура
PostgreSQL, Docker, Gunicorn, Nginx

### Локальный запуск проекта:
  
Клонировать репозиторий и перейти в директорию infra/:  
  
```  
git clone https://github.com/yankovskaya-ktr/foodgram-project-react.git
cd foodgram-project-react/infra
``` 

Создать файл .env по шаблону .env.template:

```
cp .env.template .env
```
Запустить приложение:

``` 
docker-compose up
``` 
Провести миграции:

``` 
docker-compose exec web python manage.py migrate --noinput
``` 

Создать суперпользователя:

``` 
docker-compose exec web python manage.py createsuperuser
``` 

Импортировать данные в базу данных:  
  
```  
docker-compose exec web python manage.py import_data
```

### Ресурсы:

Главная страница:
```
http://localhost/
```
Документация API:
```
http://localhost/api/docs/redoc.html
```

### Автор: 
https://github.com/yankovskaya-ktr/
