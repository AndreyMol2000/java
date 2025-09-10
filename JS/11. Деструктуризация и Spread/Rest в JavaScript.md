# 11. Деструктуризация и Spread/Rest в JavaScript

## 11.1 Деструктуризация массивов

Позволяет распаковать массив в отдельные переменные.

```javascript
let numbers = [1, 2, 3, 4];
let [first, second, ...rest] = numbers;
console.log(first);  // 1
console.log(second); // 2
console.log(rest);   // [3,4]
```

## 11.2 Деструктуризация объектов

Позволяет распаковать объект в переменные.

```javascript
let person = {name: "John", age: 30, city: "Moscow"};
let {name, age} = person;
console.log(name); // John
console.log(age);  // 30
```

* Можно менять имена переменных

```javascript
let {name: firstName, city: town} = person;
console.log(firstName); // John
console.log(town);      // Moscow
```

## 11.3 Spread оператор `...`

* Копирование массивов

```javascript
let arr1 = [1,2];
let arr2 = [...arr1, 3,4];
console.log(arr2); // [1,2,3,4]
```

* Копирование объектов

```javascript
let obj1 = {a:1, b:2};
let obj2 = {...obj1, c:3};
console.log(obj2); // {a:1, b:2, c:3}
```

## 11.4 Rest оператор `...`

* Сбор оставшихся элементов в массив

```javascript
function sum(a, b, ...rest) {
    return rest.reduce((acc, n) => acc + n, a + b);
}
console.log(sum(1,2,3,4)); // 10
```

## Советы

* Используй деструктуризацию для удобного доступа к данным
* Spread позволяет создавать новые копии массивов и объектов
* Rest удобен для передачи переменного числа аргументов функции
