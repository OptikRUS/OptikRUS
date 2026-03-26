# ARTW — Deep Knowledge Base (Multi-Project)

## 🏢 Общий контекст и роль
- Role: Python Backend Developer (частично Team Lead)
- Period: Apr 2021 – Jun 2022
- Domain: Real Estate / Marketplace
- General Stack: Python (FastAPI, Django Admin, asyncio), PostgreSQL, Redis (ограниченно), Docker, Celery, Sentry

### 📊 Scale
- RPS: ~5–10
- Тип нагрузки:
  - I/O-bound (интеграции)
  - batch processing (импорт недвижимости)
- Основные bottlenecks:
  - внешние API (AmoCRM, Движ API)
  - batch импорт данных

### 🏆 Main Achievement
- Спроектировал и реализовал ипотечный сервис с нуля
- Стабилизировал интеграции (устранил self-DDoS)
- Исправил критичную проблему консистентности
- Предотвратил внедрение неэффективного batch-решения
- Продвинул инженерную культуру (тесты, DDD)

---

## 🚀 Project: Real Estate Platform

### 📌 Overview
- What:
  Платформа для клиентов, брокеров и администраторов

- Business Value:
  - Ускорение продаж недвижимости через digital
  - Централизация брокеров
  - Монетизация через платное бронирование (~10–15k)

- Scale:
  - Низкий RPS (~5–10)

- Архитектура:
  - Modular Monolith
  - Точечное выделение сервисов

---

## 🧩 Case: Mortgage Calculator Service

### 🧩 Case: Выделение ипотечного сервиса

- Problem (S/T):
  - Сложная бизнес-логика ипотеки
  - Жесткая зависимость от внешнего API
  - Требование быстрого запуска (~3–4 недели)

- Action (A):
  - FastAPI + Django Admin
  - Feature toggle через админку
  - Переписал API client + тесты
  - Вёл декомпозицию и релизы

- Result (XYZ):
  - X: изолировали доменную логику
  - Y: time-to-market ~3–4 недели
  - Z: за счет выделения сервиса

---

## 🧩 Case: Self-DDoS интеграций

- Problem:
  - Массовые запросы → 429

- Action:
  - semaphore rate limiter (декоратор)

- Result:
  - X: стабилизация интеграций
  - Y: исчезли 429
  - Z: контроль concurrency

---

## 🧩 Case: Нарушение консистентности

- Problem:
  - запись создавалась до ответа API → inconsistent state

- Action:
  - сначала atomic
  - затем изменил порядок (API → DB)

- Result:
  - X: убрал рассинхрон
  - Y: исчезли битые записи
  - Z: корректный порядок операций

---

## 🧩 Case: Batch импорт недвижимости

- Problem:
  - долгий импорт
  - высокая нагрузка

- Action:
  - выявил anti-pattern
  - остановил внедрение плохого решения

- Result:
  - X: предотвращена деградация
  - Y: avoided проблемы
  - Z: архитектурное влияние

---

## 🛠 Engineering Culture

- pytest: 0 → 50%
- DDD (инициатива)
- менторинг
- замещение Team Lead

---

## ⚖️ Security

- role-based access

