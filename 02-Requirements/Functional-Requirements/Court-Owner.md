# Hagz — Court Owner Functional Requirements

## Actor

**Court Owner**

A court owner manages sports courts available through the Hagz platform.

---

## FR-OWN-001 — Court Owner Registration

The system shall allow a new court owner to create an account.

---

## FR-OWN-002 — Court Owner Login

The system shall allow registered court owners to authenticate securely.

---

## FR-OWN-003 — Add Court

The system shall allow a court owner to submit a new sports court.

The court information may include:

* Court name.
* Address.
* Area.
* Price.
* Photos.

---

## FR-OWN-004 — Manage Court Information

The system shall allow a court owner to update information associated with their court.

---

## FR-OWN-005 — Upload Court Photos

The system shall allow a court owner to upload photos associated with their court.

---

## FR-OWN-006 — Set Court Price

The system shall allow a court owner to define the booking price of their court.

---

## FR-OWN-007 — Define Available Time Slots

The system shall allow a court owner to define the time slots during which their court can be booked.

---

## FR-OWN-008 — View Booking Requests

The system shall allow a court owner to view booking requests submitted for their courts.

---

## FR-OWN-009 — Accept Booking

The system shall allow a court owner to accept an eligible booking request.

---

## FR-OWN-010 — Reject Booking

The system shall allow a court owner to reject an eligible booking request.

---

## FR-OWN-011 — Manage Court Availability

The system shall allow a court owner to manage the availability of their court.

---

## Business Rules

1. A court owner can only manage courts associated with their account.
2. A court cannot be publicly listed before administrative approval.
3. A court owner cannot accept a booking for an unavailable slot.
4. A rejected booking cannot remain in an accepted state.
5. Court information must contain the required fields before submission.
