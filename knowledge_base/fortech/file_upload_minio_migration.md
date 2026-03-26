# Fortech — File Upload Microservice (MinIO Migration)

## Context

- Проект: Loyalty & Rewards Platform
- Необходимость: миграция с S3 на MinIO из-за санкций
- Сервис: загрузка и хранение файлов (файловое хранилище)

## Architecture

- **MinIO**作为S3-совместимое хранилище
- **PostgreSQL metadata cache** для быстрого доступа к метаданным файлов
- Кэш проверяет наличие файла в БД перед запросом к MinIO
- Если файл в кэше — возвращаем метаданные из БД (быстрее)
- Если файла нет в кэше — запрашиваем из MinIO и кэшируем

## Performance

- УImprovement file access latency: ≈40% (оценка пользователя, конкретные метрики не приведены)
- Кэш снизил нагрузку на MinIO
- База данных (PostgreSQL) использована как read-through cache

## Key Points

- Проект включал миграцию с S3 на MinIO
- PostgreSQL выбран как кэш-слой (для ~100-500 запросов/день)
- Подход: intentional simplicity вместо Redis/Memcached

**Примечание:** Конкретные baseline/target метрики (в мс) не документированы. Заclaim "40%" требуется уточнение через графики мониторинга или результат нагрузочного тестирования.
