# 🗂 Data Model for HomeWarr Warranty Management App

## 🧑‍💻 Entity Relationship Overview

The following are the main entities:
- **User**
- **Home**
- **Warranty**
- **Notification**
- **Product**
- **Document**

---

## 📘 User

| Field | Type | Description |
|-------|------|-------------|
| user_id | UUID (PK) | Unique identifier |
| name | VARCHAR | Full name |
| email | VARCHAR (unique) | Login email |
| password_hash | TEXT | Hashed password |
| created_at | TIMESTAMP | Account creation date |

---

## 🏠 Home

| Field | Type | Description |
|-------|------|-------------|
| home_id | UUID (PK) | Unique identifier |
| user_id | UUID (FK) | References User |
| address | TEXT | Street, City, State, Zip |
| nickname | VARCHAR | User-defined label (e.g., "Primary Residence") |
| created_at | TIMESTAMP | Timestamp of home entry |

---

## 🛠 Warranty

| Field | Type | Description |
|-------|------|-------------|
| warranty_id | UUID (PK) | Unique identifier |
| home_id | UUID (FK) | References Home |
| product_id | UUID (FK) | References Product |
| purchase_date | DATE | Date of purchase |
| warranty_length_months | INTEGER | Number of months covered |
| expiration_date | DATE | Auto-calculated or user-entered |
| status | ENUM | `active`, `expiring_soon`, `expired` |
| proof_of_purchase_url | TEXT | Link to uploaded document |
| created_at | TIMESTAMP | Date of entry |

---

## 🔧 Product

| Field | Type | Description |
|-------|------|-------------|
| product_id | UUID (PK) | Unique product identifier |
| name | VARCHAR | Product name (e.g., Whirlpool Dishwasher) |
| manufacturer | VARCHAR | Company name |
| category | ENUM | e.g., `kitchen`, `laundry`, `HVAC`, `plumbing` |
| model_number | VARCHAR | Optional model info |
| support_url | TEXT | Link to support site/contact |

---

## 📄 Document

| Field | Type | Description |
|-------|------|-------------|
| document_id | UUID (PK) | Unique identifier |
| warranty_id | UUID (FK) | References Warranty |
| file_url | TEXT | Cloud storage location |
| file_type | ENUM | `receipt`, `warranty_card`, `manual` |
| uploaded_at | TIMESTAMP | Upload timestamp |

---

## 🔔 Notification

| Field | Type | Description |
|-------|------|-------------|
| notif_id | UUID (PK) | Unique identifier |
| user_id | UUID (FK) | References User |
| warranty_id | UUID (FK) | References Warranty |
| notif_type | ENUM | `email`, `push` |
| scheduled_for | TIMESTAMP | When to send |
| sent | BOOLEAN | Sent status |

---

## 🔗 Relationships Summary

- A **User** can have many **Homes**
- A **Home** can have many **Warranties**
- A **Warranty** is linked to one **Product**
- A **Warranty** can have multiple **Documents**
- A **Notification** is tied to both **Warranty** and **User**

---

Would you like this exported as an ER diagram (image or diagram tool format), or saved as a downloadable `.md` file?
