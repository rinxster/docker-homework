# pull official base image
FROM python:3.8.3
# set work directory
WORKDIR ./lib_catalog
# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
# install dependencies
RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r requirements.txt
# copy project
COPY . .
EXPOSE 8000
#COPY ./script.sh /
#RUN chmod +x /script.sh
#ENTRYPOINT ["/script.sh"]

#ENV DJANGO_DB_NAME=django
#ENV DJANGO_SU_NAME=admin
#ENV DJANGO_SU_EMAIL=admin@my.company
#ENV DJANGO_SU_PASSWORD=admin

#RUN python -c "import django; django.setup(); \
#   from django.contrib.auth.management.commands.createsuperuser import get_user_model; \
#   get_user_model()._default_manager.db_manager('$DJANGO_DB_NAME').create_superuser( \
#   username='$DJANGO_SU_NAME', \
#   email='$DJANGO_SU_EMAIL', \
#   password='$DJANGO_SU_PASSWORD')"

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]






#FROM python:3.8.3-alpine

#RUN apt-get update \
#    && apt-get install -y --no-install-recommends \
#        postgresql-client \
#    && rm -rf /var/lib/apt/lists/*

#WORKDIR /usr/src/app
#WORKDIR /lib_catalog

#COPY requirements.txt ./
#RUN pip install -r requirements.txt
#COPY . .

#EXPOSE 8000
#CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
