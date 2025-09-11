# Python Functions and Modules

## 1. Функции

Функции позволяют структурировать код и избегать повторений.

### Создание функции

```python
def greet(name):
    return f"Привет, {name}!"

print(greet("Андрей"))
```

### Параметры и значения по умолчанию

```python
def power(number, exponent=2):
    return number ** exponent

print(power(5))     # 25
print(power(5, 3))  # 125
```

### Возврат нескольких значений

```python
def min_max(numbers):
    return min(numbers), max(numbers)

minimum, maximum = min_max([1,2,3,4,5])
print(minimum, maximum)
```

---

## 2. Модули

Модуль – это файл с Python-кодом, который можно подключить.

### Импорт модулей

```python
import math
print(math.sqrt(16))  # 4.0
```

```python
from math import sqrt
print(sqrt(25))        # 5.0
```

### Создание собственного модуля

`mymodule.py`:

```python
def say_hello():
    print("Hello!")
```

```python
import mymodule
mymodule.say_hello()  # Hello!
```

---

## 3. Установка и использование сторонних библиотек

Используем `pip` для установки.

```bash
pip install requests
```

```python
import requests
response = requests.get('https://example.com')
print(response.status_code)
```

---

## 4. Мини-задания

1. Написать функцию, которая возвращает факториал числа.
2. Написать функцию, которая проверяет, является ли число простым.
3. Создать свой модуль с функцией приветствия и подключить его.
4. Установить библиотеку `requests` и сделать GET-запрос к любому сайту.

---

Конец файла `03_Functions_Modules.md`
