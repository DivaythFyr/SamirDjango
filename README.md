# SamirDjango 
Это сайт, на котором можно выкладывать свои посты и смотреть погоду


Данный проект содержит несколько приложений: django_project, blog, users, contact, api, weatherApp.
django_project содержит settings.py и urls.py проекта


Проект подключен к PostgreSQL, это можно увидеть в разделе settings.py.


blog содержит модель Post, характеризующую посты пользователей. В этом приложении находятся большинство html шаблонов, в том числе базовый шаблон, от которого наследуется большинство шаблонов - base.html. В шаблоне home.html сверстана пагинация.


users содержит модель Profile, характеризующую профиль пользователя.  views.py написан функциональным подходом, содержит функции register и profile. register создает форму регистрации, возвращает шаблон регистрации register.html. Функция profile находится под @login_required, чтобы показать профиль только если пользователь набрал логин и пароль, выводит шаблон profile.html.


contact содержит контактную форму, чтобы пользователь мог связаться с админами. views построен на функциональном подходе. 


api содержит API построенным на фреймворке Django REST API. Он содержит сериализатор для модели Post и несколько методов @api_view, например, addPost, для того, чтобы добавлять посты в базу данных.


weatherApp построен на API для показа погоды, views.py содержит функцию index, в которой прописаны параметры погоды, которые нужно высвечивать, в качестве шаблона для http ответа используется index.html
