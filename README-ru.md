[//]: # ([💾 Скачать резюме]&#40;https://disk.yandex.ru/i/1XMum6k9oq2T7Q "Скачать резюме"&#41;)
<a href="https://github.com/OptikRUS" target="_blank">На английском</a>

# Kirill M.[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&size=30&duration=2500&lines=%F0%9F%91%8B;+)](#кирилл-медведко)
### Senior Backend Engineer👨‍💻 | Python3🐍 FastAPI Asyncio | Infrastructure & Architecture

## Профиль

Senior Backend Engineer с 6+ годами опыта построения высоконагруженных распределённых систем на Python. Достиг **36x снижения задержки (latency)** на наборах данных в 20M строк, спроектировал event-driven платформу, обрабатывающую **16–19M событий Kafka**, и провёл **zero-downtime деплои** на 15–20 микросервисах. Force multiplier: наставил 4+ инженеров до повышения, внедрил культуру TDD/BDD, сократив bug rate на **70%**, и стандартизировал шаблоны микросервисов, сократив время деплоя вдвое.

## Контакты:

<p align='left'>
   📫E-mail: <a href='mailto:kirillpydev@gmail.com'>kirillpydev@gmail.com</a>
</p>
<a href="https://t.me/kirillpydev" target="_blank">
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

**Senior Backend Developer** | Октябрь 2023 – По настоящее время

**Проект**: B2B Платформа микросервисов (~20M SKU каталог, 15–20 микросервисов, 16–20M строк/сущность)

- **Search UX Discovery**: выяснил, что пользователи копируют-вставляют названия компонентов вместо печати — отказался от сложного in-memory кэширования в пользу простого ограничения результатов (1000 элементов), **сэкономив недели разработки** при соответсвии реальному поведению пользователей
- **Оптимизация поиска**: снизил API latency на 36x (с 3500 ms до 95 ms) через EXPLAIN ANALYZE-драйвенную денормализацию и B-tree индексы на таблицах 20M строк
- **Bulk import**: ускорил загрузку 15–20M записей **с 8 часов до 40 минут (12x)** через цикл drop/rebuild индексов, bulk inserts и устранение transaction locks
- **Нагрузочное тестирование**: проводил тесты с **Locust**, выявил узкие места и добился **30x улучшения response time** на критических endpoint'ах
- **Kafka event-driven pipeline**: спроектировал и внедрил pipeline на **Kafka**, обрабатывающий **16–19M событий**, достигнув near real-time синхронизации с zero downtime через dual-pipeline стратегию и feature flags
- **Асинхронный экспорт MinIO**: реализовал асинхронный экспорт данных, устранив ручные операции и снизив нагрузку на primary БД
- **Автоматизация тестирования**: внедрил **pytest**, довёл покрытие кода **до 98%** и **сократил production bugs на 70%**
- **C4-архитектурные диаграммы**: спроектировал L1/L2 диаграммы, сократив время онбординга новых инженеров и количество архитектурных митингов **на 30%**
- **BDD практики**: внедрил BDD сценарии и обучил аналитиков писать их, сократив переделку задач **на 35%** и повысив качество требований
- **Шаблон микросервиса**: создал шаблон со стандартной структурой, CI/CD и тулзингом — **сократил время деплоя нового сервиса вдвое** и обеспечил консистентность кода
- **Менторство**: наставил **4+ инженеров** в системной архитектуре, TDD и BDD — большинство учеников получили повышение или значительный рост навыков
- **Оптимизация планирования**: улучшил workflows планирования спринтов и оценок, повысив точность дедлайнов **на 35%** и сбалансировав нагрузку команды
- **Паттерн разделения на микросервисы бэкенда и фронтенда**: разработал паттерн разделения, улучшив горизонтальную масштабируемость и обеспечив повторное использование компонентов между проектами
- **Kafka для межсервисной коммуникации**: интегрировал Kafka для асинхронного обмена, улучшив пропускную способность обработки заказов **на 35%**
- **Стратегия декомпозиции монолита**: разработал стратегию и prioritized backlog для миграции монолит → микросервисы

**Технологический стек**: Python3 (FastAPI, SQLAlchemy, FastStream, pytest), PostgreSQL, Docker, Kubernetes, MinIO, Kafka, GitLab, Jira

---

<a href="https://fortech.dev/" target="_blank">
<img height="50" src="https://fortech.dev/static/a32912ca163863d6d8eba37312fee27c/fortech-standart-logo.svg" alt="Fortech">
</a>

**Backend Engineer → Acting Lead** | Июнь 2022 – Октябрь 2023

**Проект**: Loyalty & Rewards Platform (Микросервисы)

- **Event-driven аналитика**: спроектировал и внедрил аналитический pipeline (RabbitMQ → ClickHouse), заменив PostgreSQL-based reporting — снизил latency аналитики **с минут до секунд** и разгрузил OLTP БД
- **Слоистая архитектура**: внедрил слоистую архитектуру, разделив компоненты для улучшения масштабируемости, упрощения модульного тестирования и ускорения деплоев изменений
- **CI/CD quality initiative**: получил buy-in команды на восстановление отключённых линтеров и type checkers в одном MR, установив единый code style, **исключив дебаты по форматированию** в code review
- **Автоматизация тестов**: внедрил **pytest**, повысил покрытие **с 0% до 92%**, **сократив время дебага на 50%** и стабилизировав релизный цикл
- **Интеграция линтеров**: интегрировал **ruff & mypy** в процесс разработки, **снизив статические ошибки на 25%** и ускорив код-ревью
- **CI/CD пайплайны**: настроил пайплайны с тестами, линтерами и type checkers, **сократив релизный цикл на 40%** и минимизировав production regressions
- **Менторство и онбординг**: наставлял и онboardил новых инженеров, ускоряя ramp-up; проводил cross-team code reviews для выявления архитектурных ошибок
- **Техinical interviews и performance reviews**: проводил интервью и ревью, выявляя зоны роста и повышая эффективность команды
- **Анализ сторонних интеграций**: выполнял анализ сторонних интеграций, документировал процессы интеграции и обучал разработчиков — снижая сложность внедрения
- **File upload microservice**: разработал microservice с **S3/MinIO** support и PostgreSQL metadata caching, **снизив latency доступа к файлам на 40%** и уменьшив I/O нагрузку на storage
- **Наставничество джуниоров**: коммерчески наставлял 2 junior-разработчиков, выросших до самостоятельных контрибьюторов

**Технологический стек**: Python3 (FastAPI, Django DRF), PostgreSQL, ClickHouse, RabbitMQ, Docker, S3 (Amazon, MinIO), GitHub, Trello

---

**Проект**: Desktop Application — Automatic License Plate Recognition

- **OpenCV интеграция**: интегрировал алгоритм распознавания в surveillance system, улучшив скорость детекции **на 40%** и точность **на 30%**
- **Оптимизация планирования**: улучшил task decomposition и estimation, сократив время delivery фич **на 20%**
- **Архитектура**: разработал архитектуру приложения и ERD диаграммы, подобрав технологии, минимизируя technical debt
- **PyInstaller упаковка**: автоматизировал упаковку Python приложения в .exe, оптимизировал размер и зависимости — **сократив время деплоя на 50%**

**Технологический стек**: Python3 (OpenCV, PyQt6, SQLAlchemy, PyInstaller), SQLite, Docker, GitHub, Trello

---

**Проект**: Mobile Application Backend для Regulatory Authorities

- **CI/CD инфраструктура**: deployed GitLab CI + Docker, автоматизировав полный build-test-deploy пайплайн
- **Task decomposition & sprint planning**: как acting team lead, обеспечивал balanced workload и чёткие требования
- **Архитектура мобильного бэкенда**: спроектировал scalable и fault-tolerant архитектуру (FastAPI + Django Admin + TortoiseORM)
- **REST API с RBAC**: разработал высокопроизводительный REST API с role-based access control
- **Django admin с календарём**: создал Django admin панель с calendar slot management, автоматизировав scheduling и исключив booking conflicts
- **Zoom API интеграция**: интегрировал Zoom API для автоматического создания video conference и calendar sync
- **Защита проекта**: успешно защитил проект перед stakeholders с архитектурным обоснованием и live reliability demo

**Технологический стек**: Python3 (FastAPI, Django-админка, TortoiseORM), PostgreSQL, Docker, GitHub, Telegram

---

<a href="https://artw.ru/" target="_blank">
<img height="30" src="https://artw.ru/local/templates/main_new/assets/images/logo-white.svg" alt="ARTW">
</a>

**Python Backend Developer (Acting Lead)** | Апрель 2021 – Июнь 2022

**Проект**: Real Estate Brokerage Platform для Clients и Brokers

- **Mortgage Calculator Service**: спроектировал и отправил в production mortgage calculation service с нуля за 3–4 недели, изолировав доменную логику через FastAPI + Django Admin с feature toggles
- **AmoCRM интеграция**: стабилизировал third-party интеграцию (AmoCRM, DvizhAPI) через semaphore-based rate limiter, **устранив 429 ошибки** и self-DDoS паттерны
- **Critical data consistency bug**: исправил баг консистентности данных, переупорядочив API-call/DB-write sequence, обеспечив atomic operations и устранив orphaned records
- **Test coverage advocacy**: продвигал покрытие тестами **с 0% до 50%**, значительно снизив production defects
- **Team lead responsibilities**: принимал на себя lead обязанности: sprint planning, feature decomposition, release management
- **Legacy code refactoring**: рефакторил legacy код, снижая technical debt и улучшая maintainability
- **Data migration**: управлял миграцией данных между сервисами с zero data loss и minimal downtime
- **Code reviews & quality**: проводил cross-team code reviews; внедрил линтеры как lasting quality improvement перед уходом

**Технологический стек**: Python3, FastAPI, TortoiseORM, Django-админка, Celery, pytest, asyncio, aiohttp, PostgreSQL, Redis, GitLab, Docker, Sentry, YouTrack

---

<a href="https://careers.otr.ru/" target="_blank">
<img height="50" src="https://static.tildacdn.com/tild3439-3464-4030-b163-636236366533/Group_615.svg" alt="OTR">
</a>

**Backend Engineer** | 2018 – 2021

**Проект**: Admin Panel с интеграцией Dadata API

- **Dadata API кэширование**: реализовал read-through cache для Dadata API через PostgreSQL с нормализованными query keys и B-tree индексами, устранив дублирующие внешние вызовы и **все баны от rate limiting** — система оставалась стабильной даже под нагрузочным тестированием
- **Очистка stale данных**: спроектировал scheduler для автоматической очистки устаревших кэшированных данных, контролируя рост БД
- **Простота архитектуры**: выбрал PostgreSQL вместо Redis — консервативное решение, адекватное для ~100–500 запросов/день
- **Git-based workflows**: **внедрил Git** вместо zip-архивов и **установил cross-team code reviews** внутри команды из 3 человек, улучшив качество кода и коллаборацию

**Технологический стек**: Python (Django), PostgreSQL, Docker, GitHub, Trello

---

**Проект**: IoT Dashboard — Device Metrics (Near Real-Time)

- **Kafka consumer service**: построил Kafka consumer service (single consumer, ~5 msg/sec) с in-memory кэшем для отображения последних данных, отдавая приоритет низкой задержке над надёжностью
- **MongoDB persistence**: реализовал слой persistence с **MongoDB**, снизив время отклика и разгрузив broker
- **REST API с фильтрацией**: разработал REST API с фильтрацией и пагинацией для кэшированных device metrics
- **Docker CI/CD**: настроил Docker-based deployment с CI/CD для automated service rollout

**Технологический стек**: Python (FastAPI, Motor), MongoDB, Kafka, Notion, GitHub

---

**Проект**: Telegram Bot для Photographer Services с Admin Panel (Tech Lead)

- **Booking system**: спроектировал booking system с PostgreSQL transaction-based concurrency control, исключив double-booking edge cases
- **CI/CD**: deployed CI/CD pipeline с Docker и GitHub Actions для automated builds и releases
- **Domain model**: разработал domain model (users → slots → bookings), оптимизированный для scheduling workflows
- **Async notifications**: реализовал async notification scheduler с batch delivery, работая в рамках Telegram API rate limits
- **Full-cycle delivery**: управлял client communication, task decomposition, и release planning end-to-end

**Технологический стек**: Python (aiogram, Django), PostgreSQL, Docker, Trello, GitHub

---

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

**AI Tools**

![Claude](https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=claude&logoColor=white)
![ChatGPT](https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white)
![Google Gemini](https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)

## 🤝 Гибкие навыки (Soft Skills):

- **Force Multiplier**: наставил 4+ инженеров до уровня promotion через структурированное обучение TDD/BDD, архитектурные воркшопы и инженерию требований
- **Трек наставничества**:
  - **Compel**: обучил 3 системных аналитиков ERD, Swagger и BDD практикам, повысив качество требований
  - **Fortech** (вне работы): коммерчески наставлял 2 junior-разработчиков, выросших до самостоятельных контрибьюторов
  - **OTR**: наставил 2 junior-разработчиков в системной архитектуре и TDD
- Быстро осваиваю новые технологические стеки — демонстрировал выпуск продуктовых фич на незнакомых фреймворках в первый спринт
- **Улучшаю Agile процессы** (Scrum, Kanban), измеримо сокращая время выполнения задач и улучшая предсказуемость спринтов **на 35%**
- Коммуницирую сложные архитектурные решения с нетехническими стейкхолдерами — успешно защищал проекты перед руководством
- Быстро анализирую крупномасштабные системы, находя узкие места и оптимизируя критические пути (36x улучшение задержки, 12x ускорение импорта)

***

## 🎓 Высшее образование:

<p>
<a href="https://sfedu.ru/" target="_blank">
<img height="100" src="https://sfedu.ru/img/new_design_2020/logo.png" alt="SFU">
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
  * Финалист <a href="https://i.moscow/lct" target="_blank">"ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2025"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2025_msk.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2025_msk.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://i.moscow/lct" target="_blank">"ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2024"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2024_msk.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2024_msk.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://leaders2023.innoagency.ru/task_2" target="_blank">"ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2023"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_certificate.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/leaders2023_diplom.pdf" target="_blank">Диплом</a>
  * Финалист <a href="https://i.moscow/lct/krasnodar" target="_blank">"ЛИДЕРЫ ЦИФРОВОЙ ТРАНСФОРМАЦИИ 2023 Краснодарский край"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_certificate.pdf" target="_blank">Сертификат</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_diplom.pdf" target="_blank">Диплом</a>
  * <a href="https://xn--80aaaairqt2ajzt9a.xn--p1ai/" target="_blank">EVRAZ 2.0</a> Хакатон
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/evraz.pdf" target="_blank">Сертификат</a>
  * <a href="https://codenrock.com/contests/scbteamchallenge-codenrock/#/" target="_blank">SOVCOMBANK TEAM CHALLENGE 2022</a> Хакатон
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/Sovcombank.pdf" target="_blank">Сертификат</a>

***

## <p align="center">💻 О себе:</p>
<p>
Senior Backend Engineer, специализирующийся на высоконагруженных распределённых системах, event-driven архитектурах и developer experience.
Принёс измеримый бизнес-impакt в B2B маркетплейсы, loyalty платформы, real estate платформы и government systems.
Доказанный track record трансформации инженерной культуры через mentorship, test-driven development и архитектурные стандарты —
последовательно повышая эффективность команд. 4x финалист хакатона "Лидеры цифровой трансформации".
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