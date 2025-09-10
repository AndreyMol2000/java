03-css-cveta-shrifty-i-teksty.md
# Цвета, шрифты и текстовые свойства в CSS

## Краткая информация
CSS позволяет управлять **визуальным оформлением текста**:

- Цвет текста и фона  
- Размер и семейство шрифта  
- Начертание, толщина, стиль  
- Межстрочные и межсимвольные интервалы  
- Выравнивание текста  

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Текстовые свойства CSS</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }

        h1 {
            color: #2c3e50;
            font-size: 36px;
            font-weight: bold;
            text-align: center;
        }

        p {
            color: #555;
            font-size: 18px;
            line-height: 1.6;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .highlight {
            background-color: yellow;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Пример заголовка</h1>
    <p>Обычный текст с <span class="highlight">выделением</span> и изменённым стилем.</p>
</body>
</html>

Подробная информация
Цвета

color — цвет текста

background-color — цвет фона элемента

Можно использовать:

Имена цветов (red, blue)

HEX (#ff0000)

RGB (rgb(255,0,0))

HSL (hsl(0, 100%, 50%))

Шрифты

font-family — семейство шрифтов

font-size — размер текста

font-weight — толщина (normal, bold, 100–900)

font-style — стиль (normal, italic, oblique)

Межстрочные и межсимвольные интервалы

line-height — высота строки

letter-spacing — расстояние между символами

Выравнивание и трансформация текста

text-align — выравнивание (left, center, right, justify)

text-transform — преобразование текста (uppercase, lowercase, capitalize)

text-decoration — подчёркивание, перечёркивание, надчёркивание

Объяснение

CSS позволяет делать текст читаемым и красивым

Цвет, шрифт и интервалы улучшают восприятие информации пользователем

Стили могут применяться к отдельным элементам через классы, ID или теговые селекторы