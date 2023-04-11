# msOptionsPrice2

Дополнительные опции товара

## Стандартные поля

| Поле         | Название             | Возможные значения |
| -------------| -------------------- |------------------- |
| name         | Название модификации |                    |
| rid          | id ресурса           |                    |
| type         | тип модификации      | `1 \|\| 2 \|\| 3`  |
| price        | Цена                 |                    |
| old_price    | Старая цена          |                    |
| article      | Артикул              |                    |
| weight       | Вес                  |                    |
| count        | Количество           |                    |
| image        | Картинка             |                    |
| active       | Активная модификация | `0 \|\| 1`         |
| modification | Опции модификации    |                    |

## Пример

**Поля импорта:** rid,article,name,price,modification

**Уникальное поле:** rid,article

**Таблица:**

![Пример](https://file.modx.pro/files/0/5/a/05a0e708fd2ff5baa6b40ba49b209362.jpg)