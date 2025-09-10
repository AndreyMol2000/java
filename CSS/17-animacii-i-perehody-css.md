# Анимации и переходы в CSS

## Краткая информация
Анимации и переходы позволяют создавать **динамичные эффекты на сайте**, улучшая UX и визуальную привлекательность.  
- **Transitions** — плавные изменения свойств при взаимодействии  
- **Animations** — полноценные анимации с ключевыми кадрами  

---

## Пример: Переход (Transition)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Transition пример</title>
    <style>
        .button {
            background-color: #3498db;
            color: white;
            padding: 15px 30px;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .button:hover {
            background-color: #2ecc71;
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <button class="button">Наведи на меня</button>
</body>
</html>
Пример: Анимация (Animation)
html
Копировать код
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Animation пример</title>
    <style>
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-30px); }
        }

        .ball {
            width: 50px;
            height: 50px;
            background-color: #e74c3c;
            border-radius: 50%;
            margin: 50px auto;
            animation: bounce 2s infinite;
        }
    </style>
</head>
<body>
    <div class="ball"></div>
</body>
</html>
Подробная информация
Transition
Свойство transition задаёт плавное изменение CSS-свойств

Основные параметры:

transition-property — какие свойства анимировать

transition-duration — продолжительность анимации

transition-timing-function — функция времени (ease, linear, ease-in, ease-out, cubic-bezier)

transition-delay — задержка перед началом

Animation
Используются ключевые кадры с @keyframes

Свойства:

animation-name — имя анимации

animation-duration — продолжительность

animation-timing-function — функция времени

animation-delay — задержка

animation-iteration-count — количество повторов (infinite — бесконечно)

animation-direction — направление (normal, reverse, alternate)

Объяснение
Переходы удобны для простых эффектов при наведении или клике

Анимации позволяют создавать сложные движения элементов

Использование анимаций и переходов делает сайт живым и привлекательным

Комбинируя их, можно управлять вниманием пользователя и улучшать интерфейс