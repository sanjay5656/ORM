# Ex02 Django ORM Web Application
## Date: 14/05/2021


## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
### Models.py
```python
from django.db import models
from django.contrib import admin

class Railway(models.Model):    
    Train_no = models.IntegerField(primary_key=True)
    Train_name = models.CharField(max_length=50)
    Start_station_code = models.CharField(max_length=20)
    End_station_code = models.CharField(max_length=20)
    Start_date = models.DateTimeField()
    End_date = models.DateTimeField() 
 
class RailwayAdmin(admin.ModelAdmin):
    list_display = ('Train_no','Train_name','Start_station_code','End_station_code','Start_date','End_date')

```
### Admin.py
```python
from django.contrib import admin
from .models import Railway, RailwayAdmin

admin.site.register(Railway, RailwayAdmin)
```

## OUTPUT

![alt text](<Screenshot 2024-03-14 225545.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully.
