# Формы в HTML

## Краткая информация
Формы позволяют пользователям вводить данные на сайте и отправлять их на сервер. Основной тег — `<form>`. Внутри формы могут быть разные элементы ввода: текстовые поля, кнопки, переключатели, флажки, выпадающие списки и т.д.

---

## Пример простой формы

```html
<form action="/submit" method="post">
  <label for="name">Имя:</label>
  <input type="text" id="name" name="name">

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <input type="submit" value="Отправить">
</form>
Подробная информация
Атрибуты <form>
action — URL, куда будут отправлены данные формы.

method — метод отправки (get или post).

enctype — кодировка данных (application/x-www-form-urlencoded, multipart/form-data для файлов).

Основные элементы формы
Текстовое поле <input type="text">
Для ввода текста.

Пароль <input type="password">
Символы скрываются при вводе.

Email <input type="email">
Валидируется браузером как email.

Флажки <input type="checkbox">
Для выбора нескольких вариантов.

Переключатели <input type="radio">
Для выбора одного варианта из группы.

Кнопки <button> или <input type="submit">
Для отправки формы или действий на странице.

Текстовая область <textarea>
Для ввода больших объёмов текста.

Выпадающий список <select>
Список вариантов для выбора.

Пример расширенной формы
html
Копировать код
<form action="/register" method="post">
  <label for="username">Имя пользователя:</label>
  <input type="text" id="username" name="username" required>

  <label for="password">Пароль:</label>
  <input type="password" id="password" name="password" required>

  <label for="gender">Пол:</label>
  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Мужской</label>
  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Женский</label>

  <label for="hobbies">Хобби:</label>
  <input type="checkbox" id="reading" name="hobbies" value="reading">
  <label for="reading">Чтение</label>
  <input type="checkbox" id="sports" name="hobbies" value="sports">
  <label for="sports">Спорт</label>

  <label for="country">Страна:</label>
  <select id="country" name="country">
    <option value="ru">Россия</option>
    <option value="us">США</option>
    <option value="fr">Франция</option>
  </select>

  <label for="bio">О себе:</label>
  <textarea id="bio" name="bio" rows="4" cols="50"></textarea>

  <input type="submit" value="Зарегистрироваться">
</form>
Объяснение
Формы собирают информацию от пользователя и отправляют её на сервер.

Использование разных типов <input> позволяет валидировать данные ещё на стороне браузера.

Атрибуты required, maxlength, pattern помогают сделать форму более безопасной и удобной.

<label> связывает текст с элементом формы, улучшая доступность для пользователей и экранных читалок.

<textarea> и <select> дают гибкость для больших текстов и выбора из списка.

Правильное использование форм — основа взаимодействия пользователя с сайтом и сбора данных.