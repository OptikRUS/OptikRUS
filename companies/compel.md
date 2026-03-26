# COMPEL — Deep Knowledge Base

## 🏢 Общий контекст и роль
- Role: Senior Backend Developer  
- Period: Oct 2023 – now  
- Domain: B2B Marketplace (электронные компоненты)  
- General Stack: Python (FastAPI), PostgreSQL, Kafka, MinIO, Kubernetes  
- Scale:
  - ~15–20 микросервисов  
  - ~100 RPS/service (low RPS, data-heavy)  
  - DB: 16–20M rows / entity  
  - Kafka: до 16–19M событий (snapshot)  
- Main Achievement:
  - latency: 3500ms → 95ms (x36)  
  - import: 8h → 40 min (x12)  
  - bug rate: -70%  
  - 0 downtime на ключевых сервисах  

---

## 🚀 Project: B2B Microservices Platform

### 📌 Overview
- B2B каталог (~20M SKU)  
- AXAPTA → Kafka → микросервисы → PostgreSQL  
- Event-driven архитектура  

---

## 🧩 Case: Search Optimization

### Problem
- latency ~3500ms  
- seq scan (миллионы строк)  
- join-heavy  

### Action
- EXPLAIN ANALYZE  
- remove joins (денормализация)  
- add indexes  

### Result (XYZ)
- X: 3500ms → 95ms (x36)  
- Y: API latency + explain analyze  
- Z: index usage + remove joins  

### Trade-offs
- faster reads  
- denormalization  
- eventual consistency  

---

## 🧩 Case: Bulk Import Optimization

### Problem
- 15–20M записей  
- импорт → 8 часов  

### Action
- drop indexes  
- bulk insert  
- rebuild  

### Result (XYZ)
- X: 8h → 40 min (x12)  
- Y: batch time  
- Z: B-tree rebuild  

---

## 🧩 Case: Kafka Event-Driven

### Scale
- 16–19M events  
- processing ~1 hour  
- 2–3 consumers  

### Result
- near real-time  
- lag only during snapshot  

---

## 🧩 Case: Zero Downtime

- dual pipeline  
- feature flags  

### Result
- 0 downtime  

---

## 📊 Metrics
- services: 15–20  
- RPS: ~100  
- DB: 16–20M rows  
- Kafka: 16–19M events  
