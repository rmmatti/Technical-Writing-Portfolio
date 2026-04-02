# 🔗 MRI Engage Resident Platform – API Documentation

## 📘 Overview

This document provides end-to-end API documentation for:
- Resident Onboarding APIs  
- Payment Processing APIs  
- HLD & LLD (API perspective)  
- Workflow diagrams and UI mapping  

> Note: This document is for portfolio/demo purposes.

---

## 🔐 Authentication

Authorization: Bearer <access_token>

---

## 🌐 Base URL

https://api.mri-engage.com/v1

---

# 👤 Resident APIs

## Create Resident
POST /residents

Request:
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "phone": "9876543210",
  "unitId": "A-101",
  "moveInDate": "2026-04-01"
}

Response:
{
  "residentId": "R12345",
  "status": "Active"
}

---

## Get Resident
GET /residents/{residentId}

---

## Update Resident
PUT /residents/{residentId}

---

# 💳 Payment APIs

## Create Payment
POST /payments

Request:
{
  "residentId": "R12345",
  "amount": 15000,
  "paymentMethod": "UPI"
}

Response:
{
  "paymentId": "P98765",
  "status": "Success"
}

---

## Get Payment Status
GET /payments/{paymentId}

---

# ⚠️ Error Codes

400 Bad Request  
401 Unauthorized  
404 Not Found  
500 Server Error  

---

# 🔄 Workflow

Create Resident → Assign Unit → Generate Invoice → Payment → Update Status

---

# 🏗 HLD

Frontend → API Gateway → Services → Database → Payment Gateway

<img width="1661" height="366" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/70c2d56d-f23c-4581-a7e7-bb95d53e5e5b" />

---

# ⚙️ LLD

Modules:
- Resident Service
- Payment Service

Tables:
Residents(residentId, name, unitId, status)  
Payments(paymentId, residentId, amount, status)

## Data Flow
UI sends request to API Gateway
Gateway routes to appropriate service
Service processes logic
Data stored in database
External payment gateway invoked if required

<img width="1728" height="802" alt="mermaid-diagram (1)" src="https://github.com/user-attachments/assets/698f60a4-4e61-4131-8303-9e4399bcb00d" />

---

# 🖥 UI Mapping

Add Resident → POST /residents  
Make Payment → POST /payments  

---

# 📌 Summary

This document demonstrates API + architecture + workflow understanding for SaaS systems.
