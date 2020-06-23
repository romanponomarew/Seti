# Лабораторная работа 1
## Задание 1
- разобрать структуру приложенного Vagrantfile
- нарисовать схему
- расписать возможные подсети

![Alt text](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/schema.png)


---
## Задание 2
- Найти свободные подсети;
- Подсчитать, сколько узлов в каждой подсети, включая свободные;
- Указать broadcast-адрес для каждой подсети;
- Проверить, нет ли ошибок при разбиении.

### Первая сеть
Подсети:

#### 192.168.2.0/26
Узлов: 62
Broadcast: 192.168.2.63

#### 192.168.2.64/26
Узлов: 62
Broadcast: 192.168.2.127

#### 192.168.2.128/26
Узлов: 62
Broadcast: 192.168.2.191

### Вторая сеть
Подсети:

#### 192.168.1.0/25
Узлов: 126
Broadcast: 192.168.1.127

#### 192.168.1.128/26
Узлов: 62
Broadcast: 192.168.1.191

#### 192.168.1.192/26
Узлов: 62
Broadcast: 192.168.1.255

### Третья сеть
Подсети:

#### 192.168.0.0/28
Узлов: 14
Broadcast: 192.168.0.15

## Задание 3

- Все серверы и роутеры должны ходить в Интернет черз inetRouter;
- Все серверы должны видеть друг друга;
- У всех новых серверов отключить дефолт на NAT (eth0), который Vagrant поднимает для связи; 
____________________________________________________________________________________________

- в README приложить скриншоты tracepath и `ip r`

### tracepath
- centralRouter
![centralRouter_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/centralRouter_tracepath.png)
- centralServer
![centralServer_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/centralServer_tracepath.png)
- inetRouter
![inetRouter_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/inetRouter_tracepath.png)
- office1Router
![office1Router_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/office1Router_tracepath.png)
- office1Server
![office1Server](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/office1Server.png)
- office2Router
![office2Router_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/office2Router_tracepath.png)
- office2Server
![office2Server_tracepath](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/tracepath1/office2Server_tracepath.png)

### ip r

- centralRouter
![centralrouter_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/centralrouter_ip_r.png)
- centralServer
![centralServer_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/centralServer_ip_r.png)
- inetRouter
![inetrouter_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/inetrouter_ip_r.png)
- office1Router
![office1Router_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/office1Router_ip_r.png)
- office1Server
![office1Server_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/office1Server_ip_r.png)
- office2Router
![office2Router_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/office2Router_ip_r.png)
- office2Server
![office2Server_ip_r](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ip_r1/office2Server_ip_r.png)

## Задание 4
- поднять nginx на officе2Server
- запретить office1Server ходить на office2Server на 80й порт, все остальные должны работать

### Nginx

![nginx](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/nginx.png)

###  Блокировка запроса на 80 порт
![port80](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/80port.png)
![ping](https://github.com/romanponomarew/Seti/blob/master/LABA1/Screenshots/ping.png)
