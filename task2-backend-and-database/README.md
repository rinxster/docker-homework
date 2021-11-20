1. database password, login and name desfcribed in .env file
2. Dockerfile located in "lib_catalog" folder
3. Also update ./lib_catalog/settings.py database connection settings before you build your image
4. run "docker-compose up -d" to build images and start containers
5. When container started, had to login to django container and run "python manage.py createsuperuser" to set up admin use for django.
6. When all is in place you can open and check django console http://<youraddress>:8000 and also long using user created in previous step http://<youraddress>:8000/admin
