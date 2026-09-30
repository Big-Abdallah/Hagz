# Hagz — API Documentation

## 1. API Overview

Hagz exposes a RESTful API used by the web frontend to communicate with the backend application.

## 2. Base URL

```text
/api/v1
```

The production base URL will be defined during deployment.

---

# 3. Authentication

## POST `/auth/register`

Creates a new user account.

### Request

```json
{
  "name": "User Name",
  "email": "user@example.com",
  "password": "password"
}
```

### Response

Returns the created user information according to the final API contract.

---

## POST `/auth/login`

Authenticates a user.

### Request

```json
{
  "email": "user@example.com",
  "password": "password"
}
```

---

# 4. Courts

## GET `/courts`

Returns approved courts.

### Query Parameters

```text
area
minPrice
maxPrice
```

---

## GET `/courts/:id`

Returns detailed information about a specific court.

---

## POST `/courts`

Creates a new court.

**Required Role:** Court Owner

---

## PATCH `/courts/:id`

Updates court information.

**Required Role:** Court Owner

---

# 5. Availability

## GET `/courts/:id/availability`

Returns available time slots for a court.

---

## POST `/courts/:id/availability`

Creates or configures availability.

**Required Role:** Court Owner

---

# 6. Bookings

## POST `/bookings`

Creates a booking request.

**Required Role:** Player

---

## GET `/bookings/me`

Returns bookings belonging to the authenticated player.

**Required Role:** Player

---

## PATCH `/bookings/:id/cancel`

Cancels an eligible booking.

**Required Role:** Player

---

## GET `/owner/bookings`

Returns booking requests for the authenticated court owner.

**Required Role:** Court Owner

---

## PATCH `/owner/bookings/:id/accept`

Accepts a booking request.

**Required Role:** Court Owner

---

## PATCH `/owner/bookings/:id/reject`

Rejects a booking request.

**Required Role:** Court Owner

---

# 7. Administration

## GET `/admin/courts/pending`

Returns courts waiting for administrative review.

**Required Role:** Administrator

---

## PATCH `/admin/courts/:id/approve`

Approves a submitted court.

**Required Role:** Administrator

---

## PATCH `/admin/courts/:id/reject`

Rejects a submitted court.

**Required Role:** Administrator

---

## GET `/admin/users`

Returns platform users.

**Required Role:** Administrator

---

# 8. HTTP Status Codes

The API should use standard HTTP status codes.

| Status | Meaning               |
| ------ | --------------------- |
| 200    | Successful request    |
| 201    | Resource created      |
| 400    | Invalid request       |
| 401    | Unauthenticated       |
| 403    | Unauthorized          |
| 404    | Resource not found    |
| 409    | Conflict              |
| 422    | Validation error      |
| 500    | Internal server error |

---

# 9. API Design Principles

The API should follow these principles:

* RESTful resource naming.
* Consistent HTTP methods.
* Proper HTTP status codes.
* Request validation.
* Authentication for protected endpoints.
* Role-based authorization.
* Consistent response structure.
* Clear error messages.

The API contract may be refined during implementation.
