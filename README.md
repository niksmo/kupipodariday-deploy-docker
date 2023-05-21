# Проект «КупиПодариДай»

## Описание

Веб-приложение сервиса вишлистов.
В нём каждый зарегистрированный пользователь может рассказать о том, какой подарок он бы хотел получить, а также скинуться на подарок для другого пользователя, указав сумму, которую готов на это потратить.

### Функциональность приложения
- Регистрация и авторизация
- Просмотр главной с лентой подарков
- Добавление или изменение подарков
- Просмотр информации о подарке (чужом или своём)
- Просмотр тематических подборок
- Редактирование профиля
- Просмотр профилей и подарков других пользователей
- Поиск пользователей по имени пользователя или почте
- Копирование подарка
- Заявка для желающих скинуться на подарок

### Проект развернут на облачном сервере и доступен по URL

Бэкенд https://api.niksmo-wishlist.nomoredomains.monster

Фронтенд https://niksmo-wishlist.nomoredomains.monster

## Технологии

### Бэкенд
[![Nestjs][Nestjs-badge]][Nestjs-url]
[![Postgresql][Postgresql-badge]][Postgresql-url]
[![Nginx][Nginx-badge]][Nginx-url]
[![Docker][Docker-badge]][Docker-url]

### Фронтенд

[![React][React-badge]][React-url]
[![React-Router][React-Router-badge]][React-Router-url]

## Инструкция по деплою на сервере

Убедиться, что на сервере установлены docker и docker-compose
```shell
 docker -v && docker-compose -v
```
С инструкцией по установке, можно ознакомиться в [официальной документации](https://docs.docker.com/engine/)

1. Клонировать репозиторий

   ```shell
   git clone git@github.com:niksmo/kupipodariday-deploy-docker.git
   cd kupipodariday-deploy-docker
   ```
2. Переименовать примеры файлов окружения

  ```shell
  mv .env.example .env && mv .env.db.example .env.db && mv .env.api.example .env.api
  ```
3. Задать необходимые значения для свойств в файлах окружения `.env` `.env.db` `.env.api`

4. Собрать и запустить образы фронтенда и бэкенда с помощью docker-compose

  ```shell
  docker-compose up -d
  ```

<!-- MARKDOWN LINKS & BADGES -->

[Nestjs-url]: https://nestjs.com/
[Nestjs-badge]: https://img.shields.io/badge/NestJS-23272f?style=for-the-badge&logo=nestjs&logoColor=e93333

[Postgresql-url]: https://www.postgresql.org/
[Postgresql-badge]: https://img.shields.io/badge/postgresql-23272f?style=for-the-badge&logo=postgresql

[Nginx-url]: https://nginx.org/
[Nginx-badge]: https://img.shields.io/badge/Nginx-23272f?style=for-the-badge&logo=nginx&logoColor=00B140

[Docker-url]: https://www.docker.com/
[Docker-badge]: https://img.shields.io/badge/Docker-23272f?style=for-the-badge&logo=docker

[React-url]: https://react.dev/
[React-badge]: https://img.shields.io/badge/React-23272f?style=for-the-badge&logo=react

[React-Router-url]: https://reactrouter.com/en/main
[React-Router-badge]: https://img.shields.io/badge/React%20Router-23272f?style=for-the-badge&logo=reactrouter
