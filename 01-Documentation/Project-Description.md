# Hagz — Project Description

## 1. Introduction

Finding and booking sports courts can often involve manually contacting court owners, asking about availability, and waiting for confirmation.

Hagz aims to provide a centralized digital solution for this process.

The platform allows players to search for sports courts and book available time slots, while court owners can manage their courts and handle booking requests through the same system.

## 2. Problem Statement

Players may face several difficulties when trying to book sports courts:

* Finding suitable courts in a specific area.
* Comparing court prices.
* Knowing which time slots are available.
* Contacting court owners manually.
* Keeping track of existing bookings.

Court owners may also face difficulties managing:

* Court information.
* Available time slots.
* Incoming booking requests.
* Booking status.

Hagz addresses these problems by providing a centralized platform for managing the complete court booking process.

## 3. Proposed Solution

Hagz provides a web-based platform where players can search for courts based on relevant criteria, view available time slots, and submit booking requests.

Court owners can manage their courts and respond to booking requests.

Administrators provide platform-level management by reviewing newly added courts and managing users.

## 4. System Concept

The system follows a role-based model.

Each user interacts with the platform according to their role:

```text
Player
   │
   ├── Search Courts
   ├── View Availability
   ├── Book Court
   └── Manage Bookings

Court Owner
   │
   ├── Add Court
   ├── Manage Availability
   ├── Receive Bookings
   └── Accept / Reject Bookings

Admin
   │
   ├── Review Courts
   ├── Approve / Reject Courts
   └── Manage Users
```

## 5. Project Vision

Hagz aims to provide a simple and reliable digital experience for sports court booking while maintaining a clear separation between players, court owners, and administrators.

The system is designed to be scalable so that additional sports, features, and services can be introduced in future versions.
