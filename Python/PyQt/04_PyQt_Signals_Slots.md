# PyQt Signals and Slots

## 1. Сигналы и слоты

* **Сигналы** – события, происходящие в виджетах (нажатие кнопки, изменение текста)
* **Слоты** – функции, которые обрабатывают эти события

---

## 2. Пример кнопки и слота

```python
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton
import sys

app = QApplication(sys.argv)
window = QWidget()
window.setGeometry(100, 100, 300, 200)

button = QPushButton("Нажми меня", window)
button.move(100, 80)

def on_click():
    print("Кнопка нажата")

button.clicked.connect(on_click)

window.show()
sys.exit(app.exec_())
```

* `clicked` – сигнал кнопки при нажатии
* `connect()` – связывает сигнал с функцией (слотом)

---

## 3. Сигналы других виджетов

```python
from PyQt5.QtWidgets import QLineEdit

line_edit = QLineEdit(window)
line_edit.move(50, 50)

def text_changed():
    print("Текст изменен", line_edit.text())

line_edit.textChanged.connect(text_changed)
```

* `textChanged` – сигнал при изменении текста

---

## 4. Мини-задания

1. Создать кнопку и вывести сообщение при клике.
2. Добавить поле ввода и выводить текст при каждом изменении.
3. Создать две кнопки с разными слотами.
4. Попробовать использовать лямбда-функцию для передачи параметров в слот.

---

Конец файла `04_PyQt_Signals_Slots.md`
