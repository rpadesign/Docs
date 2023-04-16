# Установка

Требования: Для установки необходимо наличие miniShop2. На сервере php 5.3.0 или выше с поддержкой модулей XML (SimpleXML, XMLReader, XMLWriter).

Установка производится через установщик транспортных пакетов. При установке создается пространство имен mSync, в которое
записываются системные настройки и плагины компонента. Так же создается несколько таблиц в БД с префиксом "msync_".

## Деинсталяция

При удалении все системные настройки и плагины из пространства msync, а так же таблицы с префиксом msync_, автоматически удалятся.

## Авторизация

Если не срабатывает авторизация, для FastCGI создайте файл .htaccess в папке /assets/components/msync/ и добавьте в него следующие строки:

```apache
RewriteEngine On
RewriteCond %{HTTP:Authorization} !^$
RewriteRule ^(.*)$ $1?http_auth=%{HTTP:Authorization} [QSA]
```

Так же может помочь, если прописать в .htaccess в корне сайта следующий код:

```apache
SetEnvIf Authorization .+ HTTP_AUTHORIZATION=
```

Пример настроек сервера **nginx**:

```nginx
location / {
  rewrite ^(.*)$ /$1?http_auth=$http_authorization;
}
```

## Первоначальная настройка для работы с CommerceML 2

Желательно перед установкой компонента иметь уже созданную и пустую «Категорию с товарами» компонента miniShop2.

Необходимо, чтобы были заполнены следующие системные настройки: «Id категории каталога (msync_catalog_root_id)», «Шаблон по умолчанию для новых категорий (msync_template_category_default)» и «Шаблон по умолчанию для новых товаров (msync_template_product_default)».

Переходим в компонент и открываем вкладку «Реквизиты синхронизации».

Переписываем параметры в 1с или сервис. Логин и пароль можно задать самостоятельно, через системные настройки.
В 1с «Администрирование» -> «Синхронизация данных» -> «Узлы обмена с сайтами»

[![](https://file.modx.pro/files/0/a/9/0a92dfc1b86b68372a8ab86e4f2b2ec5s.jpg)](https://file.modx.pro/files/0/a/9/0a92dfc1b86b68372a8ab86e4f2b2ec5s.jpg)

[![](https://file.modx.pro/files/e/8/0/e80811163a05d27971fc25bf2b5b986es.jpg)](https://file.modx.pro/files/e/8/0/e80811163a05d27971fc25bf2b5b986es.jpg)

[![](https://file.modx.pro/files/f/8/0/f8075647c55dea303f913bf8c72e3560s.jpg)](https://file.modx.pro/files/f/8/0/f8075647c55dea303f913bf8c72e3560s.jpg)

::: warning
Для правильной работы синхронизации, чтобы не было перебоев во время работы, желательно в системных настройках параметр «Лимит выполнения» (msync_time_limit) сделать минимальным. Рекомендуемое значение - 5. Значение зависит от кол-ва оперативной памяти на скрипт и времени выполнения скриптов PHP
:::