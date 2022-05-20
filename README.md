<h1>Развертывание приложения написанного на React и Node.js на сервере с помощью PM2 и Nginx</h1>
Цель этой статьи — задокументировать мой путь по процессу развертывания Frontend и Backend на одном компьютере с Linux (вместе с балансировщиком нагрузки).

<h2>Установка необходимых компонентов</h2>
Обратите внимание, что эти инструкции действительны для Ubuntu 16 или более поздней версии.

<h2>Node.js</h2>
Установим nodejs:
```
$ sudo apt install nodejs
```

Проверим что установка nodejs прошла успешно:
```
$ node --version
```
<h2>Nginx (веб-сервер, обратный прокси и балансировка нагрузки)</h2>

Обновим все пакеты/программы Ubuntu
```
$ sudo apt-get update
```

Установим Nginx:
```
$ sudo apt-get install nginx
```

Проверим что установка Nginx прошла успешно:
```
$ sudo nginx -v
```

Запустим Nginx:
```
$ sudo nginx
```

Убедимся, что Nginx запущен и работает:
```
$ curl -I 127.0.0.1
```

<h2>NPM (пакетный менеджер Node.js)</h2>

Установим NPM:
```
$ sudo apt install npm
```

Проверим что установка NPM прошла успешно:
```
$ npm -v
```
<h2>PM2 (менеджер процессов для Nodejs)</h2>

Установим PM2:
```
$ npm install pm2@latest -g
```

Проверим что установка PM2 прошла успешно:
```
$ pm2 -v
```

<h2>Certbot (клиент, который получает бесплатный сертификат SSL от Let’s Encrypt)</h2>
Убедимся, что версия snap обновлена:
```
$ sudo snap install core; sudo snap refresh core
```

Установим Certbot:
```
$ sudo snap install --classic certbot
```

Проверим что установка Certbot прошла успешно:
```
$ sudo ln -s /snap/bin/certbot /usr/bin/certbot
```





