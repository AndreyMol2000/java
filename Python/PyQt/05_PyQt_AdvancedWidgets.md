# PyQt Advanced Widgets

## 1. Таблицы (QTableWidget)

```python
from PyQt5.QtWidgets import QTableWidget, QTableWidgetItem

table = QTableWidget(window)
table.setRowCount(3)
table.setColumnCount(2)
table.setItem(0, 0, QTableWidgetItem("Ячейка 1"))
table.setItem(0, 1, QTableWidgetItem("Ячейка 2"))
```

* `setRowCount` и `setColumnCount` задают размеры
* `setItem(row, column, item)` вставляет данные

---

## 2. Вкладки (QTabWidget)

```python
from PyQt5.QtWidgets import QTabWidget, QWidget, QVBoxLayout

tabs = QTabWidget(window)
tab1 = QWidget()
tab2 = QWidget()
tabs.addTab(tab1, "Вкладка 1")
tabs.addTab(tab2, "Вкладка 2")
```

* `QTabWidget` позволяет создавать вкладки
* Каждая вкладка — отдельный `QWidget`

---

## 3. Диалоги (QMessageBox)

```python
from PyQt5.QtWidgets import QMessageBox

def show_message():
    msg = QMessageBox()
    msg.setWindowTitle("Внимание")
    msg.setText("Привет, PyQt!")
    msg.exec_()

button.clicked.connect(show_message)
```

* `QMessageBox` – модальное окно с сообщением
* `exec_()` отображает диалог

---

## 4. Мини-задания

1. Создать таблицу 3x3 и заполнить ячейки данными.
2. Добавить вкладки с разными виджетами на каждой.
3. Сделать кнопку, которая вызывает диалоговое окно с сообщением.
4. Комбинировать таблицы и вкладки в одном окне.

---

Конец файла `05_PyQt_AdvancedWidgets.md`
