# 🏦 Online Banking System – Software Architecture

📘 Software Architecture project for an online banking platform, created as part of university coursework.

> Created by **Sdra Osama Awameh** – Second Semester 2024/2025

---

## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Client Presentation Layer](#client-presentation-layer)
- [Main Components](#main-components)
- [System Architecture Diagram](#system-architecture-diagram)
- [Security Features](#security-features)
- [Quality Attributes Supported](#quality-attributes-supported)
- [How to View](#how-to-view)
- [Contents](#contents)

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
- **🖥️ Web Client** – for users who prefer browser-based access
- **🏧 ATM Interface** – for physical banking needs (cash withdrawal/deposit)

Each client communicates with the backend using **HTTPS** for secure data transfer.

---

## 🧠 Main Components

- **🔀 Load Balancer** – distributes incoming requests across services for performance and availability
- **🧩 App Server**:
  - `WS1`: User Account Management
  - `WS2`: Payment & Transfer
  - `WS3`: Transaction History & Reporting
- **⚡ Cache (e.g., Redis)** – stores frequently accessed data like dashboard info
- **🗄️ Database Server**:
  - `C1`: Secure Banking Database
  - `C2`: Internal REST API Layer for DB access
- **📂 FTP Server** – for downloading user transaction reports

---


## 🔒 Security Features

- All client-server communication uses **HTTPS**
- Sensitive data (e.g., passwords) is **never cached**
- Database access is **restricted and encrypted**
- ATM connections secured through **private/internal channels**

---

## ⚙️ Quality Attributes Supported

| Attribute       | How the Architecture Supports It |
|----------------|----------------------------------|
| **Performance**     | Caching reduces DB load and improves speed |
| **Scalability**     | Load balancer supports horizontal scaling |
| **Availability**    | Requests are routed to healthy services |
| **Security**        | HTTPS, secure DB, no sensitive caching |
| **Modifiability**   | Modular REST services can be updated separately |
| **Maintainability** | Clear structure and separation of concerns |
| **Cost Efficiency** | Efficient use of cache and scalable design |

---

## 🚀 How to View

- Open the `Assignment.pdf` for the full write-up  
- View architecture diagrams inside the `Architecture_Diagrams/` folder  
- Review all components and quality mapping in the `README.md`

---

## 📁 Contents

- `README.md` – this file  
- `Assignment.pdf` – full assignment report  
- `Architecture_Diagrams/` – contains system architecture visuals  

---

> 📌 Created by **SDRA Osama Awameh**  
> 📅 Software Architecture Course – Second Semester 2024/2025
