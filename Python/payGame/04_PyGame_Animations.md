# PyGame Animations

## 1. Анимация через спрайты

* Для анимации спрайта используем список изображений (кадров)

```python
import pygame

class Player(pygame.sprite.Sprite):
    def __init__(self):
        super().__init__()
        self.frames = [pygame.Surface((50,50)) for _ in range(4)]
        colors = [(255,0,0),(0,255,0),(0,0,255),(255,255,0)]
        for frame, color in zip(self.frames, colors):
            frame.fill(color)
        self.index = 0
        self.image = self.frames[self.index]
        self.rect = self.image.get_rect()

    def update(self):
        self.index += 1
        if self.index >= len(self.frames):
            self.index = 0
        self.image = self.frames[self.index]
```

* В `update()` меняем кадр спрайта для анимации

---

## 2. Анимация движения

* Можно менять изображение спрайта в зависимости от направления

```python
keys = pygame.key.get_pressed()
if keys[pygame.K_LEFT]:
    player.rect.x -= 5
    player.image = left_frame
```

* Для каждого направления отдельный набор кадров

---

## 3. Таймеры и скорость анимации

* Можно использовать `pygame.time.get_ticks()` для контроля скорости смены кадров

```python
now = pygame.time.get_ticks()
if now - self.last_update > 100:
    self.last_update = now
    self.index = (self.index + 1) % len(self.frames)
    self.image = self.frames[self.index]
```

* 100 мс между кадрами для плавной анимации

---

## 4. Мини-задания

1. Создать анимацию для игрока с 4 разными цветами.
2. Сделать смену кадров каждые 150 мс.
3. Добавить анимацию при движении игрока влево и вправо.
4. Попробовать создать анимацию прыжка.

---

Конец файла `04_PyGame_Animations.md`
