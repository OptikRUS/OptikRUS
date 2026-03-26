# OTR — Dadata Cache: Additional Details

## Business Impact (уточнённый)

- Problem Before:
  - API Dadata периодически банила запросы (rate limiting)
  - Сервис зависел от доступности внешнего API

- Result After:
  - Полностью устранены баны от API
  - Даже при нагрузочном тестировании API не банит
  - Кэш выступает как защитный слой от rate limiting

## Key Insight

- Кэш решил не только проблему производительности, но и стабильности:
  - До: периодические отказы из-за rate limiting
  - После: стабильная работа даже под нагрузочным тестированием
## Process Improvements

- **Внедрил Git-based workflows** (заменив ручной обмен zip-архивами через email)
- **Установил cross-team code reviews** внутри команды из 3 человек, улучшив качество кода и кросс-командную коллаборацию
