# Async FastAPI + SQLAlchemy

## 1. Установка асинхронного драйвера

```bash
pip install asyncpg sqlalchemy[asyncio]
```

* Для PostgreSQL используем `asyncpg`
* Для SQLite встроенный драйвер тоже поддерживает async

---

## 2. Создание асинхронного движка

```python
from sqlalchemy.ext.asyncio import AsyncSession, create_async_engine
from sqlalchemy.orm import sessionmaker, declarative_base

DATABASE_URL = "postgresql+asyncpg://user:password@localhost/dbname"
engine = create_async_engine(DATABASE_URL, echo=True)
AsyncSessionLocal = sessionmaker(engine, expire_on_commit=False, class_=AsyncSession)
Base = declarative_base()
```

---

## 3. Асинхронная сессия и зависимость FastAPI

```python
from fastapi import Depends

async def get_db():
    async with AsyncSessionLocal() as session:
        yield session
```

* Используем `async with` для сессий
* Подключаем в эндпоинтах через `Depends`

---

## 4. Асинхронные эндпоинты

```python
from fastapi import FastAPI, Depends
from sqlalchemy.future import select

app = FastAPI()

@app.get("/users/{user_id}")
async def read_user(user_id: int, db: AsyncSession = Depends(get_db)):
    result = await db.execute(select(User).filter_by(id=user_id))
    user = result.scalar_one_or_none()
    return user
```

* Используем `async def` и `await` для запросов к базе
* `select()` вместо `query()` для асинхронного SQLAlchemy

---

## 5. Мини-задания

1. Создать асинхронный эндпоинт для получения всех пользователей.
2. Сделать POST эндпоинт для добавления нового пользователя.
3. Переделать CRUD для задач (`Task`) в асинхронный режим.
4. Попробовать вызвать несколько асинхронных эндпоинтов параллельно через `asyncio.gather`.

---

Конец файла `06_Async_FastAPI_SQLAlchemy.md`
