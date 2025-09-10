# Flexbox: основы и свойства

## Краткая информация
Flexbox — это современный способ **расположения элементов в контейнере**, позволяющий управлять направлением, выравниванием и порядком элементов.  

- Контейнер с `display: flex`  
- Элементы внутри становятся **flex-элементами**  
- Упрощает создание адаптивных и динамичных макетов  

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Flexbox пример</title>
    <style>
        .container {
            display: flex;
            flex-direction: row; /* направление строка */
            justify-content: space-between; /* распределение элементов по горизонтали */
            align-items: center; /* выравнивание по вертикали */
            height: 200px;
            background-color: #ecf0f1;
            padding: 20px;
        }

        .item {
            background-color: #3498db;
            color: white;
            padding: 20px;
            text-align: center;
            flex: 1; /* равная ширина для всех элементов */
            margin: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="item">Элемент 1</div>
        <div class="item">Элемент 2</div>
        <div class="item">Элемент 3</div>
    </div>
</body>
</html>
Подробная информация
Свойства контейнера
display: flex — превращает блок в flex-контейнер

flex-direction — направление элементов: row, row-reverse, column, column-reverse

justify-content — выравнивание по основной оси: flex-start, center, space-between, space-around

align-items — выравнивание по поперечной оси: flex-start, center, stretch, baseline

flex-wrap — перенос элементов на новую строку: nowrap, wrap, wrap-reverse

Свойства элементов
flex — сокращённая запись для flex-grow, flex-shrink, flex-basis

order — изменяет порядок элементов без изменения HTML

align-self — переопределяет align-items для отдельного элемента

Объяснение
Flexbox упрощает создание адаптивных макетов, где элементы подстраиваются под ширину контейнера

Легко выравнивать блоки горизонтально и вертикально

Свойства flex, justify-content и align-items позволяют управлять пропорциями, порядком и позиционированием элементов

Комбинируя контейнерные и элементные свойства, можно создавать гибкие и динамичные интерфейсы без сложных расчётов ширины и высоты