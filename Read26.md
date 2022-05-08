# Read: 26 - Readings: Intro to Django



## Intro to Django

> What Is Django?

*Django is a high-level Python web framework that encourages fast development and a clean, pragmatic design.*

**Install Django**
*Installing an official release with pip¶*

```
$ python -m pip install Django

```


**Features of Django**
- Fast: Django is ridiculous fast.
- Tons of Packages: Django contains set of components that helps you to develop your websites faster and easier.
- Secure: Django is highly secure as lot more work has been done there by the python web community.

- Scalable: Django has a set of good defaults and Python makes it very explicit. Also, Instagram and Disqus are two products that serve millions of users and use Django as their primary backend.

- Versatile – Django is used to build all sort of things – from content management systems to social networks to scientific computing platforms.

**Django Architecture**

* `Model` –  Model is used for storing and maintaining your data. It is the backend where your database is defined.

* `Views` – In Django templates, views are in html. View is all about the presentation and it is not at all aware of the backend. Whatever the user is seeing, it is referred to a view.

* `Controller` – Controller is a business logic which will interact with the model and the view.


**Build First Web Application in Django**

*To create a project we use the following command*

```
django-admin startproject myproject
```

*import the application manually inside your project settings*

```

INSTALLED_APPS = (
    'webapp',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
)
```

*create a view now*

```
from django.shortcuts import render
from django.http import HttpResponse
 
def index(request):
    return  HttpResponse("
 
&lt;H2&gt;HEY! Welcome to Danjo! &lt;/H2&gt;
 
 
")

```

*Now mapping this view to a URL*

```
from django.conf.urls import url
from . import views
urlpatterns = [
 url(r'^$', views.index, name='index'),
]

```

*point the root URLconf at the webapp.urls module*

```

from django.conf.urls import include, url
from django.contrib import admin
 
urlpatterns = [
    url(r'^admin/', include(admin.site.urls)),
    url(r'^webapp/', include('webapp.urls')),
]
```
*Finaly start the server*
```
python manage.py runserver
```

