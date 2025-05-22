Инфраструктура модуля :
1. mysql  Ver 8.0.42-0ubuntu0.24.04.1 for Linux on x86_64 ((Ubuntu))
2. mysql Workbench 8.0
3. Среда разработки IntelliJ IDEA 2025.1.1.1 (тестирование, отладка, код)
4. Сборщик проекта maven
5. JDK openjdk-24.0.1
6. Java — 17
7. Основной фрэймворк Spring boot 3.4.5:
    • Spring Web
    • Thymeleaf
    • Spring Boot DevTools
    • Spring Security
    • Spring Data JPA
    • MySQL Driver
Инструкция по запуску проекта IntelliJ IDEA (Linux):
1. Создать базу данных используя скрипт структуры - файл base.sql 
2. В файле application.properties:
    • указать название базы данных (схемы), username и password от mysql
    • при необходимости поменять порт
   
   
Структура базы данных:
users:
id, name, password, telegram_token, username, enabled, authorized, chat_id

messages:
id, created_at, text, user_id


Суть сервиса:
http://localhost:8081/register
1. Регистрация нового пользователя ввод логина, имени, пароля
2. Выдача токена для бота (учет токена в базе)

http://localhost:8081/login
1. В случае наличия регистрации ввод логина и пароля
2. Показ уже выданного токена

