# Hagz — Actors Analysis

## 1. Overview

The Hagz system has three primary actors.

Each actor interacts with the system according to a specific role and set of permissions.

---

# 2. Player

## Description

A Player is a registered user who uses Hagz to discover sports courts and create bookings.

## Main Responsibilities

The Player can:

* Register an account.
* Log in.
* Search for courts.
* Filter courts by area.
* Filter courts by price.
* View court details.
* View available time slots.
* Create bookings.
* Cancel eligible bookings.
* View personal bookings.

## Main Goals

The Player's main goal is to find a suitable sports court and book an available time slot.

---

# 3. Court Owner

## Description

A Court Owner is a user who owns or manages sports courts available on Hagz.

## Main Responsibilities

The Court Owner can:

* Register an account.
* Log in.
* Add courts.
* Manage court information.
* Upload court photos.
* Set court prices.
* Define available time slots.
* View booking requests.
* Accept booking requests.
* Reject booking requests.
* Manage court availability.

## Main Goals

The Court Owner's main goal is to manage their courts and handle incoming booking requests.

---

# 4. Administrator

## Description

An Administrator is a privileged system user responsible for managing the platform.

## Main Responsibilities

The Administrator can:

* Log in.
* View submitted courts.
* Review court information.
* Approve courts.
* Reject courts.
* Manage users.

## Main Goals

The Administrator's main goal is to maintain platform integrity and control administrative operations.

---

# 5. Actor Permissions

| Actor         | Authentication | Court Search | Booking | Court Management | Court Approval | User Management |
| ------------- | -------------- | ------------ | ------- | ---------------- | -------------- | --------------- |
| Player        | Yes            | Yes          | Yes     | No               | No             | No              |
| Court Owner   | Yes            | No*          | No*     | Yes              | No             | No              |
| Administrator | Yes            | No           | No      | Limited          | Yes            | Yes             |

> * Court Owner capabilities are focused on managing their own courts and bookings rather than acting as a Player.

---

# 6. Access Control Principle

The system follows Role-Based Access Control (RBAC).

Each authenticated user is assigned a role, and the system determines which operations that user is authorized to perform based on that role.

A user must not be able to perform operations belonging to another role without the required authorization.
