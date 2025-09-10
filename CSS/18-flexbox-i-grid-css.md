# Flexbox продвинутый и CSS Grid

## Краткая информация
Flexbox и Grid — современные методы **вёрстки макетов**, позволяющие создавать **адаптивные, гибкие и сложные сетки**.  

- **Flexbox** — управляет **расположением элементов в одной линии** (строка или колонка)  
- **Grid** — позволяет строить **двумерные сетки** (ряды и колонки)  

---

## Пример: Flexbox продвинутый

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Flexbox продвинутый</title>
    <style>
        .container {
            display: flex;
            flex-wrap: wrap; /* перенос на новую строку */
            justify-content: space-around; /* распределение по горизонтали */
            align-items: stretch; /* растягивание элементов по высоте */
            gap: 10px; /* отступы между элементами */
        }

        .item {
            flex: 1 1 150px; /* grow, shrink, basis */
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
    </div>
</body>
</html>
Пример: CSS Grid
html
Копировать код
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>CSS Grid</title>
    <style>
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* три колонки равной ширины */
            grid-template-rows: 100px 200px; /* две строки */
            gap: 10px; /* расстояние между ячейками */
        }

        .grid-item {
            background-color: #e74c3c;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
        }
    </style>
</head>
<body>
    <div class="grid-container">
        <div class="grid-item">1</div>
        <div class="grid-item">2</div>
        <div class="grid-item">3</div>
        <div class="grid-item">4</div>
        <div class="grid-item">5</div>
        <div class="grid-item">6</div>
    </div>
</body>
</html>
Подробная информация
Flexbox продвинутый
flex-wrap — позволяет переносить элементы на новую строку

flex-grow / flex-shrink / flex-basis — управление размерами элементов

gap — отступ между элементами

align-self — индивидуальное выравнивание элементов

order — изменяет порядок элементов

CSS Grid
grid-template-columns / rows — задают размеры колонок и строк

grid-gap / gap — расстояние между ячейками

grid-column / grid-row — позиционирование элемента внутри сетки

auto-fill / auto-fit — автоматическое заполнение сетки

Grid идеально подходит для сложных макетов, Flexbox — для простых линейных расположений

Объяснение
Flexbox лучше использовать для одномерных макетов

Grid позволяет создавать двумерные сетки с точным контролем

Комбинируя Flexbox и Grid, можно легко создавать адаптивные, красивые и гибкие интерфейсы

Продвинутые свойства Flexbox и Grid позволяют контролировать выравнивание, размеры и порядок элементов без лишнего кода