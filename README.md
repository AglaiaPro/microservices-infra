# AMA Scraping Microservices

This repository contains two separate FastAPI microservices:

- `custom-scraping` — creates and validates scraping templates for custom sector websites.
- `scraping-service` — runs the full sector scraping flow using saved templates.

## Local Setup

Create `.env` from `.env.example` and fill in your values:

```bash
cp .env.example .env
```

Required values:

- `MONGO_URI`
- `OPENAI_KEY`

Run both services with Docker Compose:

```bash
docker compose up --build
```

Service URLs:

- Custom scraping API: `http://127.0.0.1:8002/docs`
- Main scraping API: `http://127.0.0.1:8001/docs`

## Notes

Do not commit `.env` files. Use `.env.example` for documentation only.
