# Flask + Redis Counter API

Простое API-приложение на Flask с поддержкой Redis, упакованное в Docker. Предоставляет два эндпоинта: /ping и /count.

---
 
### Запуск через Docker Compose

```bash
docker compose up --build -d
```

После запуска доступны проверяем эндпоинты:

#### Через терминале
- `curl http://localhost:5000/ping` — статус
- `curl http://localhost:5000/count` — счётчик

#### В браузере
- `http://localhost:5000/count` - статус
- `http://localhost:5000/count` - счетчик

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

Счетчик посещений

```json
{ "counter": 1 }
```

---

##  Автор

️ **Егор Поцелуев**