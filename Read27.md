# Read: 27 - Readings: Django Models



## Django Models

> What Is Django Models?



*A Django model is the built-in feature that Django uses to create tables, their fields, and various constraints. In short, Django Models is the SQL of Database one uses with Django. SQL (Structured Query Language) is complex and involves a lot of different queries for creating, deleting, updating or any other stuff related to database. Django models simplify the tasks and organize tables into models. Generally, each model maps to a single database table.*


**Using Django Models**
*To use Django Models, one needs to have a project and an app working in it. After you start an app you can create models in app/models.py. Before starting to use a model let’s check how to start a project and create an app named geeks.py*

**Creating a Model**
`Syntax`

```
from django.db import models
        
class ModelName(models.Model):
        field_name = models.Field(**options)
```

*To create a model, in geeks/models.py Enter the code*

```
# import the standard Django Model 
# from built-in library 
from django.db import models 

# declare a new model with a name "GeeksModel" 
class GeeksModel(models.Model): 
		# fields of the model 
	title = models.CharField(max_length = 200) 
	description = models.TextField() 
	last_modified = models.DateTimeField(auto_now_add = True) 
	img = models.ImageField(upload_to = "images/") 

		# renames the instances of the model 
		# with their title name 
	def __str__(self): 
		return self.title 

```

**commands**
- `Python manage.py makemigrations`
- ` Python manage.py migrate`

**Render a model in Django Admin Interface**
*To render a model in Django admin, we need to modify app/admin.py.*

```
from django.contrib import admin 
	
# Register your models here. 
from .models import GeeksModel 
	
admin.site.register(GeeksModel) 

```




