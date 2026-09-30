# Hagz — Software Requirements Specification (SRS)

## 1. Introduction

### 1.1 Purpose

This document defines the software requirements for the Hagz sports court booking platform.

It describes the system functionality, users, constraints, and quality requirements that will guide the analysis, design, implementation, and testing phases of the project.

### 1.2 Product Scope

Hagz is a web-based sports court booking platform that connects players with sports court owners.

The system allows players to search for courts, check availability, and create bookings.

Court owners can manage their courts, availability, and booking requests.

Administrators manage platform-level operations and approve newly submitted courts.

### 1.3 Intended Audience

This document is intended for:

* Project team members.
* Software engineers.
* UI/UX designers.
* Testers.
* Project supervisor.
* Future developers maintaining the system.

---

# 2. System Overview

Hagz consists of three primary actors:

1. Player
2. Court Owner
3. Administrator

Each actor has different permissions and responsibilities within the system.

---

# 3. Actors

## 3.1 Player

A player is a user who searches for sports courts and creates bookings.

## 3.2 Court Owner

A court owner is a user who owns or manages one or more sports courts listed on the platform.

## 3.3 Administrator

An administrator is responsible for managing the platform and reviewing submitted courts and users.

---

# 4. Functional Requirements

The functional requirements are divided according to the system actors.

## 4.1 Player Requirements

The system shall allow players to:

* Create an account.
* Log in securely.
* Search for available courts.
* Filter courts by area.
* Filter courts by price.
* View court details.
* View available time slots.
* Create a booking.
* Cancel a booking.
* View their bookings.

## 4.2 Court Owner Requirements

The system shall allow court owners to:

* Create an account.
* Log in securely.
* Add a new court.
* Provide court information.
* Upload court photos.
* Set court pricing.
* Define available time slots.
* View incoming booking requests.
* Accept booking requests.
* Reject booking requests.
* Manage court information.

## 4.3 Administrator Requirements

The system shall allow administrators to:

* Log in securely.
* View newly submitted courts.
* Review court information.
* Approve courts.
* Reject courts.
* Manage users.

---

# 5. Non-Functional Requirements

The system shall satisfy the following quality requirements:

## 5.1 Security

* User passwords shall not be stored in plain text.
* Authentication shall be required for protected operations.
* Role-based authorization shall restrict access to role-specific operations.
* Users shall only be allowed to access resources they are authorized to access.

## 5.2 Performance

* The system should provide responsive interactions under normal expected usage.
* Database queries should be optimized where necessary.
* The API should avoid unnecessary data processing and network requests.

## 5.3 Usability

* The interface should be simple and understandable.
* Users should be able to complete common tasks with minimal steps.
* Error messages should clearly explain the problem.

## 5.4 Reliability

* The system should prevent invalid bookings.
* The system should maintain consistent booking states.
* The system should handle invalid requests without crashing.

## 5.5 Maintainability

* The application should use a modular architecture.
* Components and services should have clear responsibilities.
* Code should follow consistent naming and organization conventions.

## 5.6 Scalability

The architecture should allow future features and additional users to be introduced without requiring a complete redesign of the system.

---

# 6. System Constraints

The first version of Hagz has the following constraints:

* The system will initially be implemented as a web application.
* Online payment is outside the initial scope.
* Advanced recommendation systems are outside the initial scope.
* Native mobile applications are outside the initial scope.
* The project will initially focus on the core court booking workflow.

---

# 7. Assumptions

The system assumes that:

* Users provide valid registration information.
* Court owners provide accurate court information.
* Administrators review submitted courts before they become publicly available.
* A booking can only be created for an available time slot.
* Users have access to an internet connection.

---

# 8. Future Enhancements

Potential future features include:

* Online payments.
* Notifications.
* Reviews and ratings.
* Favorite courts.
* Map integration.
* Advanced search.
* Mobile applications.
* Promotional offers.
* Analytics.
