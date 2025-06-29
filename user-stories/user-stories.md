# 🧾 User Stories – Airbnb Clone Backend

This document outlines key user stories based on the use case diagram for the Airbnb Clone project. These stories describe how different users (Guests, Hosts, Admins) interact with the system.

---

## 👤 User Story 1 – Guest Registration and Authentication

**As a Guest**,  
I want to create an account and log in securely,  
so that I can access my dashboard and start booking properties.

**Acceptance Criteria:**
- Guest can sign up using email/password or OAuth (Google, Facebook).
- Passwords are securely hashed.
- JWT tokens are used for session management.
- Authentication errors (invalid credentials, expired token) are handled gracefully.

---

## 🧳 User Story 2 – Property Search and Filter

**As a Guest**,  
I want to search for properties based on location, price, amenities, and guest capacity,  
so that I can find listings that match my travel needs.

**Acceptance Criteria:**
- Backend supports filters by location, price range, number of guests, and amenities.
- Search results are paginated.
- Invalid or missing parameters are validated with appropriate error messages.

---

## 📅 User Story 3 – Booking a Property

**As a Guest**,  
I want to book a property for specific dates,  
so that I can reserve it and plan my stay.

**Acceptance Criteria:**
- Booking validates date availability.
- Double bookings are prevented through conflict checks.
- Booking is stored with status: `pending`, `confirmed`, `cancelled`, or `completed`.
- Notifications are triggered on successful booking.

---

## 🏠 User Story 4 – Host Listing Management

**As a Host**,  
I want to create, update, and delete property listings,  
so that I can manage the properties I rent out.

**Acceptance Criteria:**
- Hosts can create a new listing with title, description, images, price, location, and availability.
- Hosts can update existing listings.
- Hosts can delete their own listings.
- Input is validated (no empty fields, correct formats, etc.).

---

## 💳 User Story 5 – Payments and Host Payouts

**As a Guest**,  
I want to make a secure payment for a booking,  
so that I can confirm the reservation.

**And as a Host**,  
I want to receive payment after a booking is completed,  
so that I get compensated for hosting.

**Acceptance Criteria:**
- Guest payment is processed via a secure gateway (Stripe, PayPal).
- Payment status is tracked (`initiated`, `completed`, `failed`).
- Host payout is triggered after the booking end date.
- System supports multi-currency transactions.

