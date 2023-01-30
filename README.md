# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![output](./erpimage.png)
## DESIGN STEPS

### STEP 1:

An Django application is created inside dataproject folder.
### STEP 2:

A python program is written to create a table to store and retrieve data.
### STEP 3:

The table is created with 6 fields in which the username field is made as PrimaryKey.
### STEP 4:

Then the project files migrated. A superuser is also created.
### STEP 5:

Now the server side program is executed .
### STEP 6:

The admin page of our website is accessed using username and password.
### STEP 7:

Records are added and saved in the table inside the database.

## PROGRAM
```python

from django.db import models
from django.contrib import admin
# Create your models here.

class Database(models.Model):
    Patient_id = models.CharField(max_length=8, primary_key=True ,help_text="Your Patient id")
    Patient_name = models.CharField(max_length=100)
    Patient_age = models.IntegerField()
    email = models.EmailField()
    Contact_number = models.IntegerField()

class PatientAdmin(admin.ModelAdmin):
    list_display = ('Patient_id','Patient_name','Patient_age','email','Contact_number')

```
## OUTPUT

![outout](./djangopage.png)

## RESULT
Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).
