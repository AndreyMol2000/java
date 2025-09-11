# FastAPI Basics

## 1. Установка и запуск

```bash
pip install fastapi uvicorn
```

* `fastapi` – сам фреймворк
* `uvicorn` – ASGI-сервер для запуска приложения

Запуск приложения:

```bash
uvicorn main:app --reload
```

* `main` – имя файла без `.py`
* `app` – объект FastAPI
* `--reload` – автоматическая перезагрузка при изменениях

---

## 2. Создание приложения

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello World"}
```

* `@app.get()` – декоратор маршрута
* Методы HTTP: `GET`, `POST`, `PUT`, `DELETE`

---

## 3. Параметры маршрутов

### Path-параметры

```python
@app.get("/items/{item_id}")
def read_item(item_id: int):
    return {"item_id": item_id}
```

### Query-параметры

```python
@app.get("/items/")
def read_item(skip: int = 0, limit: int = 10):
    return {"skip": skip, "limit": limit}
```

---

## 4. Ответы и статусы

```python
from fastapi import status

@app.post("/items/", status_code=status.HTTP_201_CREATED)
def create_item(item: dict):
    return item
```

* Можно указывать статус ответа через `status_code`

---

## 5. Мини-задания

1. Создать приложение FastAPI с маршрутом `/hello`, возвращающим "Hello, FastAPI!".
2. Добавить маршрут `/user/{name}`, который возвращает приветствие с именем.
3. Создать маршрут `/sum` с query-параметрами `a` и `b`, возвращающий их сумму.

---

Конец файла `01_FastAPI_Basics.md`
