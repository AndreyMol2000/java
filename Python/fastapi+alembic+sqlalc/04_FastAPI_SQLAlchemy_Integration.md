# FastAPI + SQLAlchemy Integration

## 1. Подключение к базе через SQLAlchemy

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker, declarative_base

DATABASE_URL = "sqlite:///./test.db"
engine = create_engine(DATABASE_URL, connect_args={"check_same_thread": False})
SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)
Base = declarative_base()
```

* `SessionLocal` – фабрика сессий для работы с базой

---

## 2. Зависимости FastAPI для сессии

```python
from fastapi import Depends

def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()
```

* Позволяет получать сессию в эндпоинтах через `Depends`

---

## 3. Пример модели и Pydantic схемы

```python
from sqlalchemy import Column, Integer, String
from pydantic import BaseModel

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True, index=True)
    name = Column(String, index=True)
    age = Column(Integer)

class UserCreate(BaseModel):
    name: str
    age: int

class UserRead(UserCreate):
    id: int
```

* Pydantic-модели для валидации запросов и сериализации ответов

---

## 4. CRUD через FastAPI

```python
from fastapi import FastAPI, Depends
from sqlalchemy.orm import Session

app = FastAPI()

@app.post("/users/", response_model=UserRead)
def create_user(user: UserCreate, db: Session = Depends(get_db)):
    db_user = User(**user.dict())
    db.add(db_user)
    db.commit()
    db.refresh(db_user)
    return db_user

@app.get("/users/{user_id}", response_model=UserRead)
def read_user(user_id: int, db: Session = Depends(get_db)):
    return db.query(User).filter(User.id == user_id).first()
```

* Используем `Depends` для сессии базы
* Pydantic-схемы для валидации и ответа

---

## 5. Мини-задания

1. Создать эндпоинты для создания, чтения, обновления и удаления пользователей.
2. Создать эндпоинт для получения всех пользователей.
3. Добавить эндпоинты для задач (`Task`) с отношением к пользователю.
4. Использовать Pydantic для всех входящих и исходящих данных.

---

Конец файла `04_FastAPI_SQLAlchemy_Integration.md`
