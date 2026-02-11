# EShop – Modular Monolith & Microservices Architecture

[cite_start]A high-performance e-commerce platform built with **.NET 8** and **C# 12**, demonstrating advanced architectural patterns and a strategic migration path from a **Modular Monolith** to **Microservices** using the **Strangler Fig Pattern**.

## 🏗️ Architectural Excellence

[cite_start]This repository serves as a reference implementation for modern enterprise-grade patterns, showcasing the skills applied in high-performance financial systems[cite: 8, 54]:

1.  **Modular Monolith (Modulith):** Organized for high cohesion and low coupling between business modules.
2.  [cite_start]**Vertical Slice Architecture (VSA):** Focusing on features over layers to improve maintainability and delivery speed.
3.  [cite_start]**Domain-Driven Design (DDD):** Encapsulating complex business logic within core domains.
4.  [cite_start]**CQRS w/ MediatR:** Strict separation of Commands and Queries, enhanced with **Validation Pipeline Behaviors** via **FluentValidation**[cite: 9, 43, 55].

---

## 🛠️ Key Modules & Technologies

### 1. Catalog Module
* [cite_start]**Framework:** Built with **ASP.NET Core Minimal APIs** and **Carter**[cite: 3, 48].
* [cite_start]**Persistence:** Data management using **EF Core (Code-First)** with **PostgreSQL**[cite: 42, 90].
* **Cross-Cutting Concerns:** Integrated Health Checks, Global Exception Handling, and Structured Logging.

### 2. Basket Module
* [cite_start]**Caching:** High-speed data access using **Redis** distributed cache[cite: 43, 91].
* **Design Patterns:** Implementation of Proxy, Decorator, and Cache-aside patterns.
* [cite_start]**Reliability:** Guaranteed message delivery using the **Outbox Pattern**.

### 3. Identity & Security
* [cite_start]**Authentication:** Secured with **OAuth2** and **OpenID Connect** via **Keycloak**[cite: 43, 91].
* [cite_start]**Authorization:** JWTBearer token integration for secure identity management[cite: 20, 65].

---

## 📡 Communication & Messaging

[cite_start]The system handles complex integrations similar to those managed in large-scale environments[cite: 16, 61]:

* **Synchronous:** In-process method calls for high-performance module interaction.
* [cite_start]**Asynchronous:** Event-driven communication using **RabbitMQ** and **MassTransit**[cite: 18, 63].
* [cite_start]**Reliable Messaging:** Advanced implementation of the Outbox Pattern to ensure data consistency across services.

---

## 🐳 Infrastructure & DevOps

* [cite_start]**Containerization:** The entire ecosystem is orchestrated using **Docker Compose**[cite: 43, 91].
* [cite_start]**CI/CD Readiness:** Structured for automated builds and high-quality code standards[cite: 23, 68].
* [cite_start]**Observability:** Integrated monitoring and logging via **Elasticsearch and Kibana**[cite: 24, 69].

---

## 🚦 Getting Started

1.  **Clone the repository:**
    ```bash
    git clone [your-repository-url]
    ```
2.  **Infrastructure:**
    * Ensure Docker Desktop is running.
    * Run `docker-compose up -d` to launch PostgreSQL, Redis, RabbitMQ, and Keycloak.
3.  **Launch:**
    * Open the solution in Visual Studio 2022 or VS Code.
    * Run the application and explore the Minimal API endpoints via Swagger.
