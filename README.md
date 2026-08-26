# ⚙️ BookLoop - Centralized Configuration Server

## 👤 Student Information

- **Student Name:** Amarathunga Veedagamage Dilmi Kaushalya
- **Student Number:** 241722010
- **GCP Project ID:** project-fb5ef45c-cd3d-4991-92d

------------------------------------------------------------------------

## 📌 Project Overview

This repository contains the **Spring Cloud Config Server** component for the **BookLoop** microservices platform. It provides externalized, centralized configuration management across all microservice environments (API Gateway, Catalog Service, Media Service, User Service). By decoupling environment configurations from source code, it enables seamless runtime updates without rebuilding individual microservices.

------------------------------------------------------------------------

## 🎯 Objectives

- Provide centralized configuration storage for all platform microservices.
- Maintain native environment configurations (`api-gateway.yml`, `catalog-service.yml`, `media-service.yml`, `user-service.yml`).
- Eliminate hardcoded application credentials and database URLs inside individual services.
- Support consistent configuration delivery across local and GCP Compute Engine deployments.

------------------------------------------------------------------------

## 📊 Key Features

- **Centralized Properties Management:** Single source of truth for microservice configuration profiles.
- **Native File System Storage:** Serves service-specific YAML configurations from classpath resources.
- **Dynamic Configuration Fetching:** Microservices fetch active configurations at startup via HTTP REST endpoints.
- **GCP Deployment Ready:** Fully compatible with GCP Virtual Machines and PM2 process management.

------------------------------------------------------------------------

## 📁 Project Structure

```text
bookloop-config-server/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/assignment/configserver/
│   │   │       └── ConfigServerApplication.java
│   │   └── resources/
│   │       ├── config/
│   │       │   ├── api-gateway.yml
│   │       │   ├── catalog-service.yml
│   │       │   ├── media-service.yml
│   │       │   └── user-service.yml
│   │       └── application.yml
│   └── test/
│
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md

```

---

## 🛠 Technologies Used

* **Java 25**

* **Spring Boot (3.x)**

* **Spring Cloud Config Server**

* **Maven**
* **GCP Compute Engine (IaaS Deployment)**

* **PM2 (Process Manager)**


---

## 🚀 Setup & Getting Started Instructions

### Prerequisites

* Java 25 JDK installed


* Maven installed

### Local Execution

1. **Clone the repository:**
```bash
git clone [https://github.com/dil2003-av/bookloop-config-server.git](https://github.com/dil2003-av/bookloop-config-server.git)
cd bookloop-config-server

```


2. **Build the application:**
```bash
./mvnw clean package -DskipTests

```


3. **Run the Config Server:**
```bash
java -jar target/config-server-0.0.1-SNAPSHOT.jar

```


4. **Verify Configuration Endpoint:**
Fetch service configuration via HTTP: `http://localhost:8888/catalog-service/default`

---

## 📈 Platform Integration

* **Port:** `8888`

* **Served Configurations:** `api-gateway`, `catalog-service`, `media-service`, `user-service`

* **Managed via:** PM2 Process Manager on GCP Virtual Machine instances



---

## 📌 Conclusion

The Config Server serves as the central configuration hub for BookLoop, ensuring consistent environment settings, clean code separation, and streamlined multi-service management on Google Cloud Platform.

