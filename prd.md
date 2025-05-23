# 🏠 HomeWarr: Smart Warranty Manager for Homeowners

## 🧭 Overview

**Goal**:  
Create a mobile-first app that helps new homeowners digitally store, track, and manage warranties for household appliances, electronics, and systems. Users receive reminders before warranties expire, upload proof of purchase, and initiate service requests via manufacturer contact links.

---

## 👤 Target Users

- **New Homeowners**: Managing multiple new appliances with overlapping warranty periods.
- **Existing Homeowners**: Looking to digitally manage their warranty paperwork.
- **Property Managers**: Overseeing warranties for multi-unit housing or rentals.

---

## 🔑 Key Features

### 1. 📥 Warranty Upload & Capture
- Manual entry or OCR-based auto-fill via receipt upload.
- Email forwarding (e.g., warranty@homewarr.app) to auto-ingest digital receipts.
- Manufacturer database lookup to auto-populate warranty durations.
- Categorize by room or system (kitchen, HVAC, etc.)

### 2. 🗃 Warranty Vault (Dashboard)
- List view of all active/inactive warranties.
- Filters: expiration date, room, brand.
- Status indicators: Active, Expiring Soon, Expired.

### 3. 🔔 Smart Notifications
- Push/email reminders 30/15/1 day before expiration.
- Optional service contract renewal suggestions.

### 4. 📞 One-Tap Manufacturer Support
- Contact links to manufacturer service portals.
- Generate claim-ready PDF with proof of purchase and warranty terms.

### 5. 🏠 Home Profile
- Allow multiple home profiles (for investors or property managers).
- Home-specific tagging of warranties (i.e., “2nd Floor Condo”).

---

## 🧮 Functional Requirements

| ID | Feature | Description |
|----|---------|-------------|
| FR1 | Register & login | OAuth or password login |
| FR2 | Add warranty | Manual form, OCR scan, or import |
| FR3 | Auto tag by category | Kitchen, HVAC, etc. |
| FR4 | Notify on expiry | Notification scheduler |
| FR5 | View warranties | Searchable/filterable dashboard |
| FR6 | Export warranty packet | Download/share grouped PDF bundle |
| FR7 | Claim support | Manufacturer contact integrations |
| FR8 | Multi-property support | Switch between homes |

---

## 💾 Non-Functional Requirements

- **Availability**: 99.9% uptime SLA for warranty access
- **Security**: Encryption at rest (AES-256) and in transit (TLS)
- **Compliance**: GDPR & CCPA compliant
- **Scalability**: Able to handle up to 1M users with cloud storage (AWS S3)
- **Platforms**: iOS, Android, Web dashboard

---

## 🗂 Data Model (Simplified ERD)

### User
- `user_id` (PK)
- `name`
- `email`
- `password_hash`

### Home
- `home_id` (PK)
- `user_id` (FK)
- `address`
- `nickname`

### Warranty
- `warranty_id` (PK)
- `home_id` (FK)
- `product_name`
- `manufacturer`
- `category`
- `purchase_date`
- `warranty_length`
- `expiration_date` (calculated)
- `proof_of_purchase_url`
- `status` (active, expiring, expired)

### Notification
- `notif_id` (PK)
- `user_id` (FK)
- `warranty_id` (FK)
- `notif_type` (push/email)
- `scheduled_date`

---

## 🛠 Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Flutter (mobile) / React (web) |
| Backend | Node.js + Express |
| Database | PostgreSQL |
| OCR | Google Cloud Vision |
| Storage | AWS S3 |
| Notifications | Firebase Cloud Messaging + SendGrid |

---

## 🗓 Suggested Timeline (MVP)

| Phase | Milestone | Duration |
|-------|-----------|----------|
| Discovery | Interviews & UI mockups | 2 weeks |
| Build Sprint 1 | Auth, Home Profile, Manual Entry | 2 weeks |
| Build Sprint 2 | OCR, Dashboard, Notifications | 3 weeks |
| Build Sprint 3 | Export/Claim Flow + QA | 2 weeks |
| Launch | Beta testing + release | 1 week |

---

## 📌 KPIs (Key Performance Indicators)

- % of users with >3 warranties uploaded
- Retention rate after 90 days
- % of warranties renewed using reminder
- NPS from new homeowner segment
