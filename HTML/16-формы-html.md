# Формы в HTML

## Краткая информация
Формы позволяют пользователю **вводить данные**, которые потом можно отправить на сервер.  
Основные элементы формы:  
- `<form>` — контейнер для всех элементов формы  
- `<input>` — поле ввода (текст, пароль, чекбокс и др.)  
- `<textarea>` — многострочное текстовое поле  
- `<select>` и `<option>` — выпадающий список  
- `<button>` — кнопка для отправки или действий  

---

## Пример простой формы

```html
<form action="/submit" method="post">
  <label for="name">Имя:</label>
  <input type="text" id="name" name="username" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="useremail" required>

  <button type="submit">Отправить</button>
</form>
action — адрес, на который отправляются данные.

method — метод отправки (GET или POST).

required — обязательное поле.

<label> связывает текст с полем ввода (for = id поля).

Подробная информация
Типы <input>
text — текстовое поле

password — поле для пароля

email — поле для e-mail

number — числовое поле

checkbox — флажок

radio — переключатель (выбор одного варианта)

file — загрузка файлов

submit — кнопка отправки формы

reset — кнопка сброса формы

Многострочное поле
html
Копировать код
<label for="message">Сообщение:</label>
<textarea id="message" name="message" rows="5" cols="30"></textarea>
Выпадающий список
html
Копировать код
<label for="city">Город:</label>
<select id="city" name="city">
  <option value="moscow">Москва</option>
  <option value="spb">Санкт-Петербург</option>
  <option value="kazan">Казань</option>
</select>
Чекбоксы и радиокнопки
html
Копировать код
<label>
  <input type="checkbox" name="subscribe" value="yes"> Подписаться на новости
</label>

<label>
  <input type="radio" name="gender" value="male"> Мужской
</label>
<label>
  <input type="radio" name="gender" value="female"> Женский
</label>
Кнопки
<button type="submit"> — отправка формы

<button type="reset"> — сброс формы

<button type="button"> — обычная кнопка для скриптов

Объяснение
Формы — основной способ взаимодействия пользователя с сайтом.

Каждый элемент <input> имеет имя (name), которое отправляется на сервер.

<label> повышает доступность и удобство для пользователя.

Для современных сайтов формы часто валидаются через HTML-атрибуты (required, pattern) и JavaScript.

<textarea> и <select> используются для более сложных данных, а чекбоксы и радиокнопки — для выбора вариантов.

Кнопки типа submit и reset контролируют отправку и очистку данных.