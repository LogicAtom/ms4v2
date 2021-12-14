# MS4v2 (this is an updated version of the Original which can be found below)
https://github.com/LogicAtom/ecommerce


### USER STORIES
1. As a Shopper, I want to view a list of products, and select some to purchase.<br />
2. As a Shopper, I want to be able to view product details., price, description, rating, sizes, product image.<br />
3.     The last two user stories in the viewing and navigation category.<br />
    Are met with the presence of a navigation menu.<br />
    That allows users to quickly identify deals and special offers.<br />
    And a real-time shopping bag indicator.<br />
    That allows users to view the total amount of their purchase at any time
    in order to avoid spending too much.<br />
    Although it is possible to make purchases as a guest.<br />
    Our store will allow users to register for an account.<br />
    log in and out<br />
    And reset their password if they've forgotten it.<br />
    Logged in users will have access to a personalized user profile.<br />
    Where they can store their default payment information.<br />
    And view their order history as well as past order confirmations.<br />
    There are user story categories for sorting and searching.<br />
    purchasing and check out. and administration and store management as well<br />
    As we work through this project we'll check off the different user stories
    as we add more and more features to the site.<br />
4. Allow users to create an account and login (allauth)<br />
5. All users/shoppers to find products without having to search through all the products.<br />
6. 

### PIP INSTALLS (do these very first thing!)
pip3 install Django==3.2.9<br />
pip3 install django-allauth==0.46.0<br />
pip3 install dj-database-url==0.5.0<br />
pip3 install django-countries==7.2.1<br />
pip3 install django-crispy-forms==1.13.0<br />
pip3 install psycopg2-binary==2.9.2<br />
pip install pillow<br />
pip3 install stripe<br />
pip3 install gunicorn<br />


Occassionally, 

pip3 freeze > requirements.txt


### DJANGO - NEW PROJECT (dont forget the dot at the end!!!)
django-admin startproject ms4v2 .


### CREATE A SUPERUSER

python3 manage.py createsuperuser


### MAKE DIRECTORIES
mkdir templates<br />
mkdir templates/allauth<br />


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
python3 manage.py startapp home<br />
python3 manage.py startapp products<br />
python3 manage.py startapp bag<br />
python3 manage.py startapp checkout<br />
python3 manage.py startapp profiles<br />



We need a templates directory inside the home app.<br />
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
 https://help.heroku.com/O0EXQZTA/how-do-i-switch-branches-from-master-to-main<br />



 ### WEB TOOLS
 https://fonts.google.com/<br />
 https://fontawesome.com<br />
 https://kaggle.com<br />
 https://jsonformatter.org/<br />
 https://miniwebtool.com/django-secret-key-generator/<br />
 https://www.diffchecker.com/<br />



 ### ERRORS
 In case any errors happen, these are common places to figure it out:

 1.  foreign keys, products folder(app), models.py
 2.  


### MIGRATIONS (changes to models)
python3 manage.py makemigrations --dry-run<br />
python3 manage.py makemigrations<br />
python3 manage.py migrate --plan <!-- --plan flag, to make sure there is nothing wrong with the models --><br />
python3 manage.py migrate<br />

python3 manage.py showmigrations


### LOAD DATA (to use the fixtures)
python3 manage.py loaddata categories

python3 manage.py loaddata products

## REMINDERS
django.db.models.BigAutoField = products, apps.py = *RESOLVED* by adding this to the end of the settings.py file:  DEFAULT_AUTO_FIELD = 'django.db.models.AutoField'

django/forms/widgets/attrs.html = attributes

templates/base.html  = commented out stripe until actually used.

accounts/broken/ = displays allauth links

css > Bulma = keeps fontawesome aligned

bag/checkout-buttons.html = need to add checkout url = RESOLVED*

checkout/models.py = profiles, might cause problems as its not built yet. = WORKING*NoErrors

checkout/forms.py = attrs, args, kwargs

### LAST WORKING
old = initial Checkout app build, before adding any code<br />
new = heroku deploy<br />


