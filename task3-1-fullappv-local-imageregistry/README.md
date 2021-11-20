В данном подзадании напсаны конфиги для запуска с local image registry

$ docker run -d -p 5000:5000 --restart=always --name registry registry:2

После этого все образы загружены в локальный image registry

------------------------образ для node ---------------

$ docker tag node:alpine localhost:5000/node:alpine
$ docker push localhost:5000/node:alpine
$ docker rmi localhost:5000/node:alpine

------------------------образ для postgres ---------------

$ docker tag postgres localhost:5000/postgres
$ docker push localhost:5000/postgres
$ docker rmi localhost:5000/postgres

------------------------образ для python ---------------

$  docker tag python:3.8.3 localhost:5000/python:3.8.3
$ docker push localhost:5000/python:3.8.3
$ docker rmi localhost:5000/python:3.8.3
$ docker pull localhost:5000/python:3.8.3

-------------потом запускаем командой --------------

$ docker-compose up --build -d