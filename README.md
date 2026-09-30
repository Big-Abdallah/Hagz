# Hagz

### Less Searching. More Playing.

Hagz is a full-stack web application designed to simplify the process of finding, booking, and managing sports courts.

The platform connects **Players**, **Court Owners**, and **Administrators** through a simple and organized digital experience.

---

## 📌 Project Overview

Finding a suitable sports court can often involve searching through different sources, contacting court owners, and asking about availability manually.

**Hagz** aims to simplify this process by providing a centralized platform where players can:

* Discover available sports courts
* Search and filter courts
* View court information and pricing
* Check available time slots
* Create and manage bookings

At the same time, court owners can manage their courts, availability, and booking requests, while administrators can review courts and manage users.

---

## 🎯 Project Goal

The main goal of Hagz is to make sports court booking:

* **Simple**
* **Fast**
* **Clear**
* **Organized**

### Core Idea

> **Less Searching. More Playing.**

---

## 👥 System Roles

### Player

Players can:

* Register and log in
* Search for courts
* Filter courts by area and price
* View court details
* Check available time slots
* Create bookings
* Cancel bookings
* View their bookings

### Court Owner

Court owners can:

* Register and log in
* Add courts
* Manage court information
* Upload court photos
* Set court prices
* Define availability
* View booking requests
* Accept or reject bookings

### Administrator

Administrators can:

* Log in to the administration system
* Review submitted courts
* Approve or reject courts
* Manage users

---

## 🚀 Core Features

* User Authentication
* Role-Based Access Control
* Court Management
* Court Search
* Court Filtering
* Availability Management
* Booking Management
* Booking Cancellation
* Court Approval Workflow
* User Management
* Responsive Web Interface

---

## 📋 Project Scope

### Included in V1

* Authentication
* Authorization and RBAC
* Court management
* Court search and filtering
* Court availability
* Booking management
* Administrative moderation
* User management

### Out of Scope for V1

The following features are intentionally excluded from the first version:

* Online Payments
* Subscriptions
* Advertising
* Maps and Navigation
* Advanced Recommendation Systems
* Native Mobile Applications
* Advanced Analytics
* Loyalty and Rewards

These features may be considered as future development.

---

# 🏗️ Project Structure

The project is organized according to the Software Engineering development lifecycle.

```text
Hagz/
│
├── 01-Documentation/
│   ├── Project-Overview.md
│   ├── Project-Description.md
│   ├── Project-Scope.md
│   ├── Team-Members.md
│   └── References.md
│
├── 02-Requirements/
│   ├── SRS/
│   │   └── Software-Requirements-Specification.md
│   │
│   ├── Functional-Requirements/
│   │   ├── Player.md
│   │   ├── Court-Owner.md
│   │   └── Admin.md
│   │
│   └── Non-Functional-Requirements.md
│
├── 03-Analysis/
│   ├── Actors/
│   │   └── Actors.md
│   │
│   ├── Use-Cases/
│   │   └── Use-Case-Descriptions.md
│   │
│   ├── User-Stories/
│   │   ├── Player.md
│   │   ├── Court-Owner.md
│   │   └── Admin.md
│   │
│   └── Business-Rules.md
│
├── 04-Design/
│   ├── Architecture/
│   │   └── System-Architecture.png
│   │
│   ├── Database/
│   │   ├── Database-Schema.md
│   │   └── ERD.png
│   │
│   ├── UML/
│   │   ├── Class-Diagram.png
│   │   ├── Sequence-Diagrams/
│   │   │   └── Create-Booking.png
│   │   └── Activity-Diagrams/
│   │       └── Booking-Workflow.png
│   │
│   ├── UI-UX/
│   │   ├── Design-System/
│   │   └── Mockups/
│   │
│   └── API/
│       └── API-Documentation.md
│
├── 05-Implementation/
│   ├── frontend/
│   ├── backend/
│   └── admin-dashboard/
│
├── 06-Testing/
│   ├── Test-Plan.md
│   ├── Test-Cases.xlsx
│   ├── Test-Results.md
│   ├── Bug-Reports.md
│   └── Screenshots/
│
├── 07-Deployment/
│   ├── Deployment-Guide.md
│   ├── Environment.md
│   └── Architecture.md
│
├── 08-Presentation/
│   ├── Demo-Script.md
│   └── Screenshots/
│
└── README.md
```

---

# 🎨 Design System

Hagz follows a minimal, modern, and sporty visual identity.

### Brand Colors

| Color      | Hex       |
| ---------- | --------- |
| Deep Navy  | `#0B1220` |
| Lime       | `#B6F03C` |
| White      | `#FFFFFF` |
| Light Gray | `#E5E7EB` |

### Typography

* **Poppins** — English
* **Cairo** — Arabic

### Design Personality

* Modern
* Clean
* Sporty
* Confident
* Energetic
* Friendly
* Organized

The interface focuses on clarity and action rather than visual complexity.

---

# 🔄 Main User Journey

The main player journey is:

```text
Find Court
     ↓
Explore Court
     ↓
Check Availability
     ↓
Select Time
     ↓
Create Booking
     ↓
Booking Confirmation
```

The owner workflow is:

```text
Add Court
     ↓
Court Review
     ↓
Court Approval
     ↓
Define Availability
     ↓
Receive Booking Requests
     ↓
Accept / Reject Booking
```

---

# 🗄️ Main Data Entities

The current database design contains:

* User
* Court
* CourtImage
* Availability
* Booking

Main relationships include:

```text
User ────────< Court
Court ───────< CourtImage
Court ───────< Availability
User ────────< Booking
Court ───────< Booking
```

A detailed database design is available in:

`04-Design/Database/Database-Schema.md`

---

# 🔌 API

The backend API is organized under:

```text
/api/v1
```

The API documentation contains the available endpoints, request methods, authorization requirements, and response status codes.

See:

`04-Design/API/API-Documentation.md`

---

# 🧪 Testing

Testing documentation is located in:

```text
06-Testing/
```

It includes:

* Test Plan
* Test Cases
* Test Results
* Bug Reports
* Testing Screenshots

Testing will cover the main functional and non-functional requirements of the system.

---

# 🚀 Deployment

Deployment-related documentation is available in:

```text
07-Deployment/
```

This section contains:

* Deployment Guide
* Environment Configuration
* Deployment Architecture

---

# 📊 Presentation

Project presentation materials are organized in:

```text
08-Presentation/
```

This includes:

* Presentation materials
* Demo Script
* Presentation Screenshots

---

# 🔮 Future Scope

Potential future improvements include:

* Online Payment Integration
* Maps and Navigation
* Real-Time Notifications
* Advanced Court Search
* Recommendation Systems
* Mobile Application
* Analytics Dashboard
* Loyalty and Rewards

These features are not part of the initial V1 scope.

---

# 👨‍💻 Development Approach

Hagz is developed following a structured Software Engineering workflow:

```text
Requirements
     ↓
Analysis
     ↓
Design
     ↓
Implementation
     ↓
Testing
     ↓
Deployment
```

Each stage has its own documentation and artifacts inside the project repository.

---

# 📚 Documentation

The complete project documentation is organized into the following sections:

1. **Documentation** — Project background, scope, and team information.
2. **Requirements** — Functional and non-functional requirements.
3. **Analysis** — Actors, use cases, user stories, and business rules.
4. **Design** — Architecture, database, UML, API, and UI/UX.
5. **Implementation** — Frontend, backend, and administration system.
6. **Testing** — Test plans, test cases, results, and bug reports.
7. **Deployment** — Deployment and environment documentation.
8. **Presentation** — Presentation and demonstration materials.

---

## 📌 Project Status

**Current Stage:** Software Engineering Documentation & Design

The project is being developed incrementally, starting with requirements, analysis, and system design before implementation.

---

## 🏷️ Hagz

**Sports Court Booking & Management Platform**

> **Less Searching. More Playing.**
