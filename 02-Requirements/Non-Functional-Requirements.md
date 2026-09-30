# Hagz — Non-Functional Requirements

## NFR-SEC — Security

### NFR-SEC-001

The system shall securely store user passwords using an appropriate password hashing mechanism.

### NFR-SEC-002

The system shall authenticate users before allowing access to protected resources.

### NFR-SEC-003

The system shall enforce role-based authorization.

### NFR-SEC-004

Users shall not be allowed to access resources belonging to other unauthorized users.

### NFR-SEC-005

The system shall validate user input before processing requests.

---

# NFR-PERF — Performance

### NFR-PERF-001

The system should provide acceptable response times under normal expected usage.

### NFR-PERF-002

Database queries should be designed to avoid unnecessary processing.

### NFR-PERF-003

The system should avoid unnecessary network requests.

---

# NFR-USAB — Usability

### NFR-USAB-001

The system interface should be simple and understandable.

### NFR-USAB-002

Common operations should require a reasonable number of steps.

### NFR-USAB-003

Validation and error messages should be clear and understandable.

---

# NFR-REL — Reliability

### NFR-REL-001

The system shall prevent invalid bookings.

### NFR-REL-002

The system shall maintain consistent booking states.

### NFR-REL-003

The system shall handle invalid requests without causing system failure.

---

# NFR-MAIN — Maintainability

### NFR-MAIN-001

The system shall follow a modular software architecture.

### NFR-MAIN-002

System components shall have clearly defined responsibilities.

### NFR-MAIN-003

The source code shall follow consistent naming and organization conventions.

---

# NFR-SCAL — Scalability

### NFR-SCAL-001

The system architecture should support the addition of new features without requiring a complete redesign.

### NFR-SCAL-002

The system should support the future addition of more sports, courts, users, and booking operations.

---

# NFR-AVAIL — Availability

### NFR-AVAIL-001

The system should be available to authenticated users whenever the application services are operational.

### NFR-AVAIL-002

The system should handle temporary service failures gracefully.

---

# NFR-COMP — Compatibility

### NFR-COMP-001

The web application should support modern web browsers.

### NFR-COMP-002

The user interface should be usable across common desktop and mobile screen sizes.
