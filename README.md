# ReNova Connect — Infrastructure

**Infrastructure** repository for orchestrating all **ReNova Connect** services:  
Transform API, Collector, Telegram and WhatsApp bots, Redis, and PostgreSQL.

---

## 🧩 Services

| Service | Description |
|----------|-------------|
| PostgreSQL | Main database |
| Redis | Cache and broker |
| Transform API | Core data API |
| Collector | Data synchronization |
| Telegram Bot | Telegram interface |
| WhatsApp Bot | WhatsApp interface |

---

## ⚙️ Run

```bash
docker-compose up --build
```

---

## 🧱 Docker Compose Example

```
version: "3.8"
services:
  db:
    image: postgres:16
  redis:
    image: redis:7
  collector:
    build: ../renova-connect-collector
  transform_api:
    build: ../renova-connect-transform-api
  telegram_bot:
    build: ../renova-connect-telegram-bot
  whatsapp_bot:
    build: ../renova-connect-whatsapp-bot
```

---

## 🧾 License
MIT License  
© ReNova Beauty Hub
