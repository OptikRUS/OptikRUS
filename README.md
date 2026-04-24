[//]: # ([💾 Download Resume]&#40;https://disk.yandex.ru/i/1XMum6k9oq2T7Q "Download Resume"&#41;)
<a href="https://github.com/OptikRUS/OptikRUS/blob/main/README-ru.md" target="_blank">На русском</a>
# Kirill M.[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&size=30&duration=2500&lines=%F0%9F%91%8B;+)](#kirill-medvedko)
### Senior Backend Engineer👨‍💻 | Python3🐍 FastAPI Asyncio | Infrastructure & Architecture

## Profile

Senior Backend Engineer with 6+ years building high-load distributed systems in Python. Delivered **36x latency reduction** (from 3500ms to 95ms) on 20M-row datasets <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->, architected event-driven platforms processing **16–19M Kafka events** with zero-downtime via dual-pipeline strategy and feature flags <!-- [Evidence: knowledge_base/compel/kafka_pipeline_deep_dive.md] -->, and standardized microservice templates that **halved deployment time** <!-- [Evidence: knowledge_base/compel/microservice_template.md] -->. Force multiplier: mentored 4+ engineers to promotion-level growth, embedded TDD/BDD culture that **cut bug rates by 70%** <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->.
## Contacts:

<p align='left'>
   📫E-mail: <a href='mailto:kirillvsdev@gmail.com'>kirillvsdev@gmail.com</a>
</p>
<a href="https://t.me/kirillvsdev" target="_blank">
	<img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/kirillvsdev" target="_blank">
	<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

***

## 💼 Professional experience:
<a href="https://www.compel.ru/" target="_blank">
<img height="100" src="https://weipu.ru/upload/iblock/28a/compel_logo.png" alt="Compel">
</a>

**Senior Backend Developer** | Oct 2023 – Present

**Project**: B2B Microservices Platform (~20M SKU catalog, 15–20 microservices, 16–20M rows/entity)

- **Search UX Discovery**: Discovered users copy-paste component names (not type them) — pivoted from complex in-memory caching to simple **1000-item result limit**, **saving weeks of development** while matching actual user behavior <!-- [Evidence: knowledge_base/compel/search_ux_discovery.md] -->
- **Search optimization**: Optimized queries across 20M-row tables, reducing API latency **from 3500ms to 95ms (36x)** via EXPLAIN ANALYZE-driven denormalization and B-tree indexing <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **Bulk import acceleration**: Accelerated 15–20M record imports **from 8 hours to 40 minutes (12x)** through index drop/rebuild cycles, bulk inserts, and transaction lock elimination <!-- [Evidence: knowledge_base/compel/bulk_import_deep_dive.md] -->
- **Load testing & bottleneck resolution**: Conducted **Locust** load testing, identified system bottlenecks, and delivered **30x response time improvement** on critical endpoints <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **Kafka event-driven pipeline**: Architected **Kafka**-based pipeline processing **16–19M events** with near real-time synchronization and zero downtime via dual-pipeline strategy and feature flags <!-- [Evidence: knowledge_base/compel/kafka_pipeline_deep_dive.md] -->
- **Async MinIO export**: Engineered asynchronous data export from **MinIO**, eliminating manual workflows and reducing primary database load
- **Test automation & quality**: Introduced **pytest**, achieving **98% code coverage** and **70% reduction in production bugs** through BDD practices <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **Architecture documentation**: Designed **C4 L1/L2 architecture diagrams**, cutting new engineer onboarding time and reducing architecture alignment meetings by **30%** <!-- [Evidence: knowledge_base/compel/search_optimization_deep_dive.md] -->
- **BDD process innovation**: Implemented **BDD scenarios** and trained system analysts to author them, reducing task rework by **35%** and elevating requirement quality <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **Microservice template**: Created **GitLab-based microservice template** with standardized project structure, CI/CD, and tooling — **reduced new service deployment time by 2x** <!-- [Evidence: knowledge_base/compel/microservice_template.md] -->
- **Technical mentorship**: Mentored **3 system analysts** in BDD practices and system architecture — most achieved significant skill advancement <!-- [Evidence: knowledge_base/compel/bdd_process.md] -->
- **Agile process improvement**: Optimized sprint planning and estimation workflows, increasing deadline accuracy by **35%** and balancing team workload
- **Micro-frontend pattern**: Designed micro-BE / micro-FE separation pattern, improving horizontal scalability and enabling cross-project component reuse
- **Kafka inter-service communication**: Integrated **Kafka** for asynchronous messaging, improving order processing throughput by **35%**
- **Monolith decomposition strategy**: Developed strategy for monolith-to-microservices migration, producing prioritized backlog that accelerated architectural transition

**Tech Stack**: Python3 (FastAPI, SQLAlchemy, FastStream, pytest), PostgreSQL, Docker, Kubernetes, MinIO, Apache Kafka, GitLab CI, Jira

***

<a href="https://fortech.dev/" target="_blank">
<img height="50" src="https://fortech.dev/static/a32912ca163863d6d8eba37312fee27c/fortech-standart-logo.svg" alt="Fortech">
</a>

**Backend Engineer → Acting Lead** | Jun 2022 – Oct 2023

**Project**: Loyalty & Rewards Platform (Event-Driven Microservices)

- **Event-driven analytics pipeline**: Designed and shipped analytics pipeline (RabbitMQ → ClickHouse), replacing heavy PostgreSQL JOIN queries — reduced analytics latency **from minutes to seconds** and offloaded OLTP database <!-- [Evidence: knowledge_base/fortech/transaction_analytics_deep_dive.md] -->
- **Layered architecture**: Implemented layered architecture, decoupling components to improve scalability, simplify unit testing, and accelerate deployment of changes
- **CI/CD quality restoration**: Gained team buy-in to restore disabled linters and type checkers in single MR, establishing unified code style that **eliminated formatting debates** in code reviews <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Test automation**: Automated testing with **pytest**, raising coverage **from 0% to 92%**, **cutting debugging time by 50%**, and stabilizing release cadence <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Static analysis integration**: Integrated linters (**ruff & mypy**) into development workflow, **reducing static errors by 25%** and accelerating code reviews <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **CI/CD pipeline**: Configured CI/CD pipelines with tests, linters, and type checkers, **cutting release cycle time by 40%** and minimizing production regressions <!-- [Evidence: knowledge_base/fortech/ci_cd_quality.md] -->
- **Team mentoring & onboarding**: Mentored and onboarded new engineers, accelerating ramp-up time; conducted cross-team code reviews to catch architectural flaws early <!-- [Evidence: knowledge_base/fortech/mentoring_and_leadership.md] -->
- **Technical leadership**: Conducted technical interviews and performance reviews, identifying growth areas and boosting team efficiency; performed system analysis for third-party integrations, authored documentation, and trained developers — reducing adoption friction
- **File upload microservice**: Developed file upload microservice with **S3/MinIO** support and PostgreSQL metadata caching, **reducing file access latency by ~40%** and decreasing storage I/O load <!-- [Evidence: knowledge_base/fortech/file_upload_minio_migration.md] -->
- **External mentorship**: Commercially mentored 2 junior developers outside work to strong independent contributors <!-- [Evidence: knowledge_base/fortech/mentoring_and_leadership.md] -->

**Tech Stack**: Python3 (FastAPI, Django DRF), PostgreSQL, ClickHouse, RabbitMQ, Docker, S3 (Amazon, MinIO), GitHub, Trello

---

**Project**: Desktop Application — Automatic License Plate Recognition

- **OpenCV integration**: Integrated OpenCV-based recognition algorithm into surveillance system, improving detection **speed by 40%** and **accuracy by 30%**
- **Estimation optimization**: Optimized task decomposition and estimation processes, reducing feature delivery time by **20%**
- **Architecture & technology selection**: Designed application architecture and ERD diagrams, selecting technologies that minimized technical debt
- **PyInstaller automation**: Automated Python application packaging into `.exe` via PyInstaller, optimizing size and dependencies — **reduced deployment time by 50%**

**Tech Stack**: Python3 (OpenCV, PyQt6, SQLAlchemy, PyInstaller), SQLite, Docker, GitHub, Trello

---

**Project**: Mobile Application Backend for Regulatory Authorities

- **CI/CD automation**: Deployed GitLab CI with Docker, automating full build-test-deploy pipeline
- **Agile leadership**: Led task decomposition and sprint planning as acting team lead, ensuring balanced workload and clear requirements
- **Scalable backend architecture**: Designed fault-tolerant mobile backend (FastAPI + Django Admin with custom UI extensions + TortoiseORM)
- **REST API with RBAC**: Developed high-performance REST API with role-based access control, ensuring secure data exchange
- **Django admin scheduling**: Built Django admin panel with calendar slot management, automating scheduling and eliminating booking conflicts
- **Zoom API integration**: Integrated Zoom API for automatic video conference provisioning and calendar synchronization
- **Stakeholder defense**: Successfully defended project before stakeholders with architectural justification and live reliability demo

**Tech Stack**: Python3 (FastAPI, Django Admin with custom UI extensions, TortoiseORM), PostgreSQL, Docker, GitHub, Telegram

***

<a href="https://artw.ru/" target="_blank">
<img height="30" src="https://artw.ru/local/templates/main_new/assets/images/logo-white.svg" alt="ARTW">
</a>

**Python Backend Developer (Acting Lead)** | Apr 2021 – Jun 2022

**Project**: Real Estate Brokerage Platform for Clients and Brokers

- **Mortgage calculator service**: Designed and shipped mortgage calculation service from scratch in **3–4 weeks**, isolating domain logic via FastAPI + Django Admin with custom UI extensions and feature toggles <!-- [Evidence: knowledge_base/artw/mortgage_service_details.md] -->
- **AmoCRM integration stabilization**: Stabilized third-party integrations (AmoCRM, DvizhAPI) by implementing **semaphore-based rate limiter** (asyncio Semaphore), **eliminating 429 errors** and self-DDoS patterns <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->
- **Data consistency fix**: Fixed critical data consistency bug by reordering API-call/DB-write sequence, ensuring atomic operations and eliminating orphaned records <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->
- **Test coverage advocacy**: Advocated for and drove test coverage **from 0% to 50%**, significantly reducing production defects
- **Technical leadership**: Took on team lead responsibilities — sprint planning, feature decomposition, release management
- **Legacy refactoring**: Refactored legacy codebase, reducing technical debt and improving system maintainability
- **Zero-downtime data migration**: Managed data migration between services with zero data loss and minimal downtime
- **Code quality improvement**: Conducted cross-team code reviews; introduced linters as lasting quality improvement before transitioning out <!-- [Evidence: knowledge_base/artw/self_ddos_details.md] -->

**Tech Stack**: Python3, FastAPI, TortoiseORM, Django Admin with custom UI extensions, Celery, pytest, asyncio, aiohttp, PostgreSQL, Redis, GitLab, Docker, Sentry, YouTrack

***

<a href="https://careers.otr.ru/" target="_blank">
<img height="50" src="https://static.tildacdn.com/tild3439-3464-4030-b163-636236366533/Group_615.svg" alt="OTR">
</a>

**Backend Engineer** | 2018 – 2021

**Project**: Admin Panel with Dadata API Integration

- **Read-through cache implementation**: Implemented PostgreSQL-based read-through cache for Dadata API with normalized query keys and B-tree indexing, **eliminating all API rate-limiting bans** — system remained stable even under load testing <!-- [Evidence: knowledge_base/otr/dadata_cache_details.md] -->
- **Cache maintenance**: Designed automated scheduler for stale cached data cleanup, controlling database growth
- **Technology choice**: Chose PostgreSQL over Redis for caching layer — appropriate for ~100–500 requests/day workload with intentional simplicity <!-- [Evidence: knowledge_base/otr/dadata_cache_details.md] -->
- **Development process improvement**: Introduced **Git-based workflows** to replace zip-archive handoffs and established **cross-team code reviews** within the team (3 people), improving code quality and collaboration <!-- [Evidence: knowledge_base/otr/mentoring_and_git.md] -->

**Tech Stack**: Python (Django), PostgreSQL, Docker, GitHub, Trello

---

**Project**: IoT Dashboard — Device Metrics (Near Real-Time)

- **Kafka consumer service**: Built Kafka consumer service (single consumer, ~5 msg/sec) with in-memory caching for latest-state display, prioritizing low latency over durability
- **MongoDB persistence**: Implemented data persistence layer with **MongoDB**, reducing response time and offloading Kafka broker
- **REST API development**: Developed REST API with filtering and pagination for cached device metrics
- **Containerized deployment**: Configured Docker-based deployment with CI/CD for automated service rollout

**Tech Stack**: Python (FastAPI, Motor), MongoDB, Kafka, Notion, GitHub

---

**Project**: Telegram Bot for Photographer Services with Admin Panel (Tech Lead)

- **Booking system architecture**: Architected booking system with PostgreSQL transaction-based concurrency control, **eliminating double-booking** edge cases
- **CI/CD automation**: Deployed GitLab CI with Docker for automated builds and releases
- **Domain modeling**: Designed domain model (users → slots → bookings) optimized for scheduling workflows
- **Async notifications**: Implemented async notification scheduler with batch delivery, operating within Telegram API rate limits
- **End-to-end delivery**: Managed client communication, task decomposition, and release planning throughout project lifecycle

**Tech Stack**: Python (aiogram, Django), PostgreSQL, Docker, Trello, GitHub

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

## 🤝 Soft skills:
- **Force Multiplier**: mentored 4+ engineers to promotion-level growth through structured TDD/BDD training, architecture workshops, and requirements engineering
- **Mentorship track record**:
  - **Compel**: trained 3 system analysts in ERD, Swagger, and BDD practices, elevating requirement quality across teams
  - **Fortech** (outside work): commercially mentored 2 junior developers to strong independent contributors
  - **OTR**: mentored 2 junior developers in system architecture and TDD
- Adapt to new tech stacks within two weeks — demonstrated by shipping production features on unfamiliar frameworks during first sprint
- Drive **Agile process improvements** (Scrum, Kanban) that measurably reduced task completion time and improved sprint predictability by **35%**
- Communicate complex architectural decisions to non-technical stakeholders — successfully defended projects before executive review boards
- Analyze large-scale systems rapidly, identifying bottlenecks and optimizing critical paths (36x latency improvement, 12x import acceleration)

***

## 🎓 Higher education:

<p>
<a href="https://sfedu.ru/" target="_blank">
<img height="100" src="https://sfedu.ru/img/new_design_2020/logo.png" alt="SFU">
</a>
</p>

* Master's Degree
  * <a href="https://inep.sfedu.ru/chairs/rte/" target="_blank">Electronics and Nanoelectronics</a>

* Bachelor's Degree
  * <a href="https://inep.sfedu.ru/chairs/rte/" target="_blank">Electronics and Nanoelectronics</a>

* <a href="http://mrcpk.tgn.sfedu.ru/" target="_blank">Intersectoral Regional Center for Advanced Training and Retraining of Personnel</a>
  * Law
* Python Programming

***
## <p align="center">🏆 Achievements:</p>
  * Finalist of <a href="https://i.moscow/lct" target="_blank">"LEADERS OF DIGITAL TRANSFORMATION 2025"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2025_msk.pdf" target="_blank">Certificate</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2025_msk.pdf" target="_blank">Diploma</a>
  * Finalist of <a href="https://i.moscow/lct" target="_blank">"LEADERS OF DIGITAL TRANSFORMATION 2024"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_certificate_lct_2024_msk.pdf" target="_blank">Certificate</a>
    * <a href="https://github.com/OptikRUS/resume/blob/files/files/finalist_diploma_lct_2024_msk.pdf" target="_blank">Diploma</a>
  * Finalist of <a href="https://leaders2023.innoagency.ru/task_2" target="_blank">"LEADERS OF DIGITAL TRANSFORMATION 2023"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_certificate.pdf" target="_blank">Certificate</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders2023_diplom.pdf" target="_blank">Diploma</a>
  * Finalist of <a href="https://i.moscow/lct/krasnodar" target="_blank">"LEADERS OF DIGITAL TRANSFORMATION 2023 Krasnodar Region"</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_certificate.pdf" target="_blank">Certificate</a>
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/leaders_2023_krasnodar_diplom.pdf" target="_blank">Diploma</a>
  * <a href="https://xn--80aaaairqt2ajzt9a.xn--p1ai/" target="_blank">EVRAZ 2.0</a> Hackathon
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/evraz.pdf" target="_blank">Certificate</a>
  * <a href="https://codenrock.com/contests/scbteamchallenge-codenrock/#/" target="_blank">SOVCOMBANK TEAM CHALLENGE 2022</a> Hackathon
    * <a href="https://github.com/OptikRUS/resume/blob/master/files/Sovcombank.pdf" target="_blank">Certificate</a>


***
## <p align="center">💻 About:</p>
<p>
Senior Backend Engineer specializing in high-load distributed systems, event-driven architectures, and developer experience.
Delivered measurable business impact across B2B marketplaces, loyalty platforms, real estate platforms, and government systems.
Proven track record of transforming engineering culture through mentorship, test-driven development, and architectural standards —
consistently turning teams into higher-performing units. 4x hackathon finalist (Leaders of Digital Transformation).
</p>

***
<div align="center">

[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%23000202&size=25&multiline=true&width=640&lines=Information+updated+in+March+2026;.+.+.)](#кирилл-медведко)

</div>

***

[//]: # (<div align="center">)

[//]: # (  <a href="https://github.com/OptikRUS/resume/blob/files/files/cv_02_02_2024.pdf" download>)

[//]: # (    💾 Скачать резюме)

[//]: # (  </a>)

[//]: # (</div>)