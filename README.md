# CampusBite Tanzania — MVP

This folder contains a mobile-first working MVP/prototype.

## Demo accounts
Student:
- College ID: COL-000123
- Student number: DEMO-001
- Password: 1234

Admin: tap "Admin demo"
Vendor: tap "Vendor demo"

## What works in the demo
- Multi-college identification number concept
- Admin adds students
- Student registration requires a pre-added student number
- Admin adds/removes food and controls price/time
- Student browses menu and adds to cart
- Checkout and demo payment flow
- Digital receipt with unique order/receipt IDs
- 4-hour receipt expiry
- One-time receipt redemption
- Admin order/student/food dashboards
- Vendor order/redeem flow
- Local browser persistence

## Production integrations still required
This MVP deliberately does not fake external services. Before public launch, connect:
1. A real backend/database (e.g. Supabase/PostgreSQL or your chosen backend).
2. Real authentication and server-side authorization.
3. A Tanzania-supported payment gateway and webhook verification.
4. Official WhatsApp Business/API messaging for invitation and receipt delivery.
5. Secure server-generated signed QR tokens.
6. HTTPS, backups, monitoring, audit logging and production secrets.

`schema.sql` provides a starting relational schema.

## Run
Open `index.html` in a browser for the demo. For production, serve through HTTPS and replace the demo/localStorage logic with the backend APIs.


## New in v2
- Admin can set a college/university ID, college name, and upload a college DP/logo.
- The selected college logo is stored locally for this demo and shown on the login and app header.
- Different College IDs can have different logos.
- In production, logo files should be stored in secure cloud storage and each admin must be server-authorized to manage only their own college.
