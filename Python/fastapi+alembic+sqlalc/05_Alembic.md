# Alembic Basics

## 1. Установка

```bash
pip install alembic
```

* Alembic используется для управления миграциями базы данных

---

## 2. Инициализация

```bash
alembic init migrations
```

* Создаётся директория `migrations` с конфигом
* Настроить `alembic.ini` и `env.py` для подключения к базе

---

## 3. Создание миграций

```bash
alembic revision --autogenerate -m "Initial migration"
alembic upgrade head
```

* `--autogenerate` – Alembic сравнивает модели с текущей схемой и создаёт миграцию
* `upgrade head` – применяет миграцию

---

## 4. Работа с миграциями

* Добавление новых колонок, таблиц или изменений в модели
* Создание новой миграции:

```bash
alembic revision --autogenerate -m "Add age to user"
alembic upgrade head
```

* Откат миграции:

```bash
alembic downgrade -1
```

* Просмотр истории миграций:

```bash
alembic history
```

---

## 5. Мини-задания

1. Инициализировать Alembic в проекте с FastAPI + SQLAlchemy.
2. Создать первую миграцию для всех моделей.
3. Добавить колонку `email` в модель `User` и сделать миграцию.
4. Откатить последнюю миграцию и проверить изменения в базе.

---

Конец файла `05_Alembic.md`
