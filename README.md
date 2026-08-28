# Microservices Platform (Parent Repository)

## Student Information
- **Student Name:** Shavindi R. Aloka
- **Student Number:** [241711095]
- **Slack Handle:** [Shavindi Aloka]
- **GCP Project ID:** [project-c2d114f1-e0c4-497d-a05]

---

## Project Description
This repository acts as the main parent (super) repository for the core microservice platform components. It utilizes Git Submodules to manage essential infrastructure and routing services (`api-gateway`, `config-server`, and `eureka-server`) built with Spring Cloud to ensure high availability, centralized configuration, and service discovery.

---

## Technology Stack
- **Language:** Java 25
- **Framework:** Spring Boot (Latest), Spring Cloud (Config Server, Eureka Service Registry, API Gateway)
- **Process Manager:** PM2 (for automatic restarts and process management)
- **Cloud Platform:** Google Cloud Platform (GCP)

---

## Included Submodules
This platform repository contains the following core infrastructure submodules:
1. **`api-gateway`** - Acts as the single entry point for all backend microservices.
2. **`config-server`** - Centralizes and externalizes configuration properties for all microservices.
3. **`eureka-server`** - Provides service registration and discovery capabilities.

---

## Setup / Getting Started Instructions
1. Clone this parent repository along with all its submodules:
   
   ```bash
   git clone --recursive [https://github.com/Shavindi0609/microservices-platform.git](https://github.com/Shavindi0609/microservices-platform.git)

   ```
3. If already cloned without submodules, initialize and update them:
   
   ```bash
   git submodule update --init --recursive
   ```

4. Build the platform modules using Maven:
   
   ```bash
   mvn clean install
   ```

5. Start and manage the platform services using PM2 as configured in ecosystem.config.js (ensuring multi-instance high availability and automatic restarts):
   
   ```bash
   pm2 start ecosystem.config.js
   ```
   
