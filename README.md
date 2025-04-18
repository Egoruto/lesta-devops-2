# Flask + Redis Counter API

Простое API-приложение на Flask с поддержкой Redis, упакованное в Docker. Предоставляет два эндпоинта: /ping и /count.

---

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
### Запуск через Docker Compose

```bash
docker compose up --build -d
```

После запуска доступны проверяем эндпоинты:

- `curl http://localhost:5000/ping` — статус

Ответ:

```json
{"status": "ok"}
```

- `curl http://localhost:5000/count` — счётчик

Ответ:

```json
{ "counter": 1 }
```


---

##  Автор

️ **Егор Поцелуев**