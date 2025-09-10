# 20. JavaScript в браузере: BOM и таймеры

BOM (Browser Object Model) предоставляет объекты для взаимодействия с браузером.

## 20.1 Window

* Главный объект, доступный глобально
* Методы и свойства:

```javascript
alert('Hello');
console.log(window.innerWidth);
window.open('https://example.com');
window.close();
```

## 20.2 Navigator

* Информация о браузере

```javascript
console.log(navigator.userAgent);
console.log(navigator.language);
```

## 20.3 Location

* Работа с URL

```javascript
console.log(location.href);
location.href = 'https://example.com';
```

## 20.4 History

* Работа с историей браузера

```javascript
history.back();
history.forward();
history.go(-1);
```

## 20.5 Таймеры

* `setTimeout(callback, delay)` — выполнить один раз через delay мс
* `setInterval(callback, delay)` — повторять через delay мс
* `clearTimeout(id)` и `clearInterval(id)` — отмена таймера

```javascript
let timeoutId = setTimeout(() => console.log('Hello after 1s'), 1000);
clearTimeout(timeoutId);

let intervalId = setInterval(() => console.log('Repeat every 2s'), 2000);
clearInterval(intervalId);
```

## Советы

* Используй BOM для управления браузером и окнами
* Таймеры полезны для анимаций и отложенного выполнения
* clearTimeout и clearInterval помогают избегать утечек памяти
