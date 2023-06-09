# Селекторы

В данном разделе находится информация о селекторах, с которыми взаимодействует компонент **FetchIt**.

## `data-fetchit`

Данный селектор добавляется элементу формы сниппетом. Он позволяет компоненту обрабатывать только нужные формы не нарушая поведения остальных форм на странице.

:::info Подсказка
Сниппет во время загрузки чанка ищет форму и в случае отсутствия данного атрибута самостоятельно устанавливает его.
:::

```html
<form action="#" method="post" data-fetchit="*">
  ...
</form>
```

## `data-error`

Указав в зачении данного атрибута название поля, т.е. то же значение что в атрибуте `name` вы указываете компоненту подгружать текст ошибки конкретного поля.

```html
<input type="text" name="username" />
<span data-error="username"></span>
```

## `data-custom`

По умолчанию **FetchIt** добавляет CSS классы из системной настройки `fetchit.frontend.input.invalid.class` элементам полей ввода, но бывают случаи, когда из-за особенности вёрстки нужно добавлять их другим элементам, например элементам-обёрткам и для таких случаев есть данный селектор и системная настройка `fetchit.frontend.custom.invalid.class`.

```html
<div class="input-parent" data-custom="password">
  <input type="password" name="password" />
</div>
```