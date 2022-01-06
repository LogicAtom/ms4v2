# MS4v2 - December 15, 2021 

(Updated December 30, 2021)
Created to show Django and Python e-commerce website.

## LIVE SITE:  https://akoz-ms4v2.herokuapp.com/ 

## UPDATES
Adding TESTING PROCEDURES section with associated screenshots, and a basic description for each.<br />
Adding NEW SCREENSHOTS for the Testing Procedures section<br />
Adding CODE VALIDATION URLs<br />


## 👷 Built with these Technologies
Python3, Django, HTML5, CSS3, PostGres, AWS, STRIPE, JS.

## TESTING PROCEDURES
1. UI: Adding items to shopping bag = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/add_to_bag_working.png
2. AUTH: Authentication Error = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/checkout_auth_fail.png
3. AUTH: Successful connection with Heroku CLI = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/heroku_cli.png
4. Disabling Heroku from collection static media files, because static files are stored in AWS = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/heroku_config_set_disableCollectStatic.png
5. Pushing git to Heroku directly = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/heroku_gitPush_working.png
6. After migrating files to Heroku, Test to ensure all files made it there = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/heroku_migrations_noGo.png
7. UX: Testing to see how the landing page looks = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/main_nav_working_and_toasts_working.png
8. TEST Error with Python code = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/product_detail-add_to_bag_error.png
9. Editing products = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/product_edit.png
10. SEARCH QUERY for Specific product types = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/search_query_jeans_working.png
11. Connecting the SHOP NOW button to the Products Page = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/wire_up_shop_now_button_to_products_page.png
12. Connecting the SHOP NOW button to the Products Page (Success) = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/ShopNowButtonToProducts-Success.png
13. Adding new products via Django Administration, as shown on the project main site = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/test_django_add_product-confirm.png
14. Successful products added via Django Administration, as shown on the Django Administration = https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/test_django_add_product.png


Screenshots folder = https://github.com/LogicAtom/ms4v2/tree/main/media/screenshots
<br />

## USER STORIES
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
6. As an administrator be able to access and edit products as well as be a shopper.

(Updated January 6, 2022)
## TESTING USER STORIES
1. As a Shopper, I want to view a list of products : https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/UserStories1_asUserViewProducts.png
2. As a Shopper, I want to be able to view product details, price, description, rating, sizes, product image : 



A user cannot delete a product if they are not a superuser : https://github.com/LogicAtom/ms4v2/blob/main/media/screenshots/nonAdmin_CRUD_directLinkDelete_NoGo.png

Admin CRUD Delete direct link:
https://akoz-ms4v2.herokuapp.com/products/delete/177/ <br />


### CODE VALIDATION
 CSS = https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fakoz-ms4v2.herokuapp.com%2F&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en<br />
 https://validator.w3.org/#validate_by_input<br />
 HTML w/Errors = https://validator.w3.org/nu/?doc=https%3A%2F%2Fakoz-ms4v2.herokuapp.com%2F<br />

 
    ##### Testing Python code using Python Tutor at https://pythontutor.com/visualize.html#mode=edit
 
 

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


### Capture and save the project code libraries, so they are available to everyone who opens this project as a clone or fork :)
pip3 freeze > requirements.txt


### DJANGO - NEW PROJECT (dont forget the dot at the end!!!)
django-admin startproject ms4v2 .


### CREATE A SUPERUSER
python3 manage.py createsuperuser
(This is for the Django Administration)


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
 https://stripe.com/docs/testing#cards<br />
 

 ### WEB TOOLS
 https://fonts.google.com/<br />
 https://fontawesome.com<br />
 https://kaggle.com<br />
 https://jsonformatter.org/<br />
 https://miniwebtool.com/django-secret-key-generator/<br />
 https://www.diffchecker.com/<br />
 https://pythontutor.com/visualize.html#mode=edit


 ### ERRORS
 In case any errors happen, these are common places to figure it out:

 1.  foreign keys, products folder(app), models.py
 2.  bigautofield. *RESOLVED* via last line of code in settings.py (apparently its related to django version).


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


#### Assistant Services and Drivers
NodeJS - https://nodejs.org/en/download/ = Dependency Manager<br />
JQuery - https://jqueryui.com/ = Hamburger Mobile Side Menu<br />
Materialize CSS - https://materializecss.com/ = Enhance UI/UX<br />
Amazon Web Services - https://aws.amazon.com/ = Database Connector <br />
[Git](https://git-scm.com/ "Git") : Version Control System <br />
[GitPod](https://gitpod.io/ "GitPod") : IDE <br />
FontAwesome.com = Custom Icons<br />
Random Keygen https://randomkeygen.com/<br />
Favicon = https://www.favicon.cc/?action=icon&file_id=957941<br />
Data Modeling Software = https://dbdiagram.io/<br />

## Credits and Acknowledgements

[Code Institute](https://codeinstitute.net/ "Code Institute")Code Institute - FullStack Boot Camp - Most of the code and instructions was written by Code Institute, I cannot take credit for the code, only the customization of the code is actually mine.
<br />
Code Institute - for having me create a Python3 - Full-Stack MileStone4 project

Code Institute - Tutors for all your help..you rock!<br />
Tutors:<br />
Code Institute Tutors (Alan) = Django Admin Model and Project Migrations. :)<br />
Code Institute Tutors (Ed) = Django and Site Views and Templates. :) <br />
Code Institute Tutors (Sheryl) = Django Environment Variables., and Heroku help. :)<br />
Code Institute Tutors (Rebecca) = AWS, ACL's, Stripe Docs, and Heroku CVARs :)<br />
Code Institute - Student Care Team and Advisers..You are the most amazing people and I couldn't get this far without you!<br />

stackoverflow - For all of the custom questions and answers.

Akshat Garg - My Mentor for Software Development from Code Institute ... Thank you so very much for everything!! :)


### Educational Acknowledgements
Palmetto Goodwill - In collaboration with TTC - Grant Funder (my beautiful angels!)
<br />
Code Institute - Web Development School - You are the best Teachers!
<br />
Ed2Go/Cengage - Online Courses - You brought it all together, and offered the course. Awesome!
<br />
Charleston County Public Library - Thank you for letting me borrow around 100 books!


## 🧑🏻 Code Developer

**Anthony Kozloski**

- 🌌 [Profile](https://github.com/LogicAtom "Anthony Kozloski")
