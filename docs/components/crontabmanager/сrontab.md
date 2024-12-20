## Crontab

Задания Cron запускаются на основе созданных команд, и все запланированные задачи хранятся в базе данных.

#### Добавление команды в задачи Cron

```shell
php artisan crontab:add --command=mysupertask
```

#### Список заданий Cron

```shell
php artisan schedule:list

# ------ -------- ------------- --------------------- ----------------- ---------------------------
#  Path   Active   Crontab       Next run              Diff              Comment
# ------ -------- ------------- --------------------- ----------------- ---------------------------
#  demo   Yes      */1 * * * *   2024-11-30 05:48:00   через 6 секунд    Тестовое задание для демонстрации
# ------ -------- ------------- --------------------- ----------------- ---------------------------
```

#### Запуск текущих заданий Cron

Будут выполнены задания, которые совпадают с текущим временем.

```shell
php artisan schedule:run
# // Тестовое задание для демонстрации работы контроллера...
#
# [INFO] [1 1 * * *] mysupertask.php run
```

### Настройка времени для crontab

В административной части сайта можно настроить время для крон
[manager](http://127.0.0.1:9001/manager/?a=home&namespace=crontabmanager)

