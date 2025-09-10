# 📚 Generics (Обобщения) в Java

Generics позволяют создавать **классы, интерфейсы и методы**, работающие с разными типами данных, **без дублирования кода**.  
Главная цель — **типобезопасность** и повторное использование кода.

---

## 1️⃣ Основы Generics

Синтаксис: `<T>`  
- `T` – Type (тип данных, который будет передан при использовании класса/метода).  
- Обычно используют: `T` (тип), `E` (element), `K` (key), `V` (value).

Пример **класса с Generics**:

```java
public class Printer<T> {
    T thingToPrint;

    public Printer(T thingToPrint) {
        this.thingToPrint = thingToPrint;
    }

    public void print() {
        System.out.println(thingToPrint);
    }
}
Использование:
java
Копировать код
public class Main {
    public static void main(String[] args) {
        Printer<String> stringPrinter = new Printer<>("Hello, Java!");
        stringPrinter.print(); // Hello, Java!

        Printer<Integer> intPrinter = new Printer<>(123);
        intPrinter.print(); // 123

        Printer<Double> doublePrinter = new Printer<>(3.14);
        doublePrinter.print(); // 3.14
    }
}
2️⃣ Методы с Generics
Можно использовать Generics только для методов, без создания отдельного класса.

java
Копировать код
public class Utils {
    public static <T> void printArray(T[] array) {
        for (T element : array) {
            System.out.println(element);
        }
    }
}
Использование:
java
Копировать код
public class Main {
    public static void main(String[] args) {
        Integer[] numbers = {1, 2, 3};
        String[] words = {"hello", "world"};

        Utils.printArray(numbers);
        Utils.printArray(words);
    }
}
3️⃣ Ограничения Generics (Bounded Types)
Можно ограничивать типы, которые допускаются.

java
Копировать код
public class Calculator<T extends Number> {
    T num1, num2;

    public Calculator(T num1, T num2) {
        this.num1 = num1;
        this.num2 = num2;
    }

    public double sum() {
        return num1.doubleValue() + num2.doubleValue();
    }
}
Использование:
java
Копировать код
public class Main {
    public static void main(String[] args) {
        Calculator<Integer> calcInt = new Calculator<>(5, 10);
        System.out.println(calcInt.sum()); // 15.0

        Calculator<Double> calcDouble = new Calculator<>(5.5, 2.5);
        System.out.println(calcDouble.sum()); // 8.0
    }
}
4️⃣ Wildcards (?)
<?> – любой тип

<? extends Number> – только наследники Number

<? super Integer> – Integer или родительский тип

java
Копировать код
public void printList(List<? extends Number> list) {
    for (Number n : list) {
        System.out.println(n);
    }
}
5️⃣ Советы и рекомендации
Используйте Generics для повторного использования кода.

Обеспечивает типобезопасность, меньше ошибок времени выполнения.

Для коллекций Generics обязателен (ArrayList<String> вместо ArrayList).

Можно комбинировать с наследованием и интерфейсами.

📌 Итог
Generics позволяют создавать универсальные классы и методы, которые могут работать с разными типами данных, оставаясь типобезопасными.

Особенность	Пример
Класс с Generics	Printer<T>
Метод с Generics	<T> void printArray(T[] array)
Ограниченные типы	<T extends Number>
Wildcards	List<?>, List<? extends Number>