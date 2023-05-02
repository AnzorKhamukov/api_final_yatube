# api_final

# Установка
>1.Клонировать репозиторий:
>>>git clone git@github.com:AnzorKhamukov/api_final_yatube.git

>2.Перейти в папку с проектом:

>>>cd api_final_yatube/

>3.Установить виртуальное окружение для проекта:
>>>python -m venv venv

>4.Активировать виртуальное окружение для проекта:

>>>для OS Lunix и MacOS

>>>source venv/bin/activate

>>>для OS Windows

>>>source venv/Scripts/activate

>5.Установить зависимости:

>>>python3 -m pip install --upgrade pip
>>>pip install -r requirements.txt

>6.Выполнить миграции на уровне проекта:

>>>cd yatube
>>>python3 manage.py makemigrations
>>>python3 manage.py migrate

>7.Запустить проект:

>>>python manage.py runserver

# Функционал

+ Подписка и отписка от авторизованного пользователя;
+ Авторизованный пользователь просматривает посты, создаёт новые, удаляет и изменяет их;
+ Просмотр сообществ;
+ Комментирование, просмотр, удаление и обновление комментариев;
+ Фльтрация по полям.

# Примеры запросов

Получение токена

Отправить POST-запрос на адрес api/v1/jwt/create/ и передать 2 поля в data:
```
username - имя пользователя. 

password - пароль пользователя.
```
Отправить POST-запрос на адрес api/v1/posts/ и передать обязательное поле text, в заголовке указать Authorization:Bearer <токен>.
## Пример запроса
```
{
  "text": "Мой первый пост."
}
```
## Пример ответа:

```
{
  "id": 2,
  "author": "leo",
  "text": "текст поста.",
  "pub_date": "дата создания поста",
  "image": null,
  "group": null
}
```
# Документация проэкта
~~~
http://127.0.0.1:8000/redoc/
~~~
# По для тестирования APi
~~~
https://www.postman.com/
~~~



![logo](https://www.programming-hero.com/blog/assets/images/blog/blog-24-python-django.png)
