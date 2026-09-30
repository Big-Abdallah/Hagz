# Hagz — Admin Functional Requirements

## Actor

**Administrator**

The administrator manages the platform and controls administrative operations.

---

## FR-ADM-001 — Admin Login

The system shall allow an authorized administrator to authenticate securely.

---

## FR-ADM-002 — View Submitted Courts

The system shall allow the administrator to view courts submitted by court owners.

---

## FR-ADM-003 — Review Court

The system shall allow the administrator to review submitted court information before approval.

The administrator may review:

* Court name.
* Address.
* Area.
* Price.
* Photos.
* Court owner information.

---

## FR-ADM-004 — Approve Court

The system shall allow the administrator to approve a submitted court.

### Expected Result

The court becomes eligible to appear to players according to the system's listing rules.

---

## FR-ADM-005 — Reject Court

The system shall allow the administrator to reject a submitted court.

### Expected Result

The court does not become publicly available.

---

## FR-ADM-006 — Manage Users

The system shall allow administrators to manage platform users.

User management may include:

* Viewing users.
* Reviewing user information.
* Managing account status.

---

## Business Rules

1. Administrative operations require administrator authorization.
2. Only administrators can approve or reject submitted courts.
3. A rejected court cannot be listed as approved.
4. Regular users cannot access administrative operations.
