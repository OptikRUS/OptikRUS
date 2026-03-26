# OTR — Deep Knowledge Base (Multi-Project)

## 🏢 Общий контекст и роль
- Role: Backend Developer → Tech Lead (в отдельных проектах)
- Period: 2018 – 2021
- Domain:
  - Государственные / окологосударственные системы (телеком / инфраструктура)
  - IoT / сбор данных с приборов (отдельные проекты)
  - B2C сервис (Telegram-бот)
- General Stack:
  - Python (Django, FastAPI, aiogram)
  - PostgreSQL, MongoDB
  - Kafka
  - Docker, GitHub Actions
- Scale:
  - Команды: 1–3 разработчика
  - Архитектура: от простых CRUD до event-driven
  - Нагрузка:
    - Dadata: ~100–500 запросов/день (низкая)
- Main Achievement:
  - Переход от начального уровня к полной ответственности за проекты:
    - проектирование БД
    - интеграции
    - CI/CD
    - коммуникация с заказчиком

---

## 🚀 Project: Админка с интеграцией Dadata

### 📌 Overview
- What:
  - Django-админка с интеграцией внешнего API Dadata для поиска и валидации адресов
- Business Value:
  - Упрощение ввода данных сотрудниками
  - Снижение количества ручных ошибок
- Scale:
  - ~100–500 запросов/день
  - ~500 пользователей внутри компании
- Архитектура:
  - Django → PostgreSQL (cache) → Dadata API
  - Scheduler для очистки

---

### 🧩 Case: Read-through cache для внешнего API

- Problem (S/T):
  - Повторяющиеся запросы к Dadata
  - Зависимость от внешнего API
  - Избыточные вызовы при одинаковых данных

- Action (A):
  - Реализовал кэш:
    - ключ: normalized_query
  - Нормализация:
    - lowercase
    - strip
  - Индексация:
    - B-tree индекс
  - Scheduler:
    - очистка устаревших данных (~каждые 2 часа)

- Result (XYZ):
  - Устранение дублирующих запросов
  - Полностью устранены баны от API (rate limiting)
  - Стабильная работа даже под нагрузочным тестированием
  - Кэш как защитный слой от rate limiting внешнего API
  - Контроль роста базы данных

---

### 🧠 Engineering Insight

- Осознанный выбор:
  - PostgreSQL вместо Redis
  - простая нормализация вместо сложных алгоритмов
- Причина:
  - низкая нагрузка
  - достаточность решения

> Principle: “Не усложнять систему без необходимости”

---

## 🚀 Project: IoT платформа (Kafka → MongoDB → API)

### 📌 Overview
- What:
  - Сервис отображения показателей с приборов (near real-time)
- Business Value:
  - Отображение актуальных данных пользователю
- Scale:
  - Низкая нагрузка (~несколько сообщений в секунду)
- Архитектура:
  - Kafka → Consumer → MongoDB → FastAPI → Frontend
  - RAM cache (последние значения)

---

### 🧩 Case: Streaming с приоритетом latency

- Problem (S/T):
  - Требуется отображение самых свежих данных
  - История не критична

- Action (A):
  - Kafka:
    - 1 topic
    - ~5 msg/sec
  - Consumer:
    - single consumer
    - ошибки → skip
  - Storage:
    - MongoDB
  - Cache:
    - in-memory (dict)

- Result (XYZ):
  - Минимальная задержка отображения данных
  - Простая и устойчивая архитектура

---

### 🧠 Trade-offs

- Latency > Reliability
- Нет retry
- Потеря данных допустима
- RAM cache вместо Redis

---

### 🧠 Architectural Insight

> Pattern: Latest State Streaming System  
(важно последнее значение, а не история)

---

## 🚀 Project: Telegram-бот для фотографа

### 📌 Overview
- What:
  - Telegram-бот + админка для записи клиентов
- Business Value:
  - Автоматизация записи
  - Устранение конфликтов
- Scale:
  - Низкая нагрузка (десятки пользователей)
- Архитектура:
  - Bot API → Backend → PostgreSQL
  - Scheduler → уведомления

---

### 🧩 Case: Domain modeling booking system

- Data Model:
  - users
  - slots
  - bookings

- Result:
  - Простая и понятная модель

---

### 🧩 Case: Concurrency control

- Problem (S/T):
  - Двойное бронирование

- Action (A):
  - PostgreSQL транзакции
  - проверка is_booked
  - обновление внутри транзакции

- Result (XYZ):
  - Консистентность данных
  - отсутствие двойных записей

---

### 🧩 Case: Асинхронные уведомления

- Problem:
  - ограничения Telegram API

- Action:
  - Scheduler
  - batch отправка сообщений

- Result:
  - стабильная доставка уведомлений

---

### 🧠 Engineering Insight

- Bottleneck:
  - Telegram API
  - а не backend

> Principle: “Сначала найди реальное ограничение системы”

---

## 🛠 Shared Leadership & Engineering Culture

- Mentoring:
  - обучение 2 junior-разработчиков (коммерческий менторинг, вне работы)
  - Результат: оба стали сильными самостоятельными разработчиками
- Engineering Culture:
  - внедрение GitHub (отказ от zip-архивов по почте)
  - Перевёл 2 локальных разработчиков на Git
  - Внедрил cross-code-review между разработчиками
  - Изменил культуру: от изолированной работы к совместной разработке
- Product Ownership:
  - прямое общение с заказчиком
- Delivery:
  - декомпозиция задач
  - управление релизами

---

## ⚖️ Security, Compliance & AI

- Compliance:
  - работа с гос/окологос системами
- Security:
  - базовый контроль доступа
- AI-Workflow:
  - —