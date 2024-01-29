# Create virtual environment
```
```

## Install django on venv
```shell
pip install django
```

# Create a [[project]]
```shell
django-admin startproject project_name
```

`project_name` can be any name you want for your project. This creates the default configuration and backbone of the web


# Create an [[app]]
```Shell
python manage.py startapp app_name
```
`app_name` can be any name you want for your app. This creates the default configuration and backbone of the web

## Creating views and updating urls

### Create [[views]]
on `\project_name\app_name\views.py` 

```python
from django.shortcuts import render
from django.http import HttpResponse


def view_name(request):
    return HttpResponse('<h><u>nicenice boi</u></h>')
```

This creates an [[http]] view when `view_name` is called. `view_name` can be any name you want to name your view. In this code, when `view_name` is called later, it returns an `HttpResponse` of possibly an [[html]] page

### Create [[urls]]
on `\project_name\app_name\urls.py` 
```python
from django.urls import path
from . import views


urlpatterns = [
    path("", views.index, name="index"),
    ]
```

`urlpatterns` is a list of directories or paths you can navigate on your [[app]]
`path(route, view, name)`
#edit

on `\project_name\project_name\urls.py` 
```python
from django.contrib import admin
from django.urls import include, path


urlpatterns = [
    path("app_name/", include("app_name.urls")),
    path("admin/", admin.site.urls),
]
```

### Create [[Web Development/Django/database|database]]
creating [[models]]
