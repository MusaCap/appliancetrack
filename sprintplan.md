# 🚀 Sprint Plan: HomeWarr App Development (Windsurf)

## ⏱ Sprint Duration
- 2 Weeks per sprint
- 6 Total Sprints for MVP completion

---

## 🟢 Sprint 1: Foundation & Authentication

**Goals:**
- Establish core backend and frontend setup
- Implement user registration, login, and home profile creation

**Tasks:**
- ✅ US-001: User Registration (email + Google OAuth)
- ✅ US-002: Login & Session Handling
- ✅ US-003: Create Home Profile
- 🔧 Setup: Windsurf workspace, CI/CD pipeline, PostgreSQL schema
- 📦 Deliverables: Auth-ready app shell with working home profile flow

**Labels:** `auth`, `backend`, `frontend`, `data-model`, `MVP`

---

## 🟡 Sprint 2: Warranty Entry & Dashboard View

**Goals:**
- Build UI/UX for manual warranty entry
- Create dashboard view for tracking warranties

**Tasks:**
- ✅ US-005: Add Warranty Manually
- ✅ US-007: View & Filter Warranties
- 🔧 Add relational logic between homes and warranties
- 🧪 Unit test forms and filter logic

**Labels:** `frontend`, `UX`, `backend`, `data-binding`

---

## 🔵 Sprint 3: Uploads, OCR & Smart Categorization

**Goals:**
- Enable document upload and OCR ingestion
- Categorize warranties automatically

**Tasks:**
- ✅ US-006: Upload Warranty via Receipt Scan
- ✅ US-008: Attach Supporting Documents
- 🔧 Integrate Google Cloud Vision OCR API
- 🧪 Manual review interface for scanned data

**Labels:** `OCR`, `AI`, `cloud-storage`, `frontend`, `integration`

---

## 🟣 Sprint 4: Notifications & Alerts

**Goals:**
- Implement warranty expiration reminders
- Notification preference UI

**Tasks:**
- ✅ US-009: Expiration Alerts
- ✅ US-010: Resend or Snooze Notifications
- 🔧 Schedule background jobs with CRON or Firebase functions
- 🧪 Simulate date-based expiration and alerts

**Labels:** `notifications`, `backend`, `UX`, `reminders`

---

## 🟠 Sprint 5: Support, Export & Claims

**Goals:**
- Help users contact manufacturers and export data
- Finalize dashboard functionality

**Tasks:**
- ✅ US-011: Manufacturer Support Link Suggestion
- ✅ US-012: Export Warranty Packet (PDF generator)
- 🔧 Add product support info to product model
- 🧪 Validate multi-document exports and download logic

**Labels:** `integration`, `PDF`, `frontend`, `support-tools`

---

## ⚫ Sprint 6: QA, Admin Panel & Launch Prep

**Goals:**
- Stabilize MVP with testing, admin tools, and analytics
- Prep beta deployment

**Tasks:**
- ✅ US-013: Profile Settings UI
- ✅ US-014: Admin Dashboard
- 🧪 Write and run E2E tests across flows
- 🧪 Load test warranty uploads
- 🚀 Deploy beta version on TestFlight / Firebase Hosting

**Labels:** `admin`, `QA`, `testing`, `deployment`, `security`

---

## 🧠 Optional Future Sprints (Post-MVP)

| Feature | Goal |
|--------|------|
| AI auto-categorization | Predict category based on product name |
| API integrations | Connect to top manufacturer APIs for live status |
| Revenue module | Track service contracts and upsell offers |

---

## 📌 Notes for Windsurf DevOps

- Use **agent tasks** to define acceptance test specs for each US.
- Add **chat-triggered branches** like `/sprint-3-test-notification` for live debugging.
- Enable **auto-documentation agents** to convert code → API docs every commit.

