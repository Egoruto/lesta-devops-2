# Flask + Redis Counter API

Простое API-приложение на Flask с поддержкой Redis, упакованное в Docker. Предоставляет два эндпоинта: /ping и /count.

---
 
### Запуск через Docker Compose

```bash
docker compose up --build
```

После запуска доступны проверяем эндпоинты:

- `http://localhost:5000/ping` — статус
- `http://localhost:5000/count` — счётчик

## Структура проекта

```
my-flask-app/
├── app.py                 # Flask-приложение
├── requirements.txt       # Зависимости Python
├── Dockerfile             # Сборка Flask-образа
├── docker-compose.yml     # Оркестрация сервисов
└── README.md              # Документация проекта
```
---

##  API Эндпоинты

### `GET /ping`

Проверка, что сервис работает:

```json
{ "status": "ok" }
```

---

### `GET /count`

Инкрементирует Redis-счётчик и возвращает текущее значение:

```json
{ "counter": 1 }
```

---

## Используемые технологии

- [Python 3.9](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/)
- [Redis (Alpine)](https://hub.docker.com/_/redis)
- [Docker Compose](https://docs.docker.com/compose/)

---

##  Автор

️ **Егор Поцелуев**