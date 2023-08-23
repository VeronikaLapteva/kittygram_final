# Проект Kittygram
Проект Kittygram позволяет регистрироваться на сайте ***https://kittygramlbee.chickenkiller.com***, входить под своим аккаунтом, добавлять, редактировать и удалять информацию по котикам (фотография, год рождения, цвет кота, умения), а также просматривать записи других пользователей.

## Технологии проекта
Python 3.10, Django3, Nginx, Gunicorn, React, Django REST framework, Certbot, Docker

## Как запустить проект на сервере:
 - Клонируем проект https://github.com/VeronikaLapteva/kittygram_final.git
 - Подключаемся к удаленному серверу и создаем на нем папку под названием kittygram
 - Устанавливаем Nginx
   ```
   sudo apt install nginx -y
   sudo systemctl start nginx
   ```
 - Через редактор Nano открываем файл конфигурации веб-сервера и вписываеми необходимые настройки:
   ```
   sudo nano /etc/nginx/sites-enabled/default
   ```
 - Устанавливаем Cerbot и получаем SSL-сертификат
   ```
   sudo apt install snapd
   sudo certbot --nginx
   ```
- Копируем файлы docker-compose.yml и .env (создаем и заполняем по примеру показанному в файле .env.example) в папку проекта kittygram
- Запускаем прооет на сервере в контейнерах
  ```
  sudo docker compose -f docker-compose.yml up -d
  ```
- Проверяем все ли контейнеры запущены
  ```
  sudo docker compose -f docker-compose.yml ps
   ```
- Проверяем доступность приложения в браузере по ссылке  ***https://kittygramlbee.chickenkiller.com***, регистрируемся и добавляем новых котиков

## Автор
Лаптева Вероника  
