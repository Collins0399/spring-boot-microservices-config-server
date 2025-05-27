# spring-boot-microservices-config-server
# 📦 Spring Cloud Config Server – Centralized Configuration for Microservices

## Overview

This project implements a **Spring Cloud Config Server** that provides **centralized external configuration management** for microservices in a distributed system. It is designed to work seamlessly with Spring Boot applications, allowing each service to fetch configuration properties from a central location — typically backed by a Git repository.

> ✅ Last Updated: 20 May, 2024

---

## ✨ Key Features

- Centralized storage for microservice configurations
- Environment-specific configuration support
- Git-based configuration versioning
- Supports multiple client applications and profiles
- Fetch configurations at runtime for dynamic microservices

---

## 📘 Key Terminologies

| Term                  | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| **Config Server**     | Centralized server to manage configuration for all microservices            |
| **Config Client**     | A microservice that fetches its configuration from the Config Server        |
| **@EnableConfigServer** | Annotation to enable Config Server functionality in Spring Boot             |
| **Environment Repository** | Backend storage (e.g., Git) used to serve config properties          |
| **spring.config.import** | Property to define config server source in client applications         |

---

## 🔧 How It Works

### Config Server Setup

1. Create a Spring Boot project with the following dependencies:
   - Spring Web
   - Spring DevTools
   - Lombok
   - Spring Cloud Config Server

2. Update `application.properties`:
   ```properties
   spring.application.name=config-server
   server.port=8888
   spring.cloud.config.server.git.uri=<your-github-repo-url>
