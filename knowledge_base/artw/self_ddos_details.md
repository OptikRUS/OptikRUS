# ARTW — Self-DDoS AmoCRM: Details

## Case: Устранение self-DDoS интеграции с AmoCRM

- Problem (S/T):
  - Приложение массово отправляло запросы к AmoCRM API
  - AmoCRM отвечала 429 (Too Many Requests)
  - Интеграция постоянно падала
  - Связанная проблема: консистентность данных нарушалась при 429 ошибках

- Action (A):
  - Реализовал semaphore rate limiter (asyncio Semaphore) как декоратор
  - Ограничил concurrency к внешнему API
  - После устранения 429 — выявились скрытые проблемы с консистентностью
  - Исправил порядок операций: API call → DB write (вместо DB write → API call)

- Result (XYZ):
  - 429 ошибки полностью исчезли
  - Стабильная интеграция с AmoCRM
  - Устранена проблема консистентности данных (битые записи)

## Key Insight
> Устранение одной проблемы (rate limiting) выявило скрытую проблему (нарушение порядка операций → inconsistent state)