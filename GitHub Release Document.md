# Pet Owner App — Unified Desktop Edition
## Initial GitHub Release — Version 1.0.0

This release introduces the first unified version of the Pet Owner App, a simple and
powerful Windows `.exe` application designed for everyday pet owners who want an organized,
offline‑ready way to track their pets’ health, activities, and care routines.

The app uses a lightweight SQL‑ready architecture and includes all features in a single,
one‑time‑purchase build. No subscription tiers, no add‑ons, and no role restrictions.

---

## Included in This Release
- Full Pet Profile Management  
- Vaccination Tracking + Due‑Date Forecasting  
- Medication Tracking + Refill Reminders  
- Activities Log (walks, feeding, grooming, training, playtime)  
- Appointments (vet, grooming, training)  
- Weight Tracking + Charts  
- Photo Gallery  
- Expenses (optional)  
- Reminder Engine  
- PDF Reports  
- Unified local database  
- One installer, one app, one onboarding flow  

---

## User Access Model

The Pet Owner App is designed for **single‑user personal use**.  
There are **no staff roles, no multi‑user accounts, and no subscription plans**.

### Owner (Single Role)
Full access to all features including pets, vaccinations, medications, activities,
appointments, reminders, weight tracking, expenses, and reports.

### Local‑Only Registration
No online account is required.  
No cloud login.  
All data is stored locally on the user’s device.

### Simplified UI Permissions
Because the app is single‑role, all modules are available without gating or restrictions.

### Centralized Permission Enforcement
A simplified RBAC engine ensures consistent access control and future extensibility.

This model ensures a clean, private, and user‑friendly experience for individual pet owners.

---

## Feature Descriptions

### Pet Profiles
Create detailed profiles with photos, medical notes, weight history, and care details.

---

### Vaccination Tracking
Log vaccinations, track due dates, and generate alerts for upcoming or overdue shots.

Includes:
- Due‑date forecasting  
- Color‑coded status indicators  
- PDF vaccination history report  

---

### Medication Tracking
Track medications, dosage instructions, schedules, and refill reminders.

---

### Activities Log
Record daily care activities including:
- Walks  
- Feeding  
- Grooming  
- Training  
- Playtime  
- Custom activities  

---

### Appointments
Manage vet visits, grooming sessions, training appointments, and personal reminders.

---

### Weight Tracking
Log weight entries and view trend charts for long‑term health monitoring.

---

### Photo Gallery
Store and organize pet photos directly inside each pet profile.

---

### Expenses (Optional)
Track pet‑related expenses such as food, grooming, vet bills, and supplies.

---

### Reminders
Automated alerts for:
- Vaccinations  
- Medications  
- Appointments  
- Custom tasks  

---

### Reports
Generate clean PDF summaries for:
- Vaccinations  
- Medications  
- Activities  
- Vet visit summaries  

---

## License Activation
This application requires a valid license key to unlock full functionality.

- You will be prompted to enter your license key on first launch.  
- The app verifies your key securely through the licensing service.  
- If the license is invalid or revoked, access will be restricted.  
- Internet access is required for initial license validation.

After activation, the app operates fully offline.

---

## Database

The Pet Owner App uses a unified local database architecture.

### SQLite (Default Local Database)
- Automatically created and managed by the app  
- Ideal for single‑user personal use  
- Fully offline and self‑contained  

### SQL Server Express (Optional)
- Supported for users who prefer a more robust local database  
- Uses the same schema and feature set  

Both modes use the same unified application and data model.

---

## Stability
This version is the current stable build and serves as the foundation for all future updates.
All modules have been tested for reliability, data integrity, and smooth single‑user
operation.

