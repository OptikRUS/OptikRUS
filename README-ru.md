[//]: # ([💾 Скачать резюме]&#40;https://disk.yandex.ru/i/1XMum6k9oq2T7Q "Скачать резюме"&#41;)
<a href="https://github.com/OptikRUS" target="_blank">На английском</a>

# Кирилл М.[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&size=30&duration=2500&lines=%F0%9F%91%8B;+)](#кирилл-медведко)
### Старший бэкенд-разработчик👨‍💻 | Python3🐍 FastAPI Asyncio | Инфраструктура и архитектура

## Профиль

Старший бэкенд-разработчик с опытом 6+ лет в проектировании высоконагруженных распределённых систем на Python. Сократил задержку API **в 36 раз** (с 3500 мс до 95 мс) на таблицах в 20M строк, <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] --> спроектировал событийно-ориентированную платформу, обрабатывающую **16–19M событий Kafka** с нулевым простоем благодаря стратегии двойного пайплайна и feature flags,<!-- [Evidence: knowledge_base/compel/kafka_pipeline_deep_dive.md] --> стандартизировал шаблоны микросервисов, **сократив время развёртывания вдвое** <!-- [Evidence: knowledge_base/compel/microservice_template.md] -->. Катализатор роста команды: подготовил 4+ инженеров к повышению, внедрил культуру TDD/BDD и **сократил количество дефектов на 70%** <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->. Практикую **AI-native разработку** — TDD-процессы на базе Claude Code с автоматическим AI-ревью кода и промпт-инженерией для BDD-сценариев.

## Контакты:

<p align='left'>
   📫E-mail: <a href='mailto:kirillvsdev@gmail.com'>kirillvsdev@gmail.com</a>
</p>
<a href="https://t.me/kirillvsdev" target="_blank">
	<img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/kirillpydev" target="_blank">
	<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

***

## 💼 Профессиональный опыт:

<a href="https://www.compel.ru/" target="_blank">
<img height="100" src="https://weipu.ru/upload/iblock/28a/compel_logo.png" alt="Компэл">
</a>

**Старший бэкенд-разработчик** | Октябрь 2023 – По настоящее время

**Проект**: B2B-платформа микросервисов (~20M SKU в каталоге, 15–20 микросервисов, 16–20M строк/сущность)

- **UX-исследование поиска**: обнаружил, что пользователи копируют названия компонентов (а не набирают вручную) — отказался от сложного кэширования в памяти в пользу простого **ограничения на 1000 результатов**, **сэкономив недели разработки** при соответствии реальному поведению пользователей <!-- [Evidence: knowledge_base/compel/search_ux_discovery.md] -->
- **Оптимизация поиска**: снизил задержку API **с 3500 мс до 95 мс (в 36 раз)** на таблицах в 20M строк через денормализацию на основе EXPLAIN ANALYZE и B-tree индексы <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **Ускорение массового импорта**: ускорил загрузку 15–20M записей **с 8 часов до 40 минут (в 12 раз)** через цикл удаления/пересоздания индексов, пакетные вставки и устранение блокировок транзакций <!-- [Evidence: knowledge_base/compel/bulk_import_deep_dive.md] -->
- **Нагрузочное тестирование**: провёл нагрузочное тестирование с **Locust**, выявил узкие места и сократил **время отклика в 30 раз** на критических эндпоинтах <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **Событийный пайплайн на Kafka**: спроектировал пайплайн на **Kafka**, обрабатывающий **16–19M событий** с синхронизацией в режиме, близком к реальному времени, и нулевым простоем благодаря стратегии двойного пайплайна и feature flags <!-- [Evidence: knowledge_base/compel/kafka_pipeline_deep_dive.md] -->
- **Асинхронный экспорт из MinIO**: реализовал асинхронный экспорт данных из **MinIO**, автоматизировав ручные операции и снизив нагрузку на основную БД
- **Автоматизация тестирования и качество**: внедрил **pytest**, доведя покрытие кода **до 98%** и **сократив дефекты в продакшене на 70%** через BDD-практики <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **Архитектурная документация**: спроектировал **C4 L1/L2 архитектурные диаграммы**, сократив время онбординга новых инженеров и количество архитектурных совещаний **на 30%** <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **Внедрение BDD-процесса**: внедрил **BDD-сценарии** и обучил системных аналитиков их написанию, сократив переделку задач **на 35%** и повысив качество требований <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **Шаблон микросервиса**: создал **шаблон микросервиса на GitLab** со стандартной структурой проекта, CI/CD и инструментарием — **сократил время развёртывания нового сервиса вдвое** <!-- [Evidence: knowledge_base/compel/microservice_template.md] -->
- **Техническое наставничество**: обучил **3 системных аналитиков** BDD-практикам и системной архитектуре — большинство добились значительного роста навыков <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **AI-native процесс разработки**: интегрировал **Claude Code** в ежедневный цикл TDD (Red-Green-Refactor) с кастомными навыками, субагентами и плагинами — ускорил генерацию тестов, рефакторинг и автоматическое ревью кода на соответствие архитектурным стандартам
- **Исследование LLM-инфраструктуры**: провёл исследование локальных и облачных LLM-моделей (**OpenClaw** на выделенном Mac Mini), оценив стоимость и задержку для оптимального выбора модели в инструментарии разработки
- **Промпт-инженерия**: применил **NotebookLM** и структурированные промпты для генерации BDD-сценариев, документации и автоматизации тестов — сократив ручную работу при сохранении доменной точности
- **Оптимизация планирования**: улучшил процессы планирования спринтов и оценки задач, повысив точность сроков **на 35%** и сбалансировав нагрузку команды
- **Паттерн микрофронтенда**: разработал паттерн разделения микро-BE / микро-FE, улучшив горизонтальную масштабируемость и обеспечив повторное использование компонентов между проектами
- **Межсервисная коммуникация через Kafka**: интегрировал **Kafka** для асинхронного обмена сообщениями, улучшив пропускную способность обработки заказов **на 35%**
- **Стратегия декомпозиции монолита**: разработал стратегию миграции с монолита на микросервисы, сформировав приоритизированный бэклог для ускорения архитектурного перехода

**Технологический стек**: Python3 (FastAPI, SQLAlchemy, FastStream, pytest), PostgreSQL, Docker, Kubernetes, MinIO, Apache Kafka, GitLab CI, Jira, Claude Code, NotebookLM

***

<a href="https://fortech.dev/" target="_blank">
<img height="50" src="https://fortech.dev/static/a32912ca163863d6d8eba37312fee27c/fortech-standart-logo.svg" alt="Fortech">
</a>

**Бэкенд-разработчик → И.о. тимлида** | Июнь 2022 – Октябрь 2023

**Проект**: Платформа лояльности и вознаграждений (событийно-ориентированные микросервисы)

- **Событийный аналитический пайплайн**: спроектировал и внедрил аналитический пайплайн (RabbitMQ → ClickHouse), заменив тяжёлые JOIN-запросы в PostgreSQL — снизил задержку аналитики **с минут до секунд** и разгрузил OLTP-базу <!-- [Evidence: knowledge_base/fortech/transaction_analytics_deep_dive.md] -->
- **Слоистая архитектура**: внедрил слоистую архитектуру, разделив компоненты для улучшения масштабируемости, упрощения модульного тестирования и ускорения развёртывания изменений
- **Восстановление качества CI/CD**: убедил команду восстановить отключённые линтеры и проверки типов в одном merge request, установив единый стиль кода и **устранив споры о форматировании** при ревью <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Автоматизация тестирования**: внедрил **pytest**, повысив покрытие **с 0% до 92%**, **сократив время дебага на 50%** и стабилизировав релизный цикл <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Интеграция статического анализа**: интегрировал **ruff и mypy** в процесс разработки, **снизив количество статических ошибок на 25%** и ускорив ревью кода <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **CI/CD-пайплайны**: настроил пайплайны с тестами, линтерами и проверками типов, **сократив релизный цикл на 40%** и минимизировав регрессии в продакшене <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Наставничество и онбординг**: наставлял новых инженеров, ускоряя их адаптацию и выход на продуктивность; проводил кросс-командные ревью кода для раннего выявления архитектурных ошибок <!-- [Evidence: knowledge_base/fortech/mentoring_and_leadership.md] -->
- **Техническое лидерство**: проводил технические собеседования и ревью производительности, выявляя зоны роста и повышая эффективность команды; выполнял системный анализ сторонних интеграций, писал документацию и обучал разработчиков — снижая сложность внедрения
- **Микросервис загрузки файлов**: разработал микросервис загрузки файлов с поддержкой **S3/MinIO** и кэшированием метаданных в PostgreSQL, **снизив задержку доступа к файлам на ~40%** и уменьшив нагрузку ввода-вывода на хранилище <!-- [Evidence: knowledge_base/fortech/file_upload_minio_migration.md] -->
- **Внешнее наставничество**: коммерчески наставлял 2 junior-разработчиков вне работы, доведя их до уровня самостоятельных специалистов <!-- [Evidence: knowledge_base/fortech/mentoring_and_leadership.md] -->
- **Интеграция LLM и AI-евангелизм**: интегрировал **ChatGPT API** в Telegram-бот для автоматизированной подготовки алгоритмов к собеседованиям; провёл общекорпоративную презентацию по практическому применению ИИ для инженерных команд во всех офисах

**Технологический стек**: Python3 (FastAPI, Django DRF), PostgreSQL, ClickHouse, RabbitMQ, Docker, S3 (Amazon, MinIO), GitHub, Trello, ChatGPT API

---

**Проект**: Десктопное приложение — автоматическое распознавание номерных знаков

- **Интеграция OpenCV**: интегрировал алгоритм распознавания на основе OpenCV в систему видеонаблюдения, повысив скорость распознавания **на 40%** и точность **на 30%**
- **Оптимизация оценки задач**: улучшил декомпозицию задач и процесс оценки сроков, сократив время доставки функциональности **на 20%**
- **Архитектура и выбор технологий**: разработал архитектуру приложения и ERD-диаграммы, подобрав технологии для минимизации технического долга
- **Автоматизация сборки через PyInstaller**: автоматизировал упаковку Python-приложения в `.exe` через PyInstaller, оптимизировав размер и зависимости — **сократил время развёртывания на 50%**

**Технологический стек**: Python3 (OpenCV, PyQt6, SQLAlchemy, PyInstaller), SQLite, Docker, GitHub, Trello

---

**Проект**: Бэкенд мобильного приложения для контрольно-надзорных органов

- **CI/CD-инфраструктура**: развернул GitLab CI с Docker, автоматизировав полный пайплайн сборки, тестирования и развёртывания
- **Agile-лидерство**: в роли и.о. тимлида вёл декомпозицию задач и планирование спринтов, обеспечивая сбалансированную нагрузку и чёткие требования
- **Масштабируемая архитектура бэкенда**: спроектировал отказоустойчивую архитектуру мобильного бэкенда (FastAPI + Django Admin с расширенным UI + TortoiseORM)
- **REST API с RBAC**: разработал высокопроизводительный REST API с ролевым управлением доступом, обеспечив безопасный обмен данными
- **Django Admin с календарём**: создал Django Admin панель с управлением временными слотами, автоматизировав планирование и исключив конфликты бронирования
- **Интеграция Zoom API**: интегрировал Zoom API для автоматического создания видеоконференций и синхронизации календаря
- **Защита проекта**: успешно защитил проект перед стейкхолдерами с архитектурным обоснованием и демонстрацией надёжности в реальном времени

**Технологический стек**: Python3 (FastAPI, Django Admin с расширенным UI, TortoiseORM), PostgreSQL, Docker, GitHub, Telegram

***

<a href="https://artw.ru/" target="_blank">
<img height="30" src="https://artw.ru/local/templates/main_new/assets/images/logo-white.svg" alt="ARTW">
</a>

**Python бэкенд-разработчик (и.о. тимлида)** | Апрель 2021 – Июнь 2022

**Проект**: Брокерская платформа недвижимости для клиентов и брокеров

- **Сервис ипотечного калькулятора**: спроектировал и запустил в продакшен сервис ипотечного расчёта с нуля за **3–4 недели**, изолировав доменную логику через FastAPI + Django Admin с переключателями функциональности <!-- [Evidence: knowledge_base/artw/mortgage_service_details.md] -->
- **Стабилизация интеграции AmoCRM**: стабилизировал интеграцию со сторонними сервисами (AmoCRM, DvizhAPI) через **ограничитель частоты на семафорах** (asyncio Semaphore), **устранив ошибки 429** и паттерны непреднамеренного self-DDoS <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->
- **Исправление консистентности данных**: исправил критический баг консистентности данных, изменив порядок API-вызовов и записи в БД, обеспечив атомарность операций и устранив осиротевшие записи <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->
- **Внедрение тестового покрытия**: добился повышения покрытия тестами **с 0% до 50%**, значительно снизив дефекты в продакшене
- **Техническое лидерство**: взял на себя обязанности тимлида — планирование спринтов, декомпозиция фич, управление релизами
- **Рефакторинг устаревшего кода**: провёл рефакторинг устаревшей кодовой базы, снизив технический долг и улучшив поддерживаемость системы
- **Миграция данных без потерь**: управлял миграцией данных между сервисами без потерь и с минимальным простоем
- **Ревью кода и улучшение качества**: проводил кросс-командные ревью кода; внедрил линтеры как устойчивое улучшение качества перед уходом <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->

**Технологический стек**: Python3, FastAPI, TortoiseORM, Django Admin с расширенным UI, Celery, pytest, asyncio, aiohttp, PostgreSQL, Redis, GitLab, Docker, Sentry, YouTrack

***

<a href="https://careers.otr.ru/" target="_blank">
<img height="50" src="https://static.tildacdn.com/tild3439-3464-4030-b163-636236366533/Group_615.svg" alt="OTR">
</a>

**Бэкенд-разработчик** | 2018 – 2021

**Проект**: Админ-панель с интеграцией Dadata API

- **Read-through кэш для Dadata API**: реализовал кэш сквозного чтения для Dadata API через PostgreSQL с нормализованными ключами запросов и B-tree индексами, **полностью устранив блокировки за превышение лимитов API** — система оставалась стабильной даже под нагрузочным тестированием <!-- [Evidence: knowledge_base/otr/dadata_cache_details.md] -->
- **Очистка устаревших данных**: спроектировал планировщик для автоматической очистки устаревших кэшированных данных, контролируя рост БД
- **Осознанный выбор технологии**: выбрал PostgreSQL вместо Redis для кэширования — обоснованное решение для нагрузки ~100–500 запросов/день с приоритетом простоты <!-- [Evidence: knowledge_base/otr/dadata_cache_details.md] -->
- **Внедрение Git-процессов**: **заменил передачу кода zip-архивами на Git** и **установил практику кросс-командных ревью кода** внутри команды из 3 человек, улучшив качество кода и взаимодействие <!-- [Evidence: knowledge_base/otr/mentoring_and_git.md] -->

**Технологический стек**: Python (Django), PostgreSQL, Docker, GitHub, Trello

---

**Проект**: IoT-дашборд — метрики устройств (режим, близкий к реальному времени)

- **Kafka consumer-сервис**: построил Kafka consumer-сервис (один консьюмер, ~5 сообщ./сек) с кэшем в памяти для отображения последнего состояния, отдавая приоритет низкой задержке над надёжностью
- **Слой хранения на MongoDB**: реализовал слой хранения данных с **MongoDB**, снизив время отклика и разгрузив брокер
- **REST API с фильтрацией**: разработал REST API с фильтрацией и пагинацией для кэшированных метрик устройств
- **Контейнеризированное развёртывание**: настроил развёртывание на Docker с CI/CD для автоматизированного запуска сервисов

**Технологический стек**: Python (FastAPI, Motor), MongoDB, Kafka, Notion, GitHub

---

**Проект**: Telegram-бот для фотографа с админ-панелью (тимлид)

- **Система бронирования**: спроектировал систему бронирования с управлением конкурентным доступом через транзакции PostgreSQL, **исключив двойное бронирование**
- **CI/CD-автоматизация**: развернул CI/CD-пайплайн с Docker и GitHub Actions для автоматизированных сборок и релизов
- **Доменная модель**: разработал доменную модель (пользователи → слоты → бронирования), оптимизированную для планирования расписания
- **Асинхронные уведомления**: реализовал асинхронный планировщик уведомлений с пакетной отправкой в рамках лимитов Telegram API
- **Полный цикл разработки**: управлял коммуникацией с клиентом, декомпозицией задач и планированием релизов на протяжении всего жизненного цикла проекта

**Технологический стек**: Python (aiogram, Django), PostgreSQL, Docker, Trello, GitHub

***

## 🛠 Hard skills:

**Core & Backend**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)
![SQLAlchemy](https://img.shields.io/badge/sqlalchemy-%23D71F00.svg?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Pytest](https://img.shields.io/badge/pytest-%23ffffff.svg?style=for-the-badge&logo=pytest&logoColor=2f9fe3)

**Data & Messaging**

![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka)
![RabbitMQ](https://img.shields.io/badge/Rabbitmq-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)

**Infrastructure & DevOps**

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-330F63?style=for-the-badge&logo=gitlab&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Sentry](https://img.shields.io/badge/sentry-%23362D59.svg?style=for-the-badge&logo=sentry&logoColor=white)

**Architecture & Quality**

![C4 Model](https://img.shields.io/badge/C4_Model-0078D4?style=for-the-badge)
![TDD](https://img.shields.io/badge/TDD-25A162?style=for-the-badge)
![BDD](https://img.shields.io/badge/BDD-7B68EE?style=for-the-badge)
![Event Driven](https://img.shields.io/badge/Event--Driven-FF6F00?style=for-the-badge)
![Microservices](https://img.shields.io/badge/Microservices-1572B6?style=for-the-badge)
![AI-native Development](https://img.shields.io/badge/AI--native_Dev-D97757?style=for-the-badge)
![Test Coverage](https://img.shields.io/badge/Test%20Coverage-92%25-brightgreen?style=for-the-badge)

**Tools & Platforms**

![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-330F63?style=for-the-badge&logo=gitlab&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white)
![Miro](https://img.shields.io/badge/Miro-050038?style=for-the-badge&logo=Miro&logoColor=white)

**OS & IDE**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Mac OS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)
![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green)

**AI & Development Tools**

![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=claude&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white)
![ChatGPT](https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white)
![Google Gemini](https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![NotebookLM](https://img.shields.io/badge/NotebookLM-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt_Engineering-FF6F00?style=for-the-badge)
![AI Agents](https://img.shields.io/badge/AI_Agents-7B68EE?style=for-the-badge)
![AI Code Review](https://img.shields.io/badge/AI_Code_Review-25A162?style=for-the-badge)

## 🤝 Гибкие навыки:
- **Катализатор роста команды**: подготовил 4+ инженеров к повышению через структурированное обучение TDD/BDD, архитектурные воркшопы и инженерию требований
- **Опыт наставничества**:
  - **Компэл**: обучил 3 системных аналитиков ERD, Swagger и BDD-практикам, повысив качество требований
  - **Fortech** (вне работы): коммерчески наставлял 2 junior-разработчиков до уровня самостоятельных специалистов
  - **OTR**: наставлял 2 junior-разработчиков в системной архитектуре и TDD
- Быстро осваиваю новые технологические стеки — выпускал продуктовые фичи на незнакомых фреймворках уже в первый спринт
- **Совершенствование Agile-процессов** (Scrum, Kanban): измеримо сокращал время выполнения задач и повышал предсказуемость спринтов **на 35%**
- Доступно объясняю сложные архитектурные решения нетехническим стейкхолдерам — успешно защищал проекты перед руководством
- Быстро анализирую крупные системы, выявляя узкие места и оптимизируя критические пути (снижение задержки в 36 раз, ускорение импорта в 12 раз)

***

## 🎓 Высшее образование:

<p>
<a href="https://sfedu.ru/" target="_blank">
<img height="100" src="https://sfedu.ru/img/new_design_2020/logo.png" alt="ЮФУ">
</a>
</p>

* Магистратура
  * <a href="https://inep.sfedu.ru/chairs/rte/" target="_blank">Электроника и наноэлектроника</a>

* Бакалавриат
  * <a href="https://inep.sfedu.ru/chairs/rte/" target="_blank">Электроника и наноэлектроника</a>

* <a href="http://mrcpk.tgn.sfedu.ru/" target="_blank">Межотраслевой региональный центр повышения квалификации и переподготовки кадров</a>
  * Право
* Программирование на Python

***
## <p align="center">🏆 Достижения:</p>
  * Финалист <a href="https://i.moscow/lct" target="_blank">«ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2025»</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2025_msk.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2025_msk.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://i.moscow/lct" target="_blank">«ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2024»</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2024_msk.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2024_msk.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://leaders2023.innoagency.ru/task_2" target="_blank">«ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2023»</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_certificate.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/leaders2023_diplom.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://i.moscow/lct/krasnodar" target="_blank">«ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2023 Краснодарский край»</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_certificate.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_diplom.pdf" target="_blank">Диплом</a>
  * Хакатон <a href="https://xn--80aaaairqt2ajzt9a.xn--p1ai/" target="_blank">EVRAZ 2.0</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/evraz.pdf" target="_blank">Сертификат</a>
  * Хакатон <a href="https://codenrock.com/contests/scbteamchallenge-codenrock/#/" target="_blank">SOVCOMBANK TEAM CHALLENGE 2022</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/Sovcombank.pdf" target="_blank">Сертификат</a>


***
## <p align="center">💻 О себе:</p>
<p>
Старший бэкенд-разработчик, специализирующийся на высоконагруженных распределённых системах, событийно-ориентированных архитектурах и улучшении процессов разработки.
Обеспечил измеримые бизнес-результаты в B2B-маркетплейсах, платформах лояльности, платформах недвижимости и государственных системах.
Доказанный опыт трансформации инженерной культуры через наставничество, разработку через тестирование и архитектурные стандарты —
систематически повышаю эффективность команд. 4-кратный финалист хакатона «Лидеры цифровой трансформации».
</p>

***
<div align="center">

[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%23000202&size=25&multiline=true&width=640&lines=Информация+обновлена+в+марте+2026;.+.+.)](#кирилл-медведко)

</div>

***

[//]: # (<div align="center">)

[//]: # (  <a href="https://github.com/OptikRUS/resume/blob/files/files/cv_02_02_2024.pdf" download>)

[//]: # (    💾 Скачать резюме)

[//]: # (  </a>)

[//]: # (</div>)