# Hagz — UI Components

## 1. Buttons

### Primary Button

Used for the main action on a page.

Examples:

* Book Now.
* Add Court.
* Confirm.
* Approve.

Primary buttons should use the Hagz accent color where appropriate.

---

### Secondary Button

Used for supporting actions.

Examples:

* Cancel.
* Back.
* View Details.

---

### Destructive Button

Used for destructive actions.

Examples:

* Delete.
* Reject.
* Cancel Booking.

The destructive semantic color should be used carefully and consistently.

---

# 2. Court Card

A Court Card represents a sports court in search results.

It should contain:

* Court image.
* Court name.
* Area.
* Price.
* Availability indicator.
* Primary action.

Example structure:

```text
┌──────────────────────────────┐
│                              │
│          Court Image         │
│                              │
├──────────────────────────────┤
│ Court Name                   │
│ Area                         │
│                              │
│ EGP XXX / hour    View →     │
└──────────────────────────────┘
```

---

# 3. Booking Card

A Booking Card displays a player's booking.

Information:

* Court name.
* Date.
* Time.
* Price.
* Booking status.

---

# 4. Status Badge

Booking and court states should use clear status indicators.

Examples:

```text
Booking
├── Pending
├── Accepted
├── Rejected
└── Cancelled
```

```text
Court
├── Pending
├── Approved
└── Rejected
```

---

# 5. Form Components

Forms should use:

* Clear labels.
* Appropriate input types.
* Inline validation.
* Clear error messages.
* Consistent spacing.

---

# 6. Navigation

Navigation should remain simple.

Players should have quick access to:

* Home.
* Courts.
* Bookings.
* Profile.

Court Owners should have access to:

* Dashboard.
* Courts.
* Availability.
* Booking Requests.

Administrators should have access to:

* Dashboard.
* Pending Courts.
* Users.

---

# 7. Cards

Cards should have:

* Clear hierarchy.
* Subtle borders.
* Consistent radius.
* Controlled spacing.

Avoid excessive shadows or decorative effects.

---

# 8. Empty States

Empty states should explain:

1. What is currently missing.
2. Why it matters.
3. What the user can do next.

Dash may be used to make important empty states more friendly.

---

# 9. Feedback States

The system should clearly communicate:

* Loading.
* Success.
* Error.
* Empty.
* Disabled.
* Pending.

Feedback should be immediate and understandable.

