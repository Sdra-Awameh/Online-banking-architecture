# 🏦 Online Banking System – Software Architecture

📘 Software Architecture project for an online banking platform, created as part of university coursework.

> Created by **Sdra Osama Awameh** – Second Semester 2024/2025

---


## 📌 Project Overview

This project presents the software architecture of an online banking system / digital wallet that supports:

- Viewing account balance and transaction history  
- Performing money transfers and bill payments  
- Managing user accounts  
- Downloading reports via FTP  
- Secure database access and optimized performance using cache and load balancer

---

## 💻 Client Presentation Layer

The system supports multiple client types for user flexibility:

- **📱 Mobile App** – for fast, on-the-go access  
- **🖥️ Web Client** – for browser-based banking  
- **🏧 ATM Interface** – for physical banking operations  

Each client communicates with the backend using **HTTPS** for secure data exchange.

---

## 🧱 Part One – Initial Architecture

The original architecture includes the following key components:

- **🔀 Load Balancer** – manages traffic and improves scalability  
- **🧩 Application Server** – main logic layer interacting with web services  
- **Web Services**:
  - `WS1`: User Account Management  
  - `WS2`: Payment & Transfer  
  - `WS3`: Transaction History  
- **⚡ Redis Cache** – speeds up access to frequently used data  
- **🗄️ Secure Database (C1)** – stores sensitive banking info  
- **🔌 Internal API Layer (C2)** – provides safe access to DB  
- **📂 FTP Server** – handles downloadable transaction statements

---

## 🔧 Part Two – Architecture Extension

The system has been extended with new architectural elements based on updated requirements:

- **🔐 Fraud Detection Service** – external API used by WS2 to validate transactions  
- **📨 Notification Service** – sends email/SMS alerts on important events  
- **🪝 Message Queue** – decouples event handling between services  
- **🔁 Redundancy & Load Balancing** – replicated services and health checks  
- **🔐 Security Layer Enhancements** – TLS, OAuth2, JWT, and encrypted data at rest  

The updated architecture improves scalability, fault tolerance, and modularity. See `Assignment.pdf` for full documentation.

---

## 🔒 Security Features

- All client–server communication uses **TLS (HTTPS)**  
- User sessions authenticated using **JWT tokens**  
- Database is encrypted at rest  
- Sensitive data is never stored in cache

---

## ⚙️ Quality Attributes Supported

| Attribute         | How the Architecture Supports It                            |
|------------------|-------------------------------------------------------------|
| **Performance**   | Redis cache and async events reduce latency                |
| **Scalability**   | Services can scale independently using microservices model |
| **Availability**  | Redundant services + load balancer ensure uptime           |
| **Security**      | TLS, JWT, OAuth2, encrypted DB                             |
| **Modifiability** | Modular design, each service can evolve independently      |
| **Maintainability** | Clear layering and separation of concerns                |
| **Cost Efficiency** | Event-based design and cache reduce resource usage       |

---



> 📌 Created by **Sdra Osama Awameh**  
> 📅 Software Architecture Course – Second Semester 2024/2025
