# Найти в изображениях

Эта возможность нужна в первую очередь для больших каталогов. Для не больших сайтов с 50 ресурсами она не на столько необходима потому что:

- Во время загрузки изображения, все мета данные автоматически копируеются
- Изображения групперуются по hash, то есть если у вас есть 10 одинаковых изображений загруженные в разные ресурсы, то вы увидите только одно изображение
- Возможность переноса изображений из галереи **minishop2** в **ms2Gallery** и на оборот (мета данные переносятся автоматически)
- Возможнось поиска изображения в той же категории(родительском ресурсе) где сейчас находится ресурс/товар
- возможность поиска изображений с помощью кнопок:
  - заголовок (установит заголовок в строку поиска)
  - артикул (установит заголовок в строку поиска)
  - ID ресурса (установить заголовок в строку поиска)
  - по заголовку ресурса
  - по артикулу товара
  - по наименованию изображения
  - по описанию изображения
  - Все изображения (покажи все изображения)
- Переключение поиска по галереям minishop2 и ms2Gallery в одном и том же окне

![Найти в изображениях](https://file.modx.pro/files/2/1/7/217801fe65e72e8a9e371586e836ceef.png)

Так же в модельном окне отображается количество найденых и показанных изображений

## Мета данные

В галереях miniShop2 и ms2Gallery существует возможность прописать мета данные такие как:

### Метаданные miniShop2

- **Имя файла**
- **Название**
- **Описание**

### Метаданные ms2Gallery

- **Имя файла**
- **Название**
- **Описание**
- **Альтернативное имя**
- **Дополнительно**
- **Активен**

Во время скачивания изображения просиходит автоматически перенос этих данных.

![](https://file.modx.pro/files/c/2/2/c222cd3b7b1f539d8e99264a1cf077f4.png)

::: warning
Скачивание изображений к примеру из ms2Gallery в miniShop2 не перенесет мета данные: Альтернативное имя, Дополнительно, Активен. Так как в галереи minishop2 такие поля отсутствуют**

*в ms2Gallery **Теги (Группы)**  не переносятся*
:::

### Массовая загрузка

Для массовой загрузки необходимо использовать Shift или Ctrl, затем правой кнопкой мыши и скачать

![Массовая загрузка](https://file.modx.pro/files/c/5/d/c5d820c7ca62135b0b58c6b981cd8942.png)

### Просмотр товара

Возможность просмотреть карточку товара в модельном окне загруженом через iframe

Это удобно, когда у вас возникают сомнения относительно найдено фотографии или вы обнаружили ошибку

![Просмотр товара](https://file.modx.pro/files/4/9/c/49c48323d2dbd5acf6abb595194df592.png)

### Описания изображения

У каждого изображения есть совое описание, названия.

Вы можете просмотреть их кликнув два раза мышью по изображению. Там же есть кнопка загрузить

![Описания изображения](https://file.modx.pro/files/1/b/0/1b0c0dba3fc5459129b795a91ec8bde2.png)

### Поиск по заголовку

К примеру если у вас есть товары с одинаковыми названиями, то вы можете выбрать

![](https://file.modx.pro/files/4/9/c/49c3567e509ac7f3f158c39f60e3c1b8.pn)

### Переключение между компонентами

Эта возможность позволяет скачать изображения из ms2Gallery в minishop2 или наоборот

Для поиска по таблице **ms2_resource_files** выберите **ms2Gallery**
Для поиска по таблице **ms2_product_files** выберите **minishop2**

![Переключение между компонентами](https://file.modx.pro/files/c/1/e/c1e55de955d2ec8f4ee517c7d8d7c4bc.pn)

### Изображение уже есть в галереи

Для того чтобы определить что изображение уже было загружено в галерею сравниваются hash изображений в галереи с карточко товара и с hash найденых изображений.

Для тех изображения которые у нас уже загружены подсвечивается треугльник в левой верхнем углу **такие изображения повторно грузится не будут**

![Изображение уже есть в галереи](https://file.modx.pro/files/6/b/9/6b9acf9772dd2dd967275e39984824f0.png)