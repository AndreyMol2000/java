# Анимации и переходы в CSS

## Краткая информация
CSS позволяет создавать **движение и визуальные эффекты** без использования JavaScript.  

- **Transitions (переходы)** — плавное изменение свойств при наведении или изменении класса  
- **Animations (анимации)** — создание сложных последовательностей движения элементов  

---

## Пример: Переход (transition)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Transition пример</title>
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: #3498db;
            transition: all 0.5s ease; /* плавный переход всех свойств */
        }

        .box:hover {
            background-color: #e74c3c;
            transform: scale(1.2);
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
Пример: Анимация (animation)
html
Копировать код
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Animation пример</title>
    <style>
        @keyframes moveBox {
            0% { transform: translateX(0); background-color: #3498db; }
            50% { transform: translateX(200px); background-color: #e74c3c; }
            100% { transform: translateX(0); background-color: #3498db; }
        }

        .box {
            width: 100px;
            height: 100px;
            background-color: #3498db;
            animation: moveBox 3s infinite;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
Подробная информация
Transitions
Свойство transition задаёт какие свойства и за какое время будут изменяться

Синтаксис:

css
Копировать код
transition: property duration timing-function delay;
property — свойство, которое будет меняться

duration — длительность перехода

timing-function — функция ускорения (ease, linear, ease-in-out)

delay — задержка перед началом

Animations
Создаётся с помощью @keyframes

Свойства анимации:

animation-name — имя ключевых кадров

animation-duration — длительность

animation-iteration-count — количество повторов (infinite для бесконечной)

animation-timing-function — функция ускорения

Объяснение
Transitions удобны для небольших эффектов при взаимодействии: hover, focus

Animations позволяют создавать сложные динамические движения: карусели, бегущие строки, интерактивные эффекты

Комбинирование transition и animation повышает визуальную привлекательность сайта