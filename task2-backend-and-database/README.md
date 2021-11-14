1. database password, login and name desfcribed in .env file
2. Dockerfile located in "lib_catalog" folder
3. Also updated ./lib_catalog/settings.py database connection settings
4. When container started, had to login to django container and run "python manage.py createsuperuser" to set up admin use for django.
