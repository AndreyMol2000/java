# Псевдоклассы для взаимодействия: hover, active, focus

## Краткая информация
Псевдоклассы позволяют **менять стиль элементов в зависимости от действий пользователя**: наведение, нажатие или фокус на элементе.  

- `:hover` — при наведении мыши  
- `:active` — при нажатии на элемент  
- `:focus` — когда элемент в фокусе (input, textarea, кнопки)  

---

## Пример

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Pseudo-classes пример</title>
    <style>
        button {
            background-color: #3498db;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        button:hover {
            background-color: #2ecc71; /* при наведении */
        }

        button:active {
            transform: scale(0.95); /* при нажатии */
        }

        input {
            padding: 8px;
            border: 2px solid #ccc;
            transition: border-color 0.3s ease;
        }

        input:focus {
            border-color: #3498db; /* при фокусе */
            outline: none;
        }
    </style>
</head>
<body>
    <button>Кнопка</button>
    <br><br>
    <input type="text" placeholder="Введите текст">
</body>
</html>
Подробная информация
:hover — часто используется для кнопок, ссылок, меню

:active — применяется для визуальной обратной связи при клике

:focus — улучшает доступность: видно, где сейчас фокус на клавиатуре

Можно комбинировать псевдоклассы:

css
Копировать код
a:hover, a:focus {
    color: red;
}
Псевдоклассы работают только с интерактивными элементами (ссылки, кнопки, input)

Объяснение
Эти псевдоклассы улучшают UX и делают интерфейс интерактивным

Важны для доступности: пользователи с клавиатурой или вспомогательными технологиями видят фокус и активные элементы

В сочетании с transition и animation можно создавать плавные и визуально привлекательные эффекты

yaml
Копировать код
