[//]: # ([💾 Скачать резюме]&#40;https://disk.yandex.ru/i/1XMum6k9oq2T7Q "Скачать резюме"&#41;)
[<a href="https://github.com/OptikRUS/resume/blob/master/README.md" target="_blank">На русском</a>]
# Kirill M.[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&size=30&duration=2500&lines=%F0%9F%91%8B;+)](#кирилл-медведко)
### Senior Backend Engineer👨‍💻 | Python3🐍 FastAPI Asyncio | Infrastructure & Architecture

## Value Proposition

Senior Backend Engineer with 6+ years building high-load distributed systems in Python. Delivered **36x latency reduction** on 20M-row datasets, architected event-driven platforms processing **19M+ Kafka events**, and drove **zero-downtime deployments** across 15–20 microservices. Force multiplier: mentored 4+ engineers to promotion, embedded TDD/BDD culture that cut bug rates by **70%**, and standardized microservice templates that halved deployment time. Master's in Electronics & Nanoelectronics with a Law certification — a unique edge for compliance-aware system design.

## Contacts:

📞Phone: +7-778-237-89-68
<p align='left'>
   📫E-mail: <a href='mailto:kirillmedvedkodeveloper@gmail.com'>kirillmedvedkodeveloper@gmail.com</a>
</p>
<a href="https://t.me/kirillpydev" target="_blank">
	<img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>
</a>
<a href="https://api.whatsapp.com/send?phone=77782378968" target="_blank">
	<img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/kirillpydev" target="_blank">
	<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

***

## 💼 Professional experience:
<a href="https://www.compel.ru/" target="_blank">
<img height="100" src="https://weipu.ru/upload/iblock/28a/compel_logo.png" alt="Компэл">
</a>

**Senior Backend Developer** | Oct 2023 – Present

**Project**: B2B Microservices Platform (~20M SKU catalog, 15–20 microservices, 16–20M rows/entity)
- Optimized search queries across 20M-row tables, reducing API latency **from 3500 ms to 95 ms (36x)** via EXPLAIN ANALYZE-driven denormalization and targeted B-tree indexing
- Accelerated bulk data import of 15–20M records **from 8 hours to 40 minutes (12x)** by orchestrating index drop/rebuild cycles, bulk inserts, and transaction lock elimination
- Conducted load testing with **Locust**, pinpointed system bottlenecks, and delivered a **30x response time improvement** on critical endpoints
- Architected **Kafka**-based event-driven pipeline processing **16–19M events**, achieving near real-time data synchronization with zero downtime via dual-pipeline strategy and feature flags
- Engineered asynchronous data export from **MinIO**, eliminating manual workflows and reducing system load on the primary database
- Introduced automated testing with **pytest**, driving **code coverage to 98%** and **reducing production bugs by 70%**
- Designed **C4 L1/L2 architecture diagrams**, cutting new engineer onboarding time and reducing architecture alignment meetings by **30%**
- Implemented **BDD scenarios** and trained analysts to author them, reducing task rework by **35%** and elevating requirement quality across teams
- Created a **microservice template** with standardized project structure, CI/CD, and tooling — reducing new service deployment time **by 2x** and enforcing code consistency
- **Mentored 4+ engineers** in system architecture, TDD, and BDD practices — most mentees achieved promotions or significant skill advancement
- Optimized sprint planning and estimation workflows, increasing deadline accuracy by **35%** and balancing team workload distribution
- Designed micro-BE / micro-FE separation pattern, improving horizontal scalability and enabling cross-project component reuse
- Integrated **Kafka** for asynchronous inter-service communication, improving order processing throughput by **35%**
- Developed decomposition strategy for monolith-to-microservices migration, producing a prioritized backlog that accelerated the architectural transition

**Tech Stack**: Python3 (FastAPI, SQLAlchemy, FastStream, pytest), PostgreSQL, Docker, Kubernetes, MinIO, Kafka, GitLab, Jira

***

<a href="https://fortech.dev/" target="_blank">
<img height="50" src="https://fortech.dev/static/a32912ca163863d6d8eba37312fee27c/fortech-standart-logo.svg" alt="Fortech">
</a>

**Backend Engineer → Acting Lead** | Jun 2022 – Oct 2023

**Project**: Transaction Analytics & Web Applications (Microservices)
- Designed and shipped a transaction **analytics pipeline** (RabbitMQ → ClickHouse), replacing PostgreSQL-based reporting — reduced analytics latency **from minutes to seconds** and offloaded OLTP database
- Implemented a **layered architecture**, decoupling components to improve scalability, simplify unit testing, and accelerate change deployment
- Automated testing with **pytest**, raising coverage **from 0% to 92%**, **cutting debugging time by 50%**, and stabilizing release cadence
- Integrated linters (**ruff & mypy**) into the development workflow, **reducing static errors by 25%** and accelerating code reviews
- Configured **CI/CD pipelines** with tests, linters, and type checkers, **cutting release cycle time by 40%** and minimizing production regressions
- **Mentored and onboarded** new engineers, accelerating ramp-up time; conducted cross-team code reviews to catch architectural flaws early
- Conducted **technical interviews and performance reviews**, identifying growth areas and boosting overall team efficiency
- Performed **system analysis** for third-party integrations, authored integration documentation, and trained developers — reducing adoption friction
- Developed a file upload microservice with **S3/MinIO** support and PostgreSQL metadata caching, **reducing file access latency by 40%** and decreasing storage I/O load

**Tech Stack**: Python3 (FastAPI, Django DRF), PostgreSQL, ClickHouse, RabbitMQ, Docker, S3 (Amazon, MinIO), GitHub, Trello

---
**Project**: Desktop Application — Automatic License Plate Recognition
- Integrated an OpenCV-based recognition algorithm into a surveillance system, improving detection speed by **40%** and accuracy by **30%**
- Optimized task decomposition and estimation, reducing feature delivery time by **20%**
- Designed application architecture and ERD diagrams, selecting technologies that minimized technical debt
- Automated Python application packaging into `.exe` via PyInstaller, optimizing size and dependencies — reducing deployment time by **50%**

**Tech Stack**: Python3 (OpenCV, PyQt6, SQLAlchemy, PyInstaller), SQLite, Docker, GitHub, Trello

---
**Project**: Mobile Application Backend for Regulatory Authorities
- Deployed CI/CD infrastructure with GitLab CI and Docker, automating the full build-test-deploy pipeline
- Led task decomposition and sprint planning as acting team lead, ensuring balanced workload and clear requirements
- Designed scalable and fault-tolerant mobile backend architecture (FastAPI + Django Admin + TortoiseORM)
- Developed a high-performance REST API with role-based access control, ensuring secure data exchange
- Built a Django admin panel with calendar slot management, automating scheduling and eliminating booking conflicts
- Integrated Zoom API for automatic video conference provisioning and calendar synchronization
- Successfully defended the project before stakeholders with architectural justification and live reliability demo

**Tech Stack**: Python3 (FastAPI, Django-админка, TortoiseORM), PostgreSQL, Docker, GitHub, Telegram

***

<a href="https://artw.ru/" target="_blank">
<img height="30" src="https://artw.ru/local/templates/main_new/assets/images/logo-white.svg" alt="ARTW">
</a>

**Python Backend Developer (Acting Lead)** | Apr 2021 – Jun 2022

**Project**: Real Estate Brokerage Platform for Clients and Brokers
- Designed and shipped a **mortgage calculation service** from scratch in 3–4 weeks, isolating domain logic via FastAPI + Django Admin with feature toggles
- Stabilized third-party integrations (AmoCRM, DvizhAPI) by implementing a semaphore-based rate limiter, **eliminating 429 errors** and self-DDoS patterns
- Fixed a critical data consistency bug by reordering API-call/DB-write sequence, ensuring atomic operations and eliminating orphaned records
- Advocated for and drove test coverage **from 0% to 50%**, significantly reducing production defects
- Took on team lead responsibilities: sprint planning, feature decomposition, release management
- Refactored legacy codebase, reducing technical debt and improving system maintainability
- Managed data migration between services with zero data loss and minimal downtime
- Conducted cross-team code reviews; introduced linters as a lasting quality improvement before transitioning out

**Tech Stack**: Python3, FastAPI, TortoiseORM, Django-админка, Celery, pytest, asyncio, aiohttp, PostgreSQL, Redis, GitLab, Docker, Sentry, YouTrack

***

## NDA

**Project**: Telegram Bot for Photographer Services with Admin Panel (Tech Lead)
- Architected a booking system with PostgreSQL transaction-based concurrency control, eliminating double-booking edge cases
- Deployed CI/CD pipeline with Docker and GitHub Actions for automated builds and releases
- Designed a domain model (users → slots → bookings) optimized for scheduling workflows
- Implemented async notification scheduler with batch delivery, working within Telegram API rate limits
- Mentored a junior developer, introduced Git-based workflows (replacing zip-archive handoffs)
- Managed client communication, task decomposition, and release planning end-to-end

**Tech Stack**: Python (aiogram, Django), PostgreSQL, Docker, Trello, GitHub

---
**Project**: IoT Dashboard — Device Metrics (Near Real-Time)
- Built a Kafka consumer service (single consumer, ~5 msg/sec) with in-memory caching for latest-state display, prioritizing latency over durability
- Implemented data persistence layer with **MongoDB**, reducing response time and offloading broker
- Developed a REST API with filtering and pagination for cached device metrics
- Configured Docker-based deployment with CI/CD for automated service rollout

**Tech Stack**: Python (FastAPI, Motor), MongoDB, Kafka, Notion, GitHub

---
**Project**: NDA | Mobile Application
- Designed database schema optimized for mobile data access patterns
- Deployed CI/CD infrastructure with Docker and GitLab CI
- Developed a REST API ensuring fast and secure data exchange between mobile client and server
- Built and improved the admin interface, reducing support workload
- Integrated third-party services for extended functionality

**Tech Stack**: Python (Django DRF), PostgreSQL, Docker, GitHub, Trello

---
**Project**: Admin Panel with External API Integration
- Implemented a read-through cache for Dadata API using PostgreSQL with normalized query keys and B-tree indexing, eliminating duplicate external calls
- Designed a scheduler for automatic cleanup of stale cached data, controlling database growth
- Architected the caching layer with intentional simplicity (PostgreSQL over Redis) — appropriate for ~100–500 requests/day workload

**Tech Stack**: Python (Django), PostgreSQL, Docker, GitHub, Trello

***

## 🛠 Hard skills:

**Core & Backend**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)

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

**Architecture & Quality**

![C4 Model](https://img.shields.io/badge/C4_Model-0078D4?style=for-the-badge)
![TDD](https://img.shields.io/badge/TDD-25A162?style=for-the-badge)
![BDD](https://img.shields.io/badge/BDD-7B68EE?style=for-the-badge)
![Event Driven](https://img.shields.io/badge/Event--Driven-FF6F00?style=for-the-badge)
![Microservices](https://img.shields.io/badge/Microservices-1572B6?style=for-the-badge)

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

## 🤝 Soft skills:
- **Force Multiplier**: mentored 4+ engineers to promotion-level growth through structured TDD/BDD training and architecture workshops
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
Delivered measurable business impact across B2B marketplaces, fintech analytics, real estate platforms, and government systems.
Proven track record of transforming engineering culture through mentorship, test-driven development, and architectural standards —
consistently turning teams into higher-performing units. 3x hackathon finalist (Leaders of Digital Transformation).
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