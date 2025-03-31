# Телеграм-бот v1.0
Приложение работает с БД PostgreSQL, развернутой в docker-контейнере.

Перед запуском приложения вам необходимо зарегистрировать своего бота и получить персональный токен, используя @BotFather.
После этого, полученный токен нужно добавить в tg_bot.properties в переменную токена.

### Запуск проекта:<br>
1. Клонировать репозиторий.
2. Перейти в папку docker и запустить docker-контейнер с БД PostgreSQL.
````
cd docker
docker compose up
````
3. При первом запуске в application.yml нужно указать настройку для создания новой базы данных:
```
hibernate.ddl-auto: create
```
В дальнейшем, приложение можно запускать с параметром update, для сохранения пользовательских данных.
4. Запустить src/main/java/com/example/Telegram_Bot/TelegramBotApplication.java в IDE.

### Что может бот:
- "/start", "Зарегистрировать пользователя в базе данных бота";
- "/help", "Получить информацию о функциях приложения";
- "/get_my_data", "Получить данные текущего пользователя";
- "/delete_my_data", "Удалить данные текущего пользователя из базы данных бота";
- "/get_all_users", "Получить данные всех пользователей, зарегистрированных в базе данных бота";
- "/get_temp", "Получить температуру в Бежецке";
- "/get_time", "Получить текущие дату и время";
- "/get_course", "Получить курс валют на текущую дату";

### Стек технологий::<br>
- Java Core
- Spring Boot
- Hibernate
- PostgreSQL
- Docker
- Apache Maven
- Lombok
- Telegrambots
- Jsoup

