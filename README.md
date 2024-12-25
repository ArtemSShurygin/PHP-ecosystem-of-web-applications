# Вокруг PHP – экосистема веб-приложений

## ДЗ 1. Консольный PHP
![hw1_img1](./img/hw1.1.png "hw1_img1")

## ДЗ 2. Backend API
![hw2_img1](./img/hw2.1.png "hw2_img1")

## ДЗ 3. Тестирование приложений
![hw3_img1](./img/hw3.1.png "hw3_img1")
![hw3_img2](./img/hw3.2.png "hw3_img2")
![hw3_img3](./img/hw3.3.png "hw3_img3")
![hw3_img4](./img/hw3.4.png "hw3_img4")

## ДЗ 4. Продвинутое unit-тестирование
![hw4_img1](./img/hw4.1.png "hw4_img1")
![hw4_img2](./img/hw4.2.png "hw4_img2")
![hw4_img3](./img/hw4.3.png "hw4_img3")

## ДЗ 5. Кэширование в PHP
![hw5_img1](./img/hw5.1.png "hw5_img1")
![hw5_img2](./img/hw5.2.png "hw5_img2")
![hw5_img3](./img/hw5.3.png "hw5_img3")

## ДЗ 6. Очереди в PHP
![hw6_img1](./img/hw6.1.png "hw6_img1")
![hw6_img2](./img/hw6.2.png "hw6_img2")

## Команды
```
sudo apt update
sudo apt install composer
sudo apt install sqlite3
sudo apt-get install php8.2-xml
sudo apt install curl
sudo apt install php-curl

Для ДЗ 4:
sudo apt install php8.2-xdebug

Для ДЗ 5:
sudo apt install redis-server
composer require psr/simple-cache
composer require predis/predis

Для ДЗ 6:
sudo apt install rabbitmq-server
sudo rabbitmq-plugins enable rabbitmq_management
composer require php-amqplib/php-amqplib
```

Для настройки общей папки в виртуалке:
```
sudo usermod -aG vboxsf user
```

Создать конфиг в папке:
>/etc/supervisor/conf.d

```
[program:worker]
process_name=%(program_name)s_%(process_num)02d
command=php8.2 /home/reminder-bot/cur/runner -c handle_events_daemon
autostart=true
autorestart=true
user=reminder-bot
numprocs=1
redirect_stderr=true
stdout_logfile=/var/log/worker
```
