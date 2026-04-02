# 🛠 MRI Engage Resident Platform – Admin Guide

## 📘 Overview

The **MRI Engage Resident Platform** is a resident engagement and communication solution designed for property management teams. It enables administrators to manage residents, communications, services, and system configurations from a centralized interface.

This guide provides detailed instructions for **system administrators** to configure, manage, and maintain the platform.

---

## 🎯 Target Audience

This document is intended for:

### 1. System Administrators
- Configure platform settings  
- Manage users, roles, and permissions  
- Maintain system-wide configurations  

### 2. Property Managers (Admin Access)
- Monitor resident activity  
- Configure communication workflows  
- Manage service requests and announcements  

> 📌 Prerequisite: Admin access credentials and understanding of property management workflows.

---

## 📌 Note for Portfolio Reviewers

> This guide is created for **portfolio demonstration purposes only**.  
> The workflows and configurations are representative of a real-world system.  
> In production, additional modules such as integrations, compliance settings, and advanced configurations would be included.

---

## 🔐 Admin Access & Login

### Steps

1. Navigate to the Admin Portal URL  
2. Enter **Admin Username** and **Password**  
3. Click **Login**

> ⚠️ Ensure role-based access is assigned before attempting login.

---

## 🧑‍💼 User & Role Management

### Create New User

1. Navigate to **Admin → User Management**  
2. Click **Add User**  
3. Enter details:
   - Name  
   - Email  
   - Role  
4. Assign property access  
5. Click **Save**

### Role Types

| Role            | Permissions                                      |
|-----------------|--------------------------------------------------|
| Super Admin     | Full system access                               |
| Property Admin  | Manage specific properties                       |
| Support User    | Limited access for support operations            |

---

## 🏢 Property Configuration

### Add New Property

1. Go to **Admin → Properties**  
2. Click **Add Property**  
3. Enter:
   - Property Name  
   - Location  
   - Number of Units  
4. Save configuration  

### Configure Units

| Field Name     | Description                  |
|----------------|------------------------------|
| Unit ID        | Unique identifier            |
| Floor          | Floor number                 |
| Status         | Available / Occupied         |

---

## 👥 Resident Management

### Add Resident

1. Navigate to **Residents → Add Resident**  
2. Enter resident details:
   - Name  
   - Contact Information  
   - Unit Assignment  
3. Save record  

### Resident Lifecycle

### Resident Added → Assigned Unit → Active → Move-Out → Archived


---

## 📢 Communication Management

### Create Announcement

1. Go to **Communications → Announcements**  
2. Click **Create Announcement**  
3. Add:
   - Title  
   - Message  
   - Target Audience  
4. Publish  

### Notification Channels

- Email  
- SMS  
- In-App Notifications  

---

## 🛠 Service Request Management

### Workflow

```mermaid
flowchart TD
    A[Resident Raises Request] --> B[Admin Reviews]
    B --> C[Assign to Staff]
    C --> D[Work in Progress]
    D --> E[Completed]
    E --> F[Resident Feedback]

> Billing workflow - Invoice Generated → Notification Sent → Payment Received → Receipt Issued
