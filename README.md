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
https://github.com/AlexSterlev/Docker-Homework/main/images/nginx.png
