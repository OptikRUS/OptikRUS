# Fortech --- Deep Knowledge Base (Multi-Project)

## 🏢 Общий контекст и роль

Role: Backend Engineer → Acting Lead\
Period: Июнь 2022 -- Октябрь 2023\
General Stack: Python, FastAPI, PostgreSQL, Docker, RabbitMQ,
ClickHouse, S3/MinIO

Domain: Internal systems / analytics / integrations / mobile backend

Main Achievement: Внедрение event-driven аналитики (RabbitMQ →
ClickHouse), улучшение качества разработки (CI/CD, тесты), ускорение
релизов и снижение багов

------------------------------------------------------------------------

## 🚀 Project 1: Transaction Analytics System

Описание: Система аналитики финансовых транзакций поверх сервиса
обработки балансов пользователей.

### 🧩 Case: Переход на Event-Driven аналитику

Problem (S/T):\
Аналитика строилась через PostgreSQL → высокая нагрузка, latency до
минут, нет real-time

Action (A):\
Main Service → RabbitMQ → Consumer → ClickHouse\
Запись по одному событию (без batching)

Result (XYZ):\
Latency: минуты → секунды\
Снижение нагрузки на PostgreSQL\
Self-service аналитика

------------------------------------------------------------------------

## 🚀 Project 2: File Storage Service

Описание: Сервис загрузки файлов с S3/MinIO

### 🧩 Case: Оптимизация доступа

Problem: высокая latency доступа\
Action: кэширование метаданных в PostgreSQL\
Result: ускорение доступа \~40%

------------------------------------------------------------------------

## 🚀 Project 3: Mobile Backend (Regulatory)

Описание: Backend для мобильного приложения контрольных органов

### 🧩 Case: Быстрый запуск backend

Problem: нет инфраструктуры\
Action: FastAPI + Django admin + CI/CD\
Result: ускорен time-to-market, автоматизация процессов

------------------------------------------------------------------------

## 🚀 Project 4: License Plate Recognition

Описание: CV desktop приложение

### 🧩 Case: Computer Vision с нуля

Problem: нет экспертизы\
Action: OpenCV + Tesseract + PyQt\
Result: точность +30%, скорость +40%

------------------------------------------------------------------------

## 🛠 Shared Leadership

Mentoring: обучение команды\
DX: CI/CD, линтеры → релизы быстрее\
Quality: pytest → меньше багов

------------------------------------------------------------------------

## ⚖️ Architecture

-   Event-driven\
-   OLTP → OLAP разделение\
-   микросервисы

------------------------------------------------------------------------

## ⚖️ Security & AI

Security: роли и права\
AI: потенциальное использование для тестов и анализа
