# Python File I/O

## 1. Чтение файлов

Чтение текстового файла с помощью `open()` и контекстного менеджера `with`.

```python
with open("example.txt", "r", encoding="utf-8") as file:
    content = file.read()
print(content)
```

### Методы чтения:

* `read()` – весь файл
* `readline()` – одну строку
* `readlines()` – список строк

---

## 2. Запись в файлы

```python
with open("example.txt", "w", encoding="utf-8") as file:
    file.write("Hello, Python!\n")
```

* `w` – перезаписывает файл
* `a` – добавляет в конец файла

---

## 3. Контекстный менеджер `with`

Он автоматически закрывает файл, даже если произойдет ошибка.

```python
with open("example.txt", "r") as f:
    data = f.read()
# Файл автоматически закрыт
```

---

## 4. Чтение больших файлов построчно

```python
with open("large_file.txt", "r") as file:
    for line in file:
        print(line.strip())
```

* `strip()` убирает символы переноса строки и пробелы

---

## 5. Работа с файлами CSV (библиотека `csv`)

```python
import csv
with open('data.csv', newline='', encoding='utf-8') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)
```

---

## 6. Мини-задания

1. Создать файл `test.txt` и записать туда несколько строк.
2. Прочитать файл и вывести каждую строку с номером.
3. Дописать в файл новую строку, не удаляя старые.
4. Создать CSV-файл с данными о 3 людях (имя, возраст, город) и прочитать его через `csv.reader`.

---

Конец файла `04_File_IO.md`
