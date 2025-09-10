CSS Grid: основы и свойства

## Краткая информация
Grid — это мощный инструмент для **создания сложных двухмерных макетов**. Позволяет управлять как строками, так и столбцами контейнера.  

- Контейнер `display: grid`  
- Элементы внутри становятся **grid-элементами**  
- Удобно создавать адаптивные и структурированные макеты  

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Grid пример</title>
    <style>
        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* три равные колонки */
            grid-gap: 10px; /* расстояние между элементами */
            background-color: #ecf0f1;
            padding: 10px;
        }

        .item {
            background-color: #3498db;
            color: white;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">5</div>
        <div class="item">6</div>
    </div>
</body>
</html>
Подробная информация
Свойства контейнера
display: grid — превращает блок в grid-контейнер

grid-template-columns / grid-template-rows — задают колонки и строки

grid-gap (или gap) — расстояние между элементами

grid-template-areas — именованные области для размещения элементов

Свойства элементов
grid-column — позиция элемента по колонкам

grid-row — позиция элемента по строкам

justify-self / align-self — выравнивание элемента внутри ячейки

Объяснение
Grid позволяет легко создавать сетки и макеты любой сложности

Удобен для адаптивного дизайна и структурирования страниц

В комбинации с Flexbox можно создавать полностью отзывчивые и гибкие интерфейсы