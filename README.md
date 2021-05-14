# Docker-Homework
## Кастомный образ на базе alpine
Отправляем образ docker в частный репозиторий:

````
san4ez@edukation:~$ docker push san4ezshadow/alpine-nginx:1.0
````

Запускаем контейнер:

````
san4ez@edukation:~$ docker run -d -p 8081:80 san4ezshadow/alpine-nginx:1.0
````
![Image alt](https://github.com/AlexSterlev/Docker-Homework/raw/main/images/nginx.PNG)

## Управление набором из двух Docker контейнеров:
Собираем ещё один Docker контейнер
````
san4ez@edukation:~/LAB13/alpine-php$ sudo docker build -f Dockerfile -t san4ezshadow/alpine-php:1.0 .
````
Запускаем набор контейнеров:

````
san4ez@edukation:~/LAB13$ cd alpine-www/
san4ez@edukation:~/LAB13/alpine-www$ sudo docker-compose up -d
````
![Image alt](https://github.com/AlexSterlev/Docker-Homework/raw/main/images/PHP.PNG)
