# Hagz — Business Rules

## 1. Authentication Rules

### BR-AUTH-001

A user must be authenticated before accessing protected operations.

### BR-AUTH-002

A user can only access operations permitted by their assigned role.

### BR-AUTH-003

User credentials must be handled securely.

---

# 2. Player Rules

### BR-PLY-001

A player can only view and manage their own bookings.

### BR-PLY-002

A player cannot create a booking for an unavailable time slot.

### BR-PLY-003

A player cannot create a booking for a court that has not been approved.

### BR-PLY-004

A player can only cancel bookings that belong to them.

### BR-PLY-005

A cancelled booking cannot remain in an active booking state.

---

# 3. Court Rules

### BR-COURT-001

A court must belong to a registered court owner.

### BR-COURT-002

A newly submitted court starts in a pending approval state.

### BR-COURT-003

A court must be approved before it can be publicly listed.

### BR-COURT-004

Only the court owner can manage their court.

### BR-COURT-005

Required court information must be provided before submission.

---

# 4. Availability Rules

### BR-AVAIL-001

A booking can only be created for an available time slot.

### BR-AVAIL-002

A time slot cannot be simultaneously allocated to conflicting active bookings.

### BR-AVAIL-003

Court availability is controlled by the court owner.

---

# 5. Booking Rules

### BR-BOOK-001

Every booking must reference one player.

### BR-BOOK-002

Every booking must reference one court.

### BR-BOOK-003

Every booking must reference a valid date and time slot.

### BR-BOOK-004

A booking must have a defined status.

### BR-BOOK-005

Only authorized users can modify booking status.

### BR-BOOK-006

A booking request must be validated before being created.

---

# 6. Court Owner Rules

### BR-OWN-001

A court owner can manage only courts associated with their account.

### BR-OWN-002

A court owner can only manage booking requests belonging to their courts.

### BR-OWN-003

A court owner cannot approve their own court.

---

# 7. Administrator Rules

### BR-ADM-001

Only administrators can approve or reject courts.

### BR-ADM-002

Only administrators can perform administrative user-management operations.

### BR-ADM-003

Administrative operations must require administrator authorization.

---

# 8. Data Integrity Rules

### BR-DATA-001

Every booking must reference valid existing entities.

### BR-DATA-002

Deleting or disabling an entity must not create invalid references.

### BR-DATA-003

The system must prevent duplicate or conflicting active bookings for the same court and time slot.
