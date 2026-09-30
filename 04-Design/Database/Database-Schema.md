# Hagz — Database Schema

## 1. Overview

The Hagz database stores information required to manage users, sports courts, court availability, and bookings.

The database is designed to maintain data integrity and support the core booking workflow.

---

# 2. Main Entities

The initial database model contains the following main entities:

* User
* Court
* Court Image
* Availability
* Booking

---

# 3. User

The User entity represents all registered users of the system.

A user has one role that determines their permissions.

### Main Attributes

| Attribute | Description                   |
| --------- | ----------------------------- |
| id        | Unique user identifier        |
| name      | User's name                   |
| email     | User's unique email           |
| password  | Securely hashed password      |
| role      | Player, Court Owner, or Admin |
| status    | Account status                |
| createdAt | Account creation date         |
| updatedAt | Last update date              |

### Role Values

```text
PLAYER
COURT_OWNER
ADMIN
```

---

# 4. Court

The Court entity represents a sports court submitted by a court owner.

### Main Attributes

| Attribute | Description                  |
| --------- | ---------------------------- |
| id        | Unique court identifier      |
| ownerId   | Reference to the court owner |
| name      | Court name                   |
| address   | Court address                |
| area      | Court area                   |
| price     | Booking price                |
| status    | Approval status              |
| createdAt | Creation date                |
| updatedAt | Last update date             |

### Court Status

```text
PENDING
APPROVED
REJECTED
```

---

# 5. Court Image

The Court Image entity stores references to images belonging to a court.

### Main Attributes

| Attribute | Description             |
| --------- | ----------------------- |
| id        | Unique image identifier |
| courtId   | Reference to the court  |
| imageUrl  | Stored image location   |
| createdAt | Upload date             |

A court may have multiple images.

---

# 6. Availability

The Availability entity represents time periods during which a court can be booked.

### Main Attributes

| Attribute | Description                    |
| --------- | ------------------------------ |
| id        | Unique availability identifier |
| courtId   | Reference to the court         |
| day       | Day or applicable date         |
| startTime | Start of available period      |
| endTime   | End of available period        |
| createdAt | Creation date                  |
| updatedAt | Last update date               |

The exact scheduling model may be refined during implementation according to the final booking requirements.

---

# 7. Booking

The Booking entity represents a player's reservation request for a court.

### Main Attributes

| Attribute | Description               |
| --------- | ------------------------- |
| id        | Unique booking identifier |
| playerId  | Reference to the player   |
| courtId   | Reference to the court    |
| date      | Booking date              |
| startTime | Booking start time        |
| endTime   | Booking end time          |
| status    | Booking status            |
| createdAt | Booking creation date     |
| updatedAt | Last update date          |

### Booking Status

```text
PENDING
ACCEPTED
REJECTED
CANCELLED
```

---

# 8. Relationships

## User → Court

One Court Owner can manage multiple courts.

```text
User (Court Owner)
        │
        │ 1 : N
        ▼
      Court
```

## Court → Court Image

A court can have multiple images.

```text
Court
  │
  │ 1 : N
  ▼
Court Image
```

## Court → Availability

A court can have multiple availability configurations.

```text
Court
  │
  │ 1 : N
  ▼
Availability
```

## Player → Booking

A player can create multiple bookings.

```text
Player
  │
  │ 1 : N
  ▼
Booking
```

## Court → Booking

A court can have multiple bookings over time.

```text
Court
  │
  │ 1 : N
  ▼
Booking
```

---

# 9. Integrity Requirements

The database should enforce the following principles:

* User email must be unique.
* Every court must belong to a valid court owner.
* Every booking must reference a valid player.
* Every booking must reference a valid court.
* Every court image must reference a valid court.
* Every availability record must reference a valid court.
* Conflicting active bookings for the same court and time slot must be prevented.

---

# 10. Design Note

The final schema may be refined during implementation after the exact booking and scheduling behavior is finalized.
