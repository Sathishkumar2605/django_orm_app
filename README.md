# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Screenshot_20230129_125320](https://user-images.githubusercontent.com/119404415/215311686-a7b608da-69b2-4135-b29a-08b00d39e4c8.png)


## DESIGN STEPS

### STEP 1:
Cloning of repository.Setting up of admin and models

### STEP 2:
To make all migrations in the app. Test the server.

### STEP 3:
Include the details in the tables.

## PROGRAM


admin.py:
```
from django.contrib import admin
from.models import Employee,EmployeeAdmin

admin.site.register(Employee,EmployeeAdmin)
```
models.py:
```
from django.db import models
from django.contrib import admin



class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text="Employee ID")
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()
    email=models.EmailField()    


class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary','email') 
```
## OUTPUT

## Employee table with 10 records
![Screenshot (23)](https://user-images.githubusercontent.com/119404415/215311836-9b0989ac-c8ff-4704-bd35-e973ad98baf8.png)


## Primary key demo
![Screenshot (25)](https://user-images.githubusercontent.com/119404415/215311881-539a1582-21e5-4f00-9eb3-5668c1ad709c.png)


## RESULT
The program for Django ORM App is executed successfully.
