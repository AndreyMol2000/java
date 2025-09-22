# PyQt Widgets

## 1. Метки (Labels)

```python
from PyQt5.QtWidgets import QLabel

label = QLabel("Привет, PyQt!", window)
label.move(50, 50)
```

* `QLabel` – текстовая метка
* `move(x, y)` – позиция внутри окна

---

## 2. Кнопки (Buttons)

```python
from PyQt5.QtWidgets import QPushButton

button = QPushButton("Нажми меня", window)
button.move(50, 100)
button.resize(100, 30)
```

* `QPushButton` – кнопка
* `resize(width, height)` – размер кнопки

---

## 3. Поля ввода (LineEdit)

```python
from PyQt5.QtWidgets import QLineEdit

line_edit = QLineEdit(window)
line_edit.move(50, 150)
line_edit.resize(200, 30)
```

* `QLineEdit` – однострочное текстовое поле
* Можно получить текст через `line_edit.text()`

---

## 4. Списки (ListWidget)

```python
from PyQt5.QtWidgets import QListWidget

list_widget = QListWidget(window)
list_widget.move(50, 200)
list_widget.resize(200, 100)
list_widget.addItem("Элемент 1")
list_widget.addItems(["Элемент 2", "Элемент 3"])
```

* `QListWidget` – список элементов
* `addItem()` и `addItems()` для добавления элементов

---

## 5. Мини-задания

1. Создать окно с меткой "Hello PyQt".
2. Добавить кнопку "Click" и поле ввода.
3. Добавить список из 3 элементов.
4. Попробовать перемещать и изменять размер виджетов.

---

Конец файла `02_PyQt_Widgets.md`
