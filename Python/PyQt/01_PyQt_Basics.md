# PyQt Basics

## 1. Установка

```bash
pip install PyQt5
```

* PyQt5 позволяет создавать GUI-приложения на Python

---

## 2. Создание базового окна

```python
import sys
from PyQt5.QtWidgets import QApplication, QWidget

app = QApplication(sys.argv)
window = QWidget()
window.setWindowTitle("Мое первое окно")
window.setGeometry(100, 100, 400, 300)  # x, y, ширина, высота
window.show()
sys.exit(app.exec_())
```

* `QApplication` – основной объект приложения
* `QWidget` – базовый виджет (окно)
* `setGeometry` – позиция и размер окна
* `show()` – отображение окна
* `app.exec_()` – запуск основного цикла приложения

---

## 3. Настройка окна

```python
window.setFixedSize(400, 300)  # фиксированный размер
window.setWindowTitle("Пример PyQt")
```

* Можно фиксировать размер, менять заголовок и иконку

---

## 4. Мини-задания

1. Создать окно размером 500x400 с заголовком "PyQt Test".
2. Сделать окно фиксированного размера.
3. Поменять позицию окна на экране.
4. Попробовать создать два окна одновременно.

---

Конец файла `01_PyQt_Basics.md`
