# 🏥 Healthcare Microservices Platform

This project is a microservices-based healthcare application built using Java, Spring Boot, Docker, and AWS services. It features event-driven and real-time communication, secured APIs, and scalable deployment using ECS and Kafka.

---

## 🛠️ Tech Stack

- **Languages & Frameworks**: Java, Spring Boot
- **Microservices Orchestration**: Docker, ECS
- **Database**: PostgreSQL (via AWS RDS)
- **API Communication**: REST, gRPC
- **Event-driven Messaging**: Kafka (via MSK)
- **Security**: Bearer token authentication
- **Infrastructure**: AWS (LocalStack for local development)
- **CI/CD & Infra as Code**: Terraform / AWS CLI
- **Testing**: Integration Tests

---

## 🧱 Microservices Overview

- **Auth Service**: Handles user authentication.
- **Billing Service**: Generates and handles billing using gRPC.
- **Patient Service**: Manages patient data and sends Kafka messages.
- **Analytics Service**: Consumes Kafka topics for analytics.
- **Notification Service**: Sends notifications based on Kafka events.
- **API Gateway**: Routes requests to backend services.

---

## 🔁 Communication Flow

- **REST** between Frontend ↔ API Gateway ↔ Auth/Patient Services
- **gRPC** between Patient Service ↔ Billing Service
- **Kafka** for asynchronous messaging (Patient Service → Kafka Topic → Consumers)

---
