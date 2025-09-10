# Метаданные и SEO в HTML

## Краткая информация
Метаданные дают браузеру и поисковым системам **информацию о странице**, не видимую пользователю.  
Основные теги:  
- `<meta>` — описание, ключевые слова, кодировка  
- `<link>` — подключение внешних ресурсов (CSS, иконки)  
- `<title>` — заголовок страницы  
- `<script>` — подключение JavaScript  

---

## Пример основных метаданных

```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Пример страницы HTML для обучения">
  <meta name="keywords" content="HTML, обучение, веб">
  <meta name="author" content="Андрей Молчанов">
  <title>Пример страницы</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Добро пожаловать на страницу!</h1>
</body>
</html>
<meta charset="UTF-8"> — указывает кодировку страницы.

<meta name="description"> — описание страницы для поисковиков.

<meta name="keywords"> — ключевые слова.

<meta name="author"> — автор страницы.

<title> — название вкладки браузера.

<link> — подключение стилей или иконок.

Подробная информация
<meta>
Метатеги не отображаются на странице, но важны для SEO.

Типы атрибутов:

charset — кодировка.

name и content — ключевые данные для поисковиков (description, keywords, author).

http-equiv — специальные инструкции для браузера, например, refresh для обновления страницы.

<link>
Используется для подключения внешних ресурсов:

CSS-файлы: <link rel="stylesheet" href="style.css">

Favicon: <link rel="icon" href="favicon.ico" type="image/x-icon">

Предзагрузка ресурсов: <link rel="preload" href="script.js" as="script">

<title>
Отображается во вкладке браузера и в результатах поиска.

Должен быть уникальным для каждой страницы.

<script>
Подключение JavaScript-файлов или встроенного кода:

<script src="script.js"></script>

<script>console.log("Hello World")</script>

Размещение в <head> или перед </body> для оптимизации загрузки страницы.

Пример расширенного использования
html
Копировать код
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Учебная страница по HTML">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="robots" content="index, follow">
  <title>HTML Урок</title>
  <link rel="stylesheet" href="style.css">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
  <script src="script.js" defer></script>
</head>
<meta name="viewport"> — адаптивность под мобильные устройства.

<meta name="robots"> — указание для поисковых систем индексировать страницу.

Атрибут defer у <script> — откладывает выполнение скрипта до полной загрузки страницы.

Объяснение
Метаданные помогают поисковым системам и браузерам понять содержание страницы.

Использование правильных <meta> улучшает SEO, делает сайт более доступным и адаптивным.

<title> влияет на кликабельность в поиске.

<link> и <script> позволяют подключать внешние ресурсы и оптимизировать загрузку страницы.

Современные сайты используют метаданные для оптимизации скорости, SEO и адаптивности.