# PyGame Collisions

## 1. Проверка столкновений спрайтов

```python
import pygame

# Предполагаем, что есть два спрайта: player и enemy
if pygame.sprite.collide_rect(player, enemy):
    print("Столкновение!")
```

* `collide_rect` проверяет пересечение прямоугольников `rect`

---

## 2. Группы и столкновения

```python
# Проверяем столкновения игрока с группой врагов
hits = pygame.sprite.spritecollide(player, enemies_group, False)
for hit in hits:
    print(f"Столкновение с {hit}")
```

* `spritecollide(sprite, group, dokill)` – проверяет столкновения с группой
* `dokill=True` удаляет объект после столкновения

---

## 3. События при столкновении

* Можно уменьшать здоровье игрока, удалять врагов, менять счет и т.д.

```python
for hit in hits:
    player.health -= 10
    enemies_group.remove(hit)
```

---

## 4. Мини-задания

1. Создать игрока и несколько врагов, проверять столкновения.
2. При столкновении выводить сообщение и удалять врага.
3. Добавить счетчик очков за каждое столкновение.
4. Ограничить здоровье игрока и выводить сообщение "Game Over" при 0.

---

Конец файла `03_PyGame_Collisions.md`
