# PyGame Basics

## 1. Установка

```bash
pip install pygame
```

* PyGame используется для создания 2D-игр на Python

---

## 2. Создание окна

```python
import pygame

pygame.init()
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("Моя первая игра")

running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

pygame.quit()
```

* `pygame.init()` – инициализация всех модулей
* `pygame.display.set_mode()` – создание окна с размерами
* `pygame.display.set_caption()` – название окна
* Основной цикл игры `while running:` обрабатывает события

---

## 3. Цвета и фон

```python
WHITE = (255, 255, 255)
screen.fill(WHITE)
pygame.display.flip()  # обновление экрана
```

* Цвета задаются в формате RGB
* `fill()` – заливка фоном
* `flip()` или `update()` – обновление окна

---

## 4. События клавиатуры и мыши

```python
for event in pygame.event.get():
    if event.type == pygame.KEYDOWN:
        if event.key == pygame.K_UP:
            print("Стрелка вверх")
    if event.type == pygame.MOUSEBUTTONDOWN:
        print("Клик мыши", event.pos)
```

* `KEYDOWN` – нажатие клавиши, `KEYUP` – отпускание
* `MOUSEBUTTONDOWN` – нажатие кнопки мыши

---

## 5. Мини-задания

1. Создать окно 640x480 с названием "PyGame Test".
2. Залить окно красным цветом.
3. Вывести сообщение в консоль при нажатии клавиши пробел.
4. Вывести координаты мыши при клике.

---

Конец файла `01_PyGame_Basics.md`
