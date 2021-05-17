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

## Теоретическая часть

Поддержка операционной системы виртуальной машины и контейнера Docker сильно отличается. На изображении выше вы можете видеть, что каждая виртуальная машина имеет свою гостевую операционную систему над основной операционной системой, что делает виртуальные машины тяжелыми. С другой стороны, контейнеры Docker используют общую операционную систему хоста, и поэтому они легковесны.

Совместное использование операционной системы хоста между контейнерами делает их очень легкими и помогает им загружаться всего за несколько секунд. Следовательно, накладные расходы на управление контейнерной системой очень низкие по сравнению с виртуальными машинами.

Docker контейнеры подходят для ситуаций, когда вы хотите запустить несколько приложений в одном ядре операционной системы. Но если у вас есть приложения или серверы, которые должны работать в разных версиях операционной системы, тогда требуются виртуальные машины.

![Image alt](https://github.com/AlexSterlev/Docker-Homework/raw/main/images/docker_vs_VM.png)

| Attempt | #1  | #2  |
| :---:   | :-: | :-: |
| Seconds | 301 | 283 |
