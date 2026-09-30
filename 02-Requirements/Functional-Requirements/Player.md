# Hagz — Player Functional Requirements

## Actor

**Player**

A player is a registered user who uses Hagz to discover and book sports courts.

---

## FR-PLY-001 — Player Registration

The system shall allow a new player to create an account by providing the required registration information.

### Preconditions

* The player does not already have an account with the provided unique identifier.

### Expected Result

A player account is created successfully.

---

## FR-PLY-002 — Player Login

The system shall allow a registered player to log in using valid authentication credentials.

### Preconditions

* The player has an existing account.

### Expected Result

The player is authenticated and granted access to protected player features.

---

## FR-PLY-003 — Search Courts

The system shall allow players to search for sports courts.

### Expected Result

The system displays courts matching the search criteria.

---

## FR-PLY-004 — Filter Courts by Area

The system shall allow players to filter courts according to their area or location.

### Expected Result

Only courts matching the selected area are displayed.

---

## FR-PLY-005 — Filter Courts by Price

The system shall allow players to filter courts according to price.

### Expected Result

Only courts matching the selected price criteria are displayed.

---

## FR-PLY-006 — View Court Details

The system shall allow players to view detailed information about a court.

Court information may include:

* Court name.
* Address.
* Price.
* Photos.
* Available time slots.

---

## FR-PLY-007 — View Available Time Slots

The system shall allow players to view available booking time slots for a court.

### Expected Result

The system displays time slots that can currently be booked.

---

## FR-PLY-008 — Create Booking

The system shall allow a player to book an available time slot.

### Preconditions

* The player is authenticated.
* The court is available.
* The selected time slot is available.

### Expected Result

A booking is created and associated with the player and court.

---

## FR-PLY-009 — Cancel Booking

The system shall allow a player to cancel an eligible booking.

### Preconditions

* The player owns the booking.
* The booking is eligible for cancellation.

### Expected Result

The booking status is updated to cancelled.

---

## FR-PLY-010 — View Bookings

The system shall allow players to view their bookings.

The booking information may include:

* Court.
* Date.
* Time slot.
* Price.
* Booking status.

---

## Business Rules

1. A player cannot book an unavailable time slot.
2. A player cannot access another player's private bookings.
3. A player cannot modify another player's booking.
4. A cancelled booking cannot remain active.
5. A booking must reference a valid court and time slot.
