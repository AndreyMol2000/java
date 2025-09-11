# Python Object-Oriented Programming (OOP)

## 1. Классы и объекты

Класс – это шаблон, объект – экземпляр класса.

```python
class Animal:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def speak(self):
        print(f"{self.name} издает звук")

# Создание объекта
dog = Animal("Бобик", 3)
dog.speak()  # Бобик издает звук
```

* `__init__` – конструктор класса
* `self` – ссылка на текущий объект

---

## 2. Атрибуты и методы

* Атрибуты – переменные объекта (`self.name`, `self.age`)
* Методы – функции объекта (`speak()`, `eat()`)

Добавим метод:

```python
def birthday(self):
    self.age += 1
```

---

## 3. Наследование

Позволяет создавать класс на основе другого.

```python
class Dog(Animal):
    def speak(self):
        print(f"{self.name} гавкает")

dog = Dog("Шарик", 5)
dog.speak()  # Шарик гавкает
```

* Можно переопределять методы родителя
* Можно добавлять новые методы и атрибуты

---

## 4. Инкапсуляция

Скрытие данных и методов.

```python
class Person:
    def __init__(self, name, age):
        self.__age = age  # приватный атрибут
        self.name = name

    def get_age(self):
        return self.__age

    def set_age(self, age):
        if age > 0:
            self.__age = age

p = Person("Андрей", 25)
print(p.get_age())
```

* `__attribute` – делает атрибут приватным

---

## 5. Полиморфизм

Метод с одинаковым именем ведет себя по-разному в разных классах.

```python
class Cat(Animal):
    def speak(self):
        print(f"{self.name} мяукает")

animals = [Dog("Шарик",5), Cat("Мурка",3)]
for a in animals:
    a.speak()
```

* Одинаковый метод `speak()` работает по-разному

---

## 6. Мини-задания

1. Создать класс `Car` с атрибутами `model`, `year` и методом `drive()`.
2. Создать два класса-наследника `ElectricCar` и `GasCar`, переопределить метод `drive()`.
3. Сделать приватный атрибут `mileage` и методы для его чтения/изменения.
4. Создать список объектов и вызвать метод `drive()` для всех.

---

Конец файла `05_OOP.md`
