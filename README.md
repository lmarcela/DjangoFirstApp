1) Descargar python: https://www.python.org/downloads/
2) Al instalar activar la opcion de añadir al path
3) En cmd instalar django con el comando:
	python -m pip install django
	
4)Instalar virtual environment para poder hacer entornos virtuales:
	python -m pip install virtualenv

5)Para saber que paquetes hay instalados:
	python -m pip freeze

6) En la carpeta que queramos crear un entorno se ejecuta ejemplo:
	E:\PYTHON\DJANGO\ambientes>python -m venv test19
	
7) Para activar el entorno hacer algo similar a:
	E:\PYTHON\DJANGO\ambientes\test19\Scripts>activate
	(test19) E:\PYTHON\DJANGO\ambientes\test19\Scripts>python -m pip freeze

	(test19) E:\PYTHON\DJANGO\ambientes\test19\Scripts>


8) Para instalar django de manera virtual, entonces:
	(test19) E:\PYTHON\DJANGO\ambientes\test19\Scripts>
	(test19) E:\PYTHON\DJANGO\ambientes\test19\Scripts>cd ..

	(test19) E:\PYTHON\DJANGO\ambientes\test19>python -m pip install django
	Collecting django
	  Using cached Django-2.0-py3-none-any.whl
	Collecting pytz (from django)
	  Using cached pytz-2017.3-py2.py3-none-any.whl
	Installing collected packages: pytz, django
	Successfully installed django-2.0 pytz-2017.3

	(test19) E:\PYTHON\DJANGO\ambientes\test19>python -m pip freeze
	Django==2.0
	pytz==2017.3

	(test19) E:\PYTHON\DJANGO\ambientes\test19>

9) Para desactivar el entorno:
	(test19) E:\PYTHON\DJANGO\ambientes\test19>deactivate
	E:\PYTHON\DJANGO\ambientes\test19>

10) Empezar un proyecto en el ambiente:
	E:\PYTHON\DJANGO\ambientes\test19\Scripts>activate
	(test19) E:\PYTHON\DJANGO\ambientes\test19\Scripts>cd ..

	(test19) E:\PYTHON\DJANGO\ambientes\test19>cd ..

	(test19) E:\PYTHON\DJANGO\ambientes>cd ..

	(test19) E:\PYTHON\DJANGO>cd proyectos

	(test19) E:\PYTHON\DJANGO\proyectos>django-admin.py startproject Test

11) Instalar cliente para mysql:
	(test19) E:\PYTHON\DJANGO\proyectos\Test>pip install mysqlclient

12) Verificar lo instalado en el ambiente:
	(test19) E:\PYTHON\DJANGO\proyectos\Test>python -m pip freeze
	Django==2.0
	mysqlclient==1.3.12
	pytz==2017.3
	
13) Crear en mysql la bd vacia pruebadjango

14) E:\PYTHON\DJANGO\proyectos\Test\Test. En setting.py modificar la base de datos:

	DATABASES = {
		'default': {
			'ENGINE': 'django.db.backends.mysql', 
			'NAME': 'pruebadjango',
			'USER': 'root',
			'PASSWORD': 'root',
			'HOST': 'localhost',   # Or an IP Address that your DB is hosted on
			'PORT': '3307',
		}
	}
	
14) Ejecutar la migracion (Lo guarda en la tabla pruebadjango)
	(test19) E:\PYTHON\DJANGO\proyectos\Test>manage.py migrate

15) Crear un superusuario: manage.py createsuperuser
	user: marcela; password: abcdmarcela.
	
	(test19) E:\PYTHON\DJANGO\proyectos\Test>manage.py createsuperuser
	Username (leave blank to use 'marcela'):
	Email address: marcela9409@gmail.com
	Password:
	Password (again):
	The password is too similar to the email address.
	Password:
	Password (again):
	This password is too short. It must contain at least 8 characters.
	This password is too common.
	Password:
	Password (again):
	Superuser created successfully.
	
16) Correr el servidor: manage.py runserver
	(test19) E:\PYTHON\DJANGO\proyectos\Test>manage.py runserver
	Performing system checks...

	System check identified no issues (0 silenced).
	December 25, 2017 - 16:20:05
	Django version 2.0, using settings 'Test.settings'
	Starting development server at http://127.0.0.1:8000/

17) Comprobar http://localhost:8000/
	http://localhost:8000/admin/
	Entrar usuario y contraseña (user: marcela; password: abcdmarcela)
	
18) 
	
