# SQLAlchemy Basics

## 1. Установка

```bash
pip install sqlalchemy
```

* ORM для работы с базой данных через Python-классы

---

## 2. Создание моделей

```python
from sqlalchemy import Column, Integer, String, create_engine
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    age = Column(Integer)

engine = create_engine('sqlite:///test.db')
Base.metadata.create_all(engine)
```

* `declarative_base()` – базовый класс для моделей
* `Column` – описание столбцов таблицы

---

## 3. Сессии и CRUD

```python
from sqlalchemy.orm import sessionmaker

Session = sessionmaker(bind=engine)
session = Session()

# CREATE
new_user = User(name="Andrey", age=25)
session.add(new_user)
session.commit()

# READ
user = session.query(User).filter_by(name="Andrey").first()
print(user.name, user.age)

# UPDATE
user.age = 26
session.commit()

# DELETE
session.delete(user)
session.commit()
```

* `session.add()`, `session.commit()`, `session.query()` – основные методы

---

## 4. Связи между таблицами

```python
from sqlalchemy import ForeignKey
from sqlalchemy.orm import relationship

class Task(Base):
    __tablename__ = 'tasks'
    id = Column(Integer, primary_key=True)
    title = Column(String)
    user_id = Column(Integer, ForeignKey('users.id'))
    user = relationship('User', back_populates='tasks')

User.tasks = relationship('Task', back_populates='user')
```

* `ForeignKey` – внешний ключ
* `relationship` – связь между таблицами

---

## 5. Мини-задания

1. Создать таблицу `User` и таблицу `Task` с отношением один-ко-многим.
2. Добавить несколько пользователей и задач через сессии.
3. Сделать выборку всех задач конкретного пользователя.
4. Обновить и удалить запись через сессию.

---

Конец файла `03_SQLAlchemy_Basics.md`
