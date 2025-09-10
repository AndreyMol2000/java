# Продвинутые селекторы CSS: attribute selectors и combinators

## Краткая информация
Продвинутые селекторы позволяют **точечно выбирать элементы** по атрибутам или их взаимному положению в DOM.  
Это даёт гибкость и уменьшает количество классов и ID.  

### Основные типы:
1. **Attribute selectors** — выбор по атрибуту  
2. **Combinators** — выбор элементов на основе их взаимного расположения  

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Продвинутые селекторы</title>
    <style>
        /* Attribute selectors */
        input[type="text"] {
            border: 2px solid #3498db;
        }

        a[href^="https"] {
            color: green; /* ссылки, начинающиеся с https */
        }

        a[href$=".com"] {
            text-decoration: underline; /* ссылки, оканчивающиеся на .com */
        }

        a[href*="example"] {
            font-weight: bold; /* ссылки, содержащие "example" */
        }

        /* Combinators */
        div > p {
            color: red; /* прямые дочерние элементы p внутри div */
        }

        div p {
            font-size: 14px; /* все p внутри div (включая вложенные) */
        }

        h1 + p {
            margin-top: 0; /* первый p после h1 */
        }

        h1 ~ p {
            color: gray; /* все p после h1 на том же уровне */
        }
    </style>
</head>
<body>
    <div>
        <p>Прямой потомок div</p>
        <p>Вложенный потомок</p>
    </div>
    <h1>Заголовок</h1>
    <p>Первый параграф после h1</p>
    <p>Второй параграф после h1</p>

    <input type="text" placeholder="Текстовое поле">
    <a href="https://example.com">Ссылка Example</a>
</body>
</html>
Подробная информация
Attribute selectors
[attr] — элементы с атрибутом attr

[attr="value"] — элементы с точным значением

[attr^="value"] — элементы, где значение атрибута начинается с value

[attr$="value"] — элементы, где значение атрибута заканчивается на value

[attr*="value"] — элементы, где значение атрибута содержит value

Combinators
E F — потомок (descendant) элемента E

E > F — прямой потомок (child) элемента E

E + F — следующий сосед (adjacent sibling) элемента E

E ~ F — все последующие соседи (general sibling) элемента E

Объяснение
Продвинутые селекторы помогают сократить количество классов и ID, делая CSS более чистым

Attribute selectors позволяют стилизовать элементы по их атрибутам, например, все ссылки с https

Combinators позволяют выбирать элементы в зависимости от их расположения в DOM, что особенно полезно при работе с компонентными структурами

Используя их, можно создавать гибкие, динамичные и переиспользуемые стили

yaml
Копировать код
