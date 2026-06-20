# Buildo Путешествия — Telegram Mini App

> **AI-фото себя в любой точке мира за 30 секунд**

Часть экосистемы **Buildo** (https://buildo.ru). MIT licensed. Open source.

![Buildo](https://img.shields.io/badge/Buildo-ecosystem-5B8DEF?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

---

## Что это

Mini App интерфейс продукта Путешествия. Telegram WebApp SDK, Vite SPA, Layero/Vercel deploy.

**Сценарий использования (Telegram Mini App):** Галерея локаций (100+), выбор стиля, превью

---

## Архитектура

```
Buildo Путешествия экосистема
├── shekelstrong/buildo-travel-tg          ← этот репо (Telegram-бот)
├── shekelstrong/buildo-travel-miniapp    ← Mini App
└── shekelstrong/buildo-travel-site        ← Маркетинговый сайт
```

---

## Стек

| Слой | Технология |
|---|---|
| Bot | aiogram 3.x + Redis FSM + Docker |
| Frontend | Vite + React 19 + Tailwind + Telegram WebApp SDK |
| Backend | FastAPI + YandexART + ЮKassa + CDN |
| AI (image) | YandexART (или Photoroom API fallback) |
| AI (text) | MiniMax M3 (описания локаций) |
| Deploy | Layero / Vercel / Cloudflare Pages (manual deploy by user) |

---

## Монетизация

590 ₽ за 10 фото / 1490 ₽ за 30 фото + пресеты

**Целевая аудитория:** Туристы, SMM-щики, travel-блогеры, nomads
**Конкуренты (РФ):** Teleport AI (не в РФ), FaceApp, PicsArt

---

## Деплой

```bash
cp .env.example .env
# заполни: TELEGRAM_BOT_TOKEN, OPENROUTER_API_KEY, YOOKASSA_*
docker compose up --build
```

Продакшен:
```bash
git push origin main  # GitHub Actions → SSH → VPS → docker compose up -d --build
```

---

## Связанные репо

- [buildo-travel-tg](https://github.com/shekelstrong/buildo-travel-tg) — этот репо
- [buildo-travel-miniapp](https://github.com/shekelstrong/buildo-travel-miniapp)
- [buildo-travel-site](https://github.com/shekelstrong/buildo-travel-site)
- [nemo-team-docs/projects/buildo/travel/](https://github.com/shekelstrong/nemo-team-docs/tree/main/projects/buildo/travel) — спецификация

---

## License

MIT (c) 2026 Buildo Ecosystem. Inspired by [awesome-generative-ai-apps](https://github.com/Anil-matcha/awesome-generative-ai-apps).