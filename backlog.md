# 📋 HomeWarr Product Warranty App – Windsurf Backlog

## 🧱 Epic 1: User Authentication & Onboarding

### US-001: User Registration
**As** a new user  
**I want** to register using my email or Google account  
**So that** I can securely access my warranty dashboard

**Acceptance Criteria:**
- User can register via email/password
- OAuth with Google enabled
- Error shown for duplicate email

Labels: `auth`, `MVP`, `frontend`, `backend`

---

### US-002: Login & Session Management
**As** a returning user  
**I want** to log in and stay authenticated  
**So that** I don’t need to log in repeatedly

**Acceptance Criteria:**
- JWT or session token persists for 7 days
- Logout functionality clears session
- "Remember me" checkbox for persistent login

Labels: `auth`, `security`, `frontend`, `backend`

---

## 🧱 Epic 2: Home Profiles Management

### US-003: Create Home Profile
**As** a user  
**I want** to add multiple home profiles  
**So that** I can manage warranties across properties

**Acceptance Criteria:**
- Form includes nickname, address
- Homes are switchable via a dropdown
- Linked to user ID

Labels: `MVP`, `data-model`, `frontend`, `backend`

---

### US-004: Edit/Delete Home Profile
**As** a user  
**I want** to edit or remove home profiles  
**So that** I can keep my dashboard clean

**Acceptance Criteria:**
- Editable nickname/address
- Warnings before deletion (if warranties are linked)

Labels: `UX`, `frontend`, `backend`

---

## 🧱 Epic 3: Warranty Management

### US-005: Add Warranty Manually
**As** a user  
**I want** to input warranty details manually  
**So that** I can track my new appliances

**Acceptance Criteria:**
- Product name, category, brand, purchase date, length
- Auto-calculate expiration date
- Validation on required fields

Labels: `MVP`, `frontend`, `backend`

---

### US-006: Upload Warranty via Receipt Scan
**As** a user  
**I want** to upload a receipt for auto-fill  
**So that** I can save time on data entry

**Acceptance Criteria:**
- OCR auto-fills product name, purchase date, vendor
- Manual review before saving
- Stored in document cloud

Labels: `OCR`, `AI`, `frontend`, `backend`, `integration`

---

### US-007: View & Filter Warranties
**As** a user  
**I want** to view a dashboard of all warranties  
**So that** I can quickly find what I need

**Acceptance Criteria:**
- Table/list view with filters (status, category, home)
- Visual badge for "Expiring Soon" or "Expired"

Labels: `UX`, `dashboard`, `frontend`, `backend`

---

### US-008: Attach Supporting Documents
**As** a user  
**I want** to attach PDFs or images to warranties  
**So that** I have proof of purchase stored

**Acceptance Criteria:**
- Upload drag-and-drop
- Accepts PDF, JPG, PNG
- Links to warranty record

Labels: `MVP`, `upload`, `cloud-storage`, `frontend`

---

## 🧱 Epic 4: Notifications & Reminders

### US-009: Expiration Alerts
**As** a user  
**I want** to be notified before warranties expire  
**So that** I can take action on time

**Acceptance Criteria:**
- Notification 30, 15, 1 day before expiration
- Push (mobile) and email options
- Toggle preferences per warranty

Labels: `notifications`, `reminders`, `frontend`, `backend`

---

### US-010: Resend or Snooze Notifications
**As** a user  
**I want** to snooze or resend alerts  
**So that** I stay flexible

**Acceptance Criteria:**
- Snooze for 1 day or 1 week
- Log of sent notifications

Labels: `UX`, `reminders`, `notifications`, `frontend`

---

## 🧱 Epic 5: Product & Manufacturer Integration

### US-011: Auto-Suggest Manufacturer Support Info
**As** a user  
**I want** to contact the manufacturer easily  
**So that** I can request service or claim

**Acceptance Criteria:**
- Suggest support URL & phone for top brands
- One-click to visit support portal

Labels: `integration`, `data-enrichment`, `frontend`

---

### US-012: Export Warranty Packet
**As** a user  
**I want** to download all my documents in a bundle  
**So that** I can share or backup

**Acceptance Criteria:**
- PDF bundle with warranty data + attachments
- Select by home or category

Labels: `PDF`, `export`, `backend`, `UX`

---

## 🧱 Epic 6: Settings & Admin

### US-013: Profile Settings
**As** a user  
**I want** to update my name, password, and preferences  
**So that** I control my experience

**Acceptance Criteria:**
- Update profile info and password
- Notification preferences per channel

Labels: `MVP`, `UX`, `frontend`, `security`

---

### US-014: Admin Dashboard
**As** an admin  
**I want** to monitor usage and manage support  
**So that** I can help users troubleshoot

**Acceptance Criteria:**
- View registered users, support cases
- Export logs

Labels: `admin`, `internal`, `dashboard`, `backend`

---

## 🧪 QA & Testing Tasks

- [ ] Write unit tests for form validation
- [ ] Integration tests for warranty expiration
- [ ] E2E testing for warranty upload + notification flow
- [ ] Load testing for 1M warranty records

Labels: `QA`, `testing`, `performance`

---

## 🧠 AI / Smart Feature Ideas (Post-MVP)

- [ ] AI Tagging: Suggest categories based on product name
- [ ] Auto-renewal offer tracking via API
- [ ] Document similarity detection for duplicates

Labels: `AI`, `future`, `enhancement`

