<p align="center">
  <img src="https://hsto.org/webt/ih/ds/fu/ihdsfuqni5apj0my18tnukzztw0.png" alt="Logo" width="128" />
</p>

# Тестовое задание Back-end Golang разработчик
*Ниже будут указаны задания разного уровня сложности, на их основе мы сможем определить ваш уровень знаний и стек технологий которым вы владеете. Данное тестового задания, определить ваши знания и заинтересованность в процессе разработки и изучения материала.*
___
## Разработка REST API (CRUD)

**Описание:** Требуется создать простой сервис для обработки поступающих на сервер запросов бронирования времени. CRUD расшифровывается как Create, Read, Update, Delete, в связи с этим ваша задача будет состоять в реализации достаточно простой базы данных с зависимостью, на любом известном вам диалекте, с двумя таблицами внутри, струкутура которых будет описана ниже. После инициализации базы данных надо будет разработать API, которое будет давать возможность с ней взаимодействовать.

## Технические требования
- Система должна быть написана на языке программирования Go
    - Предпочтительно использование средств библиотеки gorilla
- Для хранения данных используйте одну из перечисленных баз данных:
    - PostgreSQL
    - MongoDB
- API должно быть документировано с помощью инструмента Swagger
- Пароль пользователя должен быть хэширован при хранении в базе данных
- Весь проект должен быть помещен в отдельный Git репозиторий
- Проект желательно должен содержать Dockerfile для запуска в Docker
- Проект должен содержать README.md с инструкциями запуска программы

## Ниже задача будет разбита на подзадачи, которые вам предстоит выполнить:
### Основная часть:
1. Создайте модели для пользователей и бронирований.
2. Создать API для добавления нового пользователя и его удаления.
3. Создайте API для бронирования и отмены бронирования (при удалении пользователя должны удаляться все его брони).
4. Создайте API для просмотра списка бронирований.
5. Валидация полей сущности в рамках API.
6. Контейнеризация приложения при помощи Docker.
7. Создание документации по работе с API.

### Опционально:
8. Написание автоматических тестов для созданного функционала.
9. Логирование(предпочтительно использование библиотеки ozzo)

## Вводные данные для инициализации базы данных:

### Сущность: User
- `id` - уникальный идентификатор пользователя
- `username` - имя пользователя
- `password` - пароль пользователя (хэширование с помощью bcrypt)
- `created_at` - дата создания элемента
- `updated_at` - дата обновления элемента

### Сущность: Booking
- `id` - уникальный идентификатор бронирования
- `user_id` - идентификатор пользователя, производящего бронирование
- `start_time` - начала бронирования
- `end_time` - окончание бронирования

*Типы данных у полей можете выбрать самостоятельно, правильно подобранные типы будут являться большим плюсом.*