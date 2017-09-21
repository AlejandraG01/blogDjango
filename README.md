# blogDjango
criação de app web de blog com Django python

You need to install virtualenv into ./blogDjango address to have a virtual environment

	$ sudo pip install virtualenv
	$ virtualenv myvenv
 
Start the virtual environment:

	$ source myvenv/bin/activate
	
You will know if you have a virtualenv started, when your console's prompt has the prefix (myvenv)

	(myvenv)~/blogDjango$ 
Then install Django:
- To install Django in localhost:
				
		(myvenv) $ pip install django~=1.9.0
	
- TO install Django in www.PythonAnywhere:

		(myvenv) $ pip install django~=1.11.0 whitenoise~=2.0
	more information https://tutorial.djangogirls.org/pt/deploy/
	
Create the Sqlite3 DATABASE (default):

	python manage.py migrate

Before to start the web server, save the application's changes in Django:
 
	(myvenv) ~/blogDjango$ python manage.py makemigrations blog
	(myvenv) ~/blogDjango$ python manage.py migrate blog

	
Start the web server:

	(myvenv)~/blogDjango$ python manage.py runserver
COnfirm that app web server was started, open de browser and write this address: 

	http://127.0.0.1:8000/admin
Create superuser to access the application:

	(myvenv) ~/blogDjango$ python manage.py createsuperuser
	Username: admin
	Email address: admin@admin.com
	Password:
	Password (again):
	Superuser created successfully.
