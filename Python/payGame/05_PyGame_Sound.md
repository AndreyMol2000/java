# PyGame Sound and Music

## 1. Установка

* PyGame уже содержит модуль `pygame.mixer` для работы со звуком

```python
import pygame
pygame.init()
pygame.mixer.init()
```

---

## 2. Загрузка и воспроизведение звуков

```python
sound = pygame.mixer.Sound("jump.wav")
sound.play()
```

* `Sound` – короткие звуки (эффекты)
* `play()` – воспроизведение

---

## 3. Музыка

```python
pygame.mixer.music.load("background.mp3")
pygame.mixer.music.play(-1)  # -1 = бесконечный цикл
pygame.mixer.music.stop()     # остановка музыки
```

* `mixer.music` – для фоновой музыки
* `play(-1)` повторяет музыку бесконечно

---

## 4. Регулировка громкости

```python
sound.set_volume(0.5)       # 50% громкости
pygame.mixer.music.set_volume(0.3)
```

* Диапазон от 0.0 до 1.0

---

## 5. Мини-задания

1. Добавить фоновую музыку в игру.
2. Создать звук прыжка и проигрывать его при нажатии клавиши.
3. Сделать звук столкновения игрока с врагом.
4. Регулировать громкость разных звуков.

---

Конец файла `05_PyGame_Sound.md`
