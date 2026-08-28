# Microservices Platform (Parent Repository)

## Student Information
- **Student Name:** Shavindi R. Aloka
- **Student Number:** [241711095]
- **Slack Handle:** [Shavindi Aloka]
- **GCP Project ID:** [project-c2d114f1-e0c4-497d-a05]

---

## Project Description
This repository acts as the main parent (super) repository for the core microservice platform components. It utilizes Git Submodules to manage essential infrastructure and routing services (`api-gateway`, `config-server`, and `eureka-server`) built with Spring Cloud to ensure high availability, centralized configuration, and service discovery[cite: 1].

---

## Technology Stack
- **Language:** Java 25[cite: 1]
- **Framework:** Spring Boot (Latest), Spring Cloud (Config Server, Eureka Service Registry, API Gateway)[cite: 1]
- **Process Manager:** PM2 (for automatic restarts and process management)[cite: 1]
- **Cloud Platform:** Google Cloud Platform (GCP)[cite: 1]

---

## Included Submodules
This platform repository contains the following core infrastructure submodules:
1. **`api-gateway`** - Acts as the single entry point for all backend microservices[cite: 1].
2. **`config-server`** - Centralizes and externalizes configuration properties for all microservices[cite: 1].
3. **`eureka-server`** - Provides service registration and discovery capabilities[cite: 1].

---

## Setup / Getting Started Instructions
1. Clone this parent repository along with all its submodules:
   ```bash
   git clone --recursive [https://github.com/Shavindi0609/microservices-platform.git](https://github.com/Shavindi0609/microservices-platform.git)

   ```
2. If already cloned without submodules, initialize and update them:
   ```bash
   git submodule update --init --recursive
   ```

3. Build the platform modules using Maven:
```bash
mvn clean install
```

4. Start and manage the platform services using PM2 as configured in ecosystem.config.js (ensuring multi-instance high availability and automatic restarts):
   ```bash
   pm2 start ecosystem.config.js
   ```
   
