# PyGame Sprites and Movement

## 1. Основы спрайтов

```python
import pygame

pygame.init()
screen = pygame.display.set_mode((800, 600))
clock = pygame.time.Clock()

class Player(pygame.sprite.Sprite):
    def __init__(self):
        super().__init__()
        self.image = pygame.Surface((50, 50))
        self.image.fill((0, 128, 255))
        self.rect = self.image.get_rect()
        self.rect.center = (400, 300)

player = Player()
all_sprites = pygame.sprite.Group()
all_sprites.add(player)

running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    all_sprites.update()
    screen.fill((255, 255, 255))
    all_sprites.draw(screen)
    pygame.display.flip()
    clock.tick(60)

pygame.quit()
```

* Класс `Sprite` используется для объектов игры
* `image` – графика объекта, `rect` – позиция и размеры
* `Group` позволяет управлять множеством спрайтов

---

## 2. Движение спрайтов

```python
keys = pygame.key.get_pressed()
if keys[pygame.K_LEFT]:
    player.rect.x -= 5
if keys[pygame.K_RIGHT]:
    player.rect.x += 5
if keys[pygame.K_UP]:
    player.rect.y -= 5
if keys[pygame.K_DOWN]:
    player.rect.y += 5
```

* `pygame.key.get_pressed()` возвращает состояние всех клавиш
* Изменяем координаты `rect` для движения

---

## 3. Мини-задания

1. Создать спрайт `Enemy` с размером 40x40 и красным цветом.
2. Добавить несколько врагов в группу спрайтов и отобразить их.
3. Сделать движение игрока стрелками.
4. Ограничить движение игрока рамками экрана.

---

Конец файла `02_PyGame_Sprites.md`
