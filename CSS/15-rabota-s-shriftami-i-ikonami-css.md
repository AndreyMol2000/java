# Работа с шрифтами и иконочными библиотеками в CSS

## Краткая информация
Шрифты и иконки позволяют **делать интерфейсы красивыми и читаемыми**, а также добавляют визуальные подсказки.  
В CSS можно использовать **встроенные шрифты**, подключать внешние через `@font-face` или подключать иконочные библиотеки (например, Font Awesome, Material Icons).

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Шрифты и иконки</title>
    <!-- Подключение иконочной библиотеки Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Подключение кастомного шрифта через @font-face */
        @font-face {
            font-family: 'MyCustomFont';
            src: url('fonts/MyCustomFont.woff2') format('woff2'),
                 url('fonts/MyCustomFont.woff') format('woff');
            font-weight: normal;
            font-style: normal;
        }

        body {
            font-family: 'MyCustomFont', Arial, sans-serif;
            font-size: 16px;
            line-height: 1.5;
        }

        .icon {
            font-size: 24px;
            color: #3498db;
            margin-right: 10px;
        }

        h1 {
            font-family: 'Arial', sans-serif;
            color: #2c3e50;
        }
    </style>
</head>
<body>
    <h1><i class="fas fa-star icon"></i>Заголовок с иконкой</h1>
    <p>Это текст с кастомным шрифтом.</p>

    <!-- Иконки из Font Awesome -->
    <i class="fas fa-home icon"></i> Дом
    <i class="fas fa-envelope icon"></i> Почта
    <i class="fas fa-user icon"></i> Пользователь
</body>
</html>
Подробная информация
Работа с шрифтами
Встроенные шрифты

font-family: Arial, sans-serif;

Используются шрифты, которые есть на устройстве пользователя

Подключение внешних шрифтов

Через Google Fonts

Через @font-face для локальных файлов

Свойства шрифтов

font-size — размер текста

font-weight — толщина (normal, bold, 100-900)

font-style — стиль (normal, italic)

line-height — межстрочный интервал

Иконочные библиотеки
Font Awesome — популярная библиотека иконок

Material Icons — иконки от Google

Использование: подключение через <link> или npm-пакеты

Вставка иконки через тег <i> или <span> с соответствующим классом

Стилизация иконок через CSS (color, font-size, margin)

Объяснение
Подключение кастомных шрифтов делает дизайн уникальным и современным

Иконки облегчают восприятие информации и улучшают UX

Используя и шрифты, и иконки, можно создавать красивые, читаемые и понятные интерфейсы без использования изображений

Комбинируя CSS-свойства и библиотеки, можно полностью контролировать визуальную часть сайта