# Microservices Management System

Backend system for order, inventory, delivery and analytics management,
designed for small and medium-sized businesses.

## Architecture

The system is composed of the following services:

- [API Gateway](https://github.com/andybercich/api-gateway)
- [Auth Service](https://github.com/andybercich/auth-service)
- [Order Service](https://github.com/andybercich/order-service)
- [Product Service](https://github.com/andybercich/product-service)
- [Analytics Service](https://github.com/andybercich/analytics-service)
- [Eureka Server](https://github.com/andybercich/eureka-server)
- [Common Events](https://github.com/andybercich/common-events)

## Technologies

- Java 17
- Spring Boot
- Spring Cloud
- Spring Security
- JWT
- Apache Kafka
- MySQL
- Redis
- Docker
- AWS
- N8N
- Groq AI

## Architecture Overview

The API Gateway is the public entry point of the system.
Authentication and authorization are handled using JWT.

The Order and Product services communicate through REST APIs
and publish domain events through Kafka.

Transactional Outbox is used to improve event publishing reliability,
while the Analytics Service consumes events and maintains its own
analytics data.

Eureka is used for service discovery.

## Repository Structure

| Service | Responsibility |
|---|---|
| API Gateway | Routing, authentication, authorization and rate limiting |
| Auth Service | Authentication and JWT |
| Order Service | Orders and deliveries |
| Product Service | Products and inventory |
| Analytics Service | Analytics and report generation |
| Eureka Server | Service discovery |
| Common Events | Shared Kafka event classes |
