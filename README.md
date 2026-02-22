# SimplySupplements Backend

C# .NET 8 REST API backend for the [SimplySupplements](https://github.com/Norby257/SimplySupplements) accessibility-focused e-commerce platform.

---

## Core Technologies

| Layer                  | Technology     |
| ---------------------- | -------------- |
| Runtime                | .NET 8         |
| Language               | C#             |
| Database               | PostgreSQL     |
| Caching                | Redis          |
| Messaging              | Apache Kafka   |
| Containerization       | Docker         |
| Orchestration          | Kubernetes     |
| Infrastructure-as-Code | Terraform      |
| CI/CD                  | GitHub Actions |

---

## Architecture Overview

The backend follows a **event-driven, service-oriented architecture** designed to handle high-throughput supplement inventory and order operations (100K+ events).

- **REST API layer** — .NET 8 Web API handling HTTP requests from the Next.js frontend
- **PostgreSQL** — Primary relational store for products, users, and orders
- **Redis** — Caching layer for frequently accessed data (e.g., product catalog, sessions)
- **Kafka** — Message bus for decoupled event streaming between services (supplement updates, order processing)
- **Kubernetes + Docker** — Containerized deployment with orchestration for horizontal scalability
- **Terraform** — Reproducible infrastructure provisioning across environments

---

## Installation & Setup

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Docker](https://www.docker.com/get-started) & Docker Compose
- [PostgreSQL](https://www.postgresql.org/) (or run via Docker)
- [Redis](https://redis.io/) (or run via Docker)

### Local Development

1. **Clone the repository**

   ```bash
   git clone https://github.com/Norby257/simplySupplements-backend.git
   cd simplySupplements-backend
   ```

2. **Configure environment variables**

   Copy the example env file and update values for your local database and services:

   ```bash
   cp .env.example .env
   ```

3. **Start supporting services with Docker Compose**

   ```bash
   docker-compose up -d
   ```

4. **Run database migrations**

   ```bash
   dotnet ef database update
   ```

5. **Start the API**

   ```bash
   dotnet run
   ```

   The API will be available at `http://localhost:5000`.

---

## Related Repository

- **Frontend**: [SimplySupplements (Next.js/React)](https://github.com/Norby257/SimplySupplements) — Accessibility-first frontend built with React 18, TypeScript, and Next.js 14.

---

## Live Application

> Coming soon.
