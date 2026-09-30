# Hagz — Use Case Descriptions

## 1. Introduction

A use case describes an interaction between an actor and the Hagz system to achieve a specific goal.

---

# UC-001 — Register Account

**Actor:** Player / Court Owner

**Goal:** Create a new account.

### Preconditions

* The user does not already have an account using the provided unique credentials.

### Main Flow

1. The user opens the registration page.
2. The user enters the required information.
3. The system validates the submitted data.
4. The system checks whether the account already exists.
5. The system creates the account.
6. The system confirms successful registration.

### Alternative Flows

* If the submitted data is invalid, the system displays validation errors.
* If the account already exists, the system informs the user.

### Postconditions

A new user account exists in the system.

---

# UC-002 — Login

**Actor:** Player / Court Owner / Administrator

**Goal:** Authenticate into the system.

### Preconditions

* The user has an existing account.

### Main Flow

1. The user enters authentication credentials.
2. The system validates the credentials.
3. The system authenticates the user.
4. The system identifies the user's role.
5. The system grants access according to the user's permissions.

### Alternative Flows

* Invalid credentials → authentication fails.
* Inactive account → access is denied.

### Postconditions

The user is authenticated.

---

# UC-003 — Search Courts

**Actor:** Player

**Goal:** Find suitable sports courts.

### Main Flow

1. The player opens the court search page.
2. The player enters search criteria.
3. The system processes the search.
4. The system retrieves matching approved courts.
5. The system displays the results.

### Postconditions

Matching courts are displayed.

---

# UC-004 — Filter Courts

**Actor:** Player

**Goal:** Narrow court search results.

### Main Flow

1. The player selects an area or price criteria.
2. The system validates the filter.
3. The system applies the selected criteria.
4. The system displays matching courts.

### Postconditions

The player receives filtered results.

---

# UC-005 — View Court Details

**Actor:** Player

**Goal:** View detailed information about a court.

### Main Flow

1. The player selects a court.
2. The system retrieves the court information.
3. The system displays the court details.
4. The system displays available booking slots.

### Postconditions

The player can review the selected court before booking.

---

# UC-006 — View Available Time Slots

**Actor:** Player

**Goal:** Check which time slots are available.

### Main Flow

1. The player selects a court.
2. The system retrieves the court's configured time slots.
3. The system checks booking status for the selected date.
4. The system identifies available slots.
5. The system displays available slots.

### Postconditions

The player can select an available slot.

---

# UC-007 — Create Booking

**Actor:** Player

**Goal:** Book an available court slot.

### Preconditions

* Player is authenticated.
* Court is approved.
* Selected time slot is available.

### Main Flow

1. The player selects a court.
2. The player selects an available time slot.
3. The player submits the booking.
4. The system validates the request.
5. The system verifies that the slot is still available.
6. The system creates the booking.
7. The system assigns the initial booking status.
8. The system confirms the booking request.

### Alternative Flows

* Slot is no longer available → booking is rejected.
* Invalid request → system returns a validation error.

### Postconditions

A booking exists for the selected player, court, date, and time slot.

---

# UC-008 — Cancel Booking

**Actor:** Player

**Goal:** Cancel an eligible booking.

### Preconditions

* Player is authenticated.
* Booking belongs to the player.
* Booking is eligible for cancellation.

### Main Flow

1. Player opens their bookings.
2. Player selects a booking.
3. Player requests cancellation.
4. System validates ownership and booking state.
5. System changes the booking status to cancelled.
6. System confirms cancellation.

### Postconditions

The booking is no longer considered active.

---

# UC-009 — View Bookings

**Actor:** Player

**Goal:** View personal bookings.

### Main Flow

1. Player opens the bookings section.
2. System identifies the authenticated player.
3. System retrieves the player's bookings.
4. System displays booking information.

### Postconditions

The player can view their booking history and current bookings.

---

# UC-010 — Add Court

**Actor:** Court Owner

**Goal:** Submit a sports court to the platform.

### Main Flow

1. Court Owner opens the add court page.
2. Court Owner enters court information.
3. Court Owner uploads required photos.
4. Court Owner submits the court.
5. System validates the information.
6. System creates the court.
7. System assigns the initial approval status.
8. Court becomes available for administrative review.

### Postconditions

A new court exists in a pending state.

---

# UC-011 — Manage Court

**Actor:** Court Owner

**Goal:** Update their court information.

### Main Flow

1. Court Owner selects one of their courts.
2. System verifies ownership.
3. Court Owner updates the information.
4. System validates the changes.
5. System saves the updated information.

### Postconditions

The court information is updated.

---

# UC-012 — Define Availability

**Actor:** Court Owner

**Goal:** Configure available booking time slots.

### Main Flow

1. Court Owner selects a court.
2. System verifies ownership.
3. Court Owner defines available times.
4. System validates the configuration.
5. System saves the availability.

### Postconditions

The court has configured availability.

---

# UC-013 — View Booking Requests

**Actor:** Court Owner

**Goal:** View incoming booking requests.

### Main Flow

1. Court Owner opens booking requests.
2. System identifies the owner's courts.
3. System retrieves related booking requests.
4. System displays the requests.

---

# UC-014 — Accept Booking

**Actor:** Court Owner

**Goal:** Accept an eligible booking request.

### Preconditions

* Booking belongs to one of the owner's courts.
* Booking is in an acceptable state.
* Selected slot is still valid.

### Main Flow

1. Court Owner opens booking requests.
2. Court Owner selects a booking.
3. System verifies ownership.
4. Court Owner accepts the booking.
5. System updates the booking status.
6. System confirms the operation.

### Postconditions

The booking becomes accepted.

---

# UC-015 — Reject Booking

**Actor:** Court Owner

**Goal:** Reject an eligible booking request.

### Main Flow

1. Court Owner opens booking requests.
2. Court Owner selects a booking.
3. System verifies ownership.
4. Court Owner rejects the booking.
5. System updates the booking status.
6. System confirms the operation.

### Postconditions

The booking becomes rejected.

---

# UC-016 — Review Court

**Actor:** Administrator

**Goal:** Review a submitted court.

### Main Flow

1. Administrator opens pending courts.
2. System retrieves submitted courts.
3. Administrator selects a court.
4. System displays the submitted information.
5. Administrator reviews the information.

### Postconditions

The administrator can proceed with approval or rejection.

---

# UC-017 — Approve Court

**Actor:** Administrator

**Goal:** Approve a submitted court.

### Preconditions

* Administrator is authenticated.
* Court is pending review.

### Main Flow

1. Administrator selects a pending court.
2. Administrator chooses approve.
3. System updates the court status.
4. System confirms approval.

### Postconditions

The court becomes approved and can be listed according to platform rules.

---

# UC-018 — Reject Court

**Actor:** Administrator

**Goal:** Reject a submitted court.

### Main Flow

1. Administrator selects a pending court.
2. Administrator chooses reject.
3. System updates the court status.
4. System confirms rejection.

### Postconditions

The court is not publicly listed as an approved court.

---

# UC-019 — Manage Users

**Actor:** Administrator

**Goal:** Manage platform users.

### Main Flow

1. Administrator opens user management.
2. System retrieves users.
3. Administrator selects a user.
4. System displays user information.
5. Administrator performs an authorized management operation.
6. System saves the change.

### Postconditions

The selected user record is updated when applicable.
