# Описание

Сервис для рассылки регулярных и одноразовых уведомлений.
На данный момент реализовано уведомление по почте.
Сервис реализован по принципу pipeline, прослойками между микро-сервисами которого служат очереди RabbitMQ.

# Ссылка на репозиторий

# Авторы

* Anton Vysotskiy [@likeinlife](https://github.com/likeinlife)
* Maxim Zaitsev [@maxim-zaitsev](https://github.com/maxim-zaitsev)
* Danil Kalganov [@yandexwork](https://github.com/yandexwork)

# Запуск и остановка

## Запуск

1. `make env` - сконфигурирует один файл из environment
2. `make up` - запустить контейнеры
3. `make create-admin password=... email=...` - создать аккаунт администратора
4. `make create-user n=...` - создать тестовых пользователей, n-штук

## Остановка

- `make down` - остановить контейнеры, но не удалить volumes
- `make downv` - удалить и контейнеры, и volumes

# Тестирование

- `make test`

# URLs

1. admin panel: http://127.0.0.1/admin , login=zaitsev, password=123qwe
2. notify-api: http://127.0.0.1/notify/api/openapi
2. openapi: http://127.0.0.1/auth/api/openapi
2. mail: http://127.0.0.1:8025
