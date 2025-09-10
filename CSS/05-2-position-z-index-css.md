# Position и Z-index в CSS

## Краткая информация
CSS позволяет управлять **расположением элементов** на странице с помощью свойства `position` и контролировать **порядок наложения** с помощью `z-index`.  

### Свойства position
- `static` — по умолчанию, элемент располагается по потоку документа  
- `relative` — смещается относительно своего обычного положения  
- `absolute` — смещается относительно ближайшего родителя с `position` отличным от `static`  
- `fixed` — фиксирован относительно окна браузера  
- `sticky` — ведет себя как `relative` до достижения определенной позиции, затем фиксируется  

### Свойство z-index
- Определяет **слойность элементов**  
- Применяется только к элементам с `position` отличным от `static`  
- Чем выше значение, тем **выше элемент на странице**

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Position и Z-index</title>
    <style>
        .box1 {
            position: relative;
            width: 200px;
            height: 100px;
            background-color: red;
            z-index: 1;
        }

        .box2 {
            position: absolute;
            top: 50px;
            left: 50px;
            width: 200px;
            height: 100px;
            background-color: blue;
            z-index: 2;
        }
    </style>
</head>
<body>
    <div class="box1">Красный блок</div>
    <div class="box2">Синий блок</div>
</body>
</html>
Подробная информация
position: relative позволяет смещать элемент без выхода из потока документа

position: absolute полностью вырывает элемент из потока, он позиционируется относительно родителя с position

position: fixed идеален для шапок и кнопок, которые должны оставаться на экране при прокрутке

position: sticky полезен для "липких" элементов (например, заголовков таблицы)

z-index управляет какой элемент сверху, чем больше значение, тем выше элемент