# PyQt Layouts

## 1. Основные Layouts

* **QVBoxLayout** – вертикальное расположение
* **QHBoxLayout** – горизонтальное расположение
* **QGridLayout** – сетка (rows, columns)

---

## 2. Пример вертикального Layout

```python
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QVBoxLayout
import sys

app = QApplication(sys.argv)
window = QWidget()
layout = QVBoxLayout()

btn1 = QPushButton("Кнопка 1")
btn2 = QPushButton("Кнопка 2")
btn3 = QPushButton("Кнопка 3")

layout.addWidget(btn1)
layout.addWidget(btn2)
layout.addWidget(btn3)

window.setLayout(layout)
window.show()
sys.exit(app.exec_())
```

* `addWidget()` добавляет виджет в layout

---

## 3. Горизонтальный Layout

```python
from PyQt5.QtWidgets import QHBoxLayout
layout = QHBoxLayout()
layout.addWidget(btn1)
layout.addWidget(btn2)
layout.addWidget(btn3)
```

* Расположение виджетов по горизонтали

---

## 4. Grid Layout

```python
from PyQt5.QtWidgets import QGridLayout
layout = QGridLayout()
layout.addWidget(btn1, 0, 0)
layout.addWidget(btn2, 0, 1)
layout.addWidget(btn3, 1, 0, 1, 2)  # занимает 1 строку и 2 колонки
```

* `addWidget(widget, row, column, rowspan, colspan)`
* Позволяет строить сложные формы и интерфейсы

---

## 5. Мини-задания

1. Создать окно с вертикальным layout из 3 кнопок.
2. Создать горизонтальный layout с кнопками.
3. Сделать сетку 2x2 и разместить кнопки в ячейках.
4. Скомбинировать вертикальные и горизонтальные layout в одном окне.

---

Конец файла `03_PyQt_Layouts.md`
