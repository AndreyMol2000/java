# 📚 Коллекции в Java (`HashMap`, `HashSet`, `TreeMap`, `TreeSet`)

Java предоставляет мощные коллекции для хранения и управления данными.  
Основные интерфейсы: **`Set`**, **`List`**, **`Map`**.  

---

## 1️⃣ `Set` – множество

### Характеристики:
- Хранит **уникальные элементы** (дубликаты не разрешены).  
- Не имеет индексов.  
- Бывает **неупорядоченным (`HashSet`)** и **упорядоченным (`TreeSet`)**.  

### Пример `HashSet`:

```java
import java.util.HashSet;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("123");
        set.add("222");
        set.add("444");
        set.add("123"); // не добавится, т.к. дубликат

        System.out.println(set); // Порядок не гарантирован
    }
}
Пример TreeSet:
java
Копировать код
import java.util.Set;
import java.util.TreeSet;

public class Main {
    public static void main(String[] args) {
        Set<String> tree = new TreeSet<>();
        tree.add("123");
        tree.add("222");
        tree.add("444");

        System.out.println(tree); // Выведет элементы в отсортированном порядке
    }
}
2️⃣ Map – отображение ключ → значение
Характеристики:
Хранит пары ключ → значение.

Ключи уникальны, значения могут повторяться.

Бывает неупорядоченный (HashMap) и сортированный (TreeMap).

Пример HashMap:
java
Копировать код
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        Map<String, String> map = new HashMap<>();
        map.put("key", "value");
        map.put("name", "John");
        map.put("city", "London");

        // Перебор ключей
        for (String key : map.keySet()) {
            System.out.println("Key: " + key);
        }

        // Перебор значений
        for (String value : map.values()) {
            System.out.println("Value: " + value);
        }

        // Получение значения по ключу
        String val = map.get("key");
        System.out.println("Value for 'key': " + val);
    }
}
Пример TreeMap:
java
Копировать код
import java.util.Map;
import java.util.TreeMap;

public class Main {
    public static void main(String[] args) {
        Map<String, Integer> treeMap = new TreeMap<>();
        treeMap.put("banana", 2);
        treeMap.put("apple", 5);
        treeMap.put("orange", 3);

        System.out.println(treeMap); 
        // Ключи автоматически отсортированы: apple, banana, orange
    }
}
3️⃣ Сравнение коллекций
Коллекция	Порядок	Дубликаты	Потокобезопасность
HashSet	нет	нет	нет
TreeSet	сортированный	нет	нет
HashMap	нет	ключи – нет, значения – да	нет
TreeMap	сортированный	ключи – нет, значения – да	нет

4️⃣ Советы
Для уникальных данных без сортировки – HashSet.

Для уникальных данных с сортировкой – TreeSet.

Для ключ → значение без сортировки – HashMap.

Для ключ → значение с сортировкой ключей – TreeMap.

Для многопоточной работы используйте ConcurrentHashMap или оборачивайте коллекции через Collections.synchronizedMap/set/list(...).