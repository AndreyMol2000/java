# Python Practice and Mini-Projects

## 1. Калькулятор

Простой калькулятор с функциями для каждой операции.

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Ошибка: деление на ноль"

while True:
    op = input("Введите операцию (+,-,*,/) или 'q' для выхода: ")
    if op == 'q':
        break
    x = float(input("Первое число: "))
    y = float(input("Второе число: "))
    if op == '+':
        print(add(x,y))
    elif op == '-':
        print(subtract(x,y))
    elif op == '*':
        print(multiply(x,y))
    elif op == '/':
        print(divide(x,y))
    else:
        print("Неизвестная операция")
```

---

## 2. Телеграм-бот

Используем библиотеку `python-telegram-bot`.

```python
from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

def start(update: Update, context: CallbackContext):
    update.message.reply_text('Привет! Я бот.')

updater = Updater('YOUR_TOKEN')
updater.dispatcher.add_handler(CommandHandler('start', start))
updater.start_polling()
updater.idle()
```

---

## 3. Парсер сайта

Используем `requests` и `BeautifulSoup`.

```python
import requests
from bs4 import BeautifulSoup

url = 'https://example.com'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

for h2 in soup.find_all('h2'):
    print(h2.text)
```

---

## 4. Идеи мини-проектов

1. Игра "Угадай число"
2. Генератор паролей
3. Список задач (ToDo) с сохранением в файл
4. Анализ CSV-файлов
5. Простой веб-сервер на `Flask`

---

## 5. Мини-задания

1. Сделать калькулятор с возможностью повторного ввода без выхода из программы.
2. Написать парсер для новостей с сайта.
3. Создать ToDo-приложение с сохранением в CSV.
4. Сделать игру "Угадай число" с ограничением попыток.

---

Конец файла `06_Projects.md`
