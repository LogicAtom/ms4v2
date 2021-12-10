# SOURCE (this is an updated version of the Original which can be found below)
https://github.com/LogicAtom/ecommerce


### USER STORIES
1. As a Shopper, I want to view a list of products, and select some to purchase.
2. As a Shopper, I want to be able to view product details., price, description, rating, sizes, product image.
3.     The last two user stories in the viewing and navigation category.
    Are met with the presence of a navigation menu.
    That allows users to quickly identify deals and special offers.
    And a real-time shopping bag indicator.
    That allows users to view the total amount of their purchase at any time
    in order to avoid spending too much.
    Although it is possible to make purchases as a guest.
    Our store will allow users to register for an account.
    log in and out
    And reset their password if they've forgotten it.
    Logged in users will have access to a personalized user profile.
    Where they can store their default payment information.
    And view their order history as well as past order confirmations.
    There are user story categories for sorting and searching.
    purchasing and check out. and administration and store management as well
    As we work through this project we'll check off the different user stories
    as we add more and more features to the site.
4. Allow users to create an account and login (allauth)
5. All users/shoppers to find products without having to search through all the products.
6. 

### PIP INSTALLS (do these very first thing!)
pip3 install Django==3.2.9
pip3 install django-allauth==0.46.0
pip3 install dj-database-url==0.5.0
pip3 install django-countries==7.2.1
pip3 install django-crispy-forms==1.13.0
pip3 install psycopg2-binary==2.9.2
pip install pillow


Occassionally, 

pip3 freeze > requirements.txt


### DJANGO - NEW PROJECT (dont forget the dot at the end!!!)
django-admin startproject ms4v2 .


### CREATE A SUPERUSER

python3 manage.py createsuperuser


### MAKE DIRECTORIES
mkdir templates
mkdir templates/allauth


### COPY PATH
To find your allauth path in Terminal type:

python


then type:

help('allauth')



allauth will display an ASCII logo and info about your path :)

__________________________________________


Update the provided command with the path you just copied. eg: cp -r [your site-package path]/allauth/templates/* ./templates/allauth/

#### Next step
right click on templates directory, and create base.html file. Will use BootStrap Starter Template.

### BOOTSTRAP
https://getbootstrap.com/docs/4.4/getting-started/introduction/#starter-template

### CREATE NEW APPS
python3 manage.py startapp home
python3 manage.py startapp products


We need a templates directory inside the home app.
So let's use 

mkdir -p home/templates/home

  to create parents as required.

  and then right click on inner home directory and right click to create a new file named:  index.html


mkdir static

mkdir media

mkdir static/css

new file base.css


mkdir -p products/templates/products (so Django knows which app these belong to, don't type this parenthesis text or parenthesis)



 ### CREATE VIEWS
 views.py

 views.py is the file used to render new files


 ### RESOURCES
 Shopping Bags - Background Image

 https://i5.walmartimages.com/asr/ca405873-3b81-4bb6-9c13-28ce98338bc5_1.5dce4e895ef268cd3466944771780ffc.jpeg


 ### WEB TOOLS
 https://fonts.google.com/
 https://fontawesome.com
 https://kaggle.com
 https://jsonformatter.org/


 ### ERRORS
 In case any errors happen, these are common places to figure it out:

 1.  foreign keys, products folder(app), models.py
 2.  


### MIGRATIONS (changes to models)
python3 manage.py makemigrations --dry-run
python3 manage.py makemigrations
python3 manage.py migrate --plan <!-- --plan flag, to make sure there is nothing wrong with the models -->
python3 manage.py migrate


### LOAD DATA (to use the fixtures)
python3 manage.py loaddata categories

python3 manage.py loaddata products

## REMINDERS
django.db.models.BigAutoField = products, apps.py

django/forms/widgets/attrs.html = attributes