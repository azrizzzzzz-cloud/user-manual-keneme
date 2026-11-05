# Medical and Diagnostic Clinic Management System (MDCMS)
## Comprehensive User Operations Manual

---

## Document Control & System Metadata

- **System Title:** Medical and Diagnostic Clinic Management System (MDCMS)
- **Primary Operational Clinics:** 
  - CABS Medical and Diagnostic Clinic (Bagasbas Rd, Brgy. VI, Daet, Camarines Norte)
  - Equal Diagnostic Laboratory
- **Document Type:** Official System User Manual & Standard Operating Procedures
- **Language:** English
- **Target Audience:** Patients, Clinic Administrators, Physicians, Registered Nurses, Receptionists, and Laboratory Technicians
- **Applicable Version:** Release 1.0 (Production Build)

---

# Table of Contents

1. [System Overview & Architecture](#1-system-overview--architecture)
   - 1.1 About MDCMS & Participating Clinics
   - 1.2 System Purpose and Core Capabilities
   - 1.3 Target Audience and User Role Definitions
   - 1.4 Technical Requirements & Supported Web Browsers
2. [Patient Portal & Public Services Guide](#2-patient-portal--public-services-guide)
   - 2.1 Public Landing Page & Services Discovery
   - 2.2 Online Multi-Step Appointment Booking Wizard
   - 2.3 Patient Account Registration & SMS OTP Verification
   - 2.4 Patient Authentication & Session Management
   - 2.5 Navigating the Patient Dashboard
   - 2.6 Viewing and Downloading Diagnostic Test Results
3. [Administrative Portal Navigation & Security](#3-administrative-portal-navigation--security)
   - 3.1 Staff Authentication & Branch Context
   - 3.2 Dynamic Clinic Branding & Visual Themes
   - 3.3 Operations Command Center (Dashboard Overview)
   - 3.4 Topbar Navigation, User Profile Menu & Secure Sign-Out
4. [Patient Management (Records & Clinical Profiles)](#4-patient-management-records--clinical-profiles)
   - 4.1 Viewing and Searching the Patient Registry
   - 4.2 Registering a New Patient (with Immediate Walk-in Option)
   - 4.3 Editing Patient Profiles & Demographics
   - 4.4 Patient 360-Degree Profile (Info, Appointments & Diagnostic Files)
   - 4.5 Generating Printable Patient Summaries and Master Directories
5. [Appointment Scheduling & Clinical Workflow Management](#5-appointment-scheduling--clinical-workflow-management)
   - 5.1 Scheduling Management Overview & Status Filters
   - 5.2 Booking a Staff-Assisted Walk-in or Follow-up Appointment
   - 5.3 Reviewing and Approving Incoming Online Appointments
   - 5.4 Starting Clinical Services (In Progress Workflow)
   - 5.5 Completing Appointments & Clinical Gatekeeper Validation
   - 5.6 Declining or Cancelling Appointments with SMS Alerts
6. [Specialized Clinical Modules](#6-specialized-clinical-modules)
   - 6.1 CABS Anti-Rabies Vaccination & Bite Care Management
     - 6.1.1 Creating & Managing Rabies Charts (Day 0 Intake)
     - 6.1.2 Tracking Comeback Doses (Day 3, Day 7, Day 28)
     - 6.1.3 Overdue Dose Monitoring & Automated SMS Reminders
     - 6.1.4 Printing Rabies Immunization Records & Certificates
   - 6.2 CABS Colon Hydrotherapy & Cleansing Records
     - 6.2.1 Clinical Intake & Contraindications Questionnaire
     - 6.2.2 Documenting Hydrotherapy Treatment Sessions
     - 6.2.3 Generating Patient Information & Legal Consent Printouts
   - 6.3 Equal Diagnostic Laboratory Result Management
     - 6.3.1 Structured Laboratory Templates (Blood Chemistry & Urinalysis)
     - 6.3.2 Entering Test Findings, Reference Values & Verifications
     - 6.3.3 Uploading Diagnostic File Attachments (PDF/Images)
     - 6.3.4 Publishing Lab Reports to the Patient Portal
     - 6.3.5 Printing Official Laboratory Result Sheets
7. [Inventory & Medical Supply Chain Management](#7-inventory--medical-supply-chain-management)
   - 7.1 Inventory Catalog, Stock Alerts & Expiry Monitoring
   - 7.2 Adding New Inventory Items & Threshold Configuration
   - 7.3 Editing Item Details & Stock Replenishment
   - 7.4 Logging Daily Item Consumption via Quick Modal
   - 7.5 Managing Inventory Categories
   - 7.6 Monthly Consumption Matrix Report (31-Day Grid & Print)
8. [Clinic Administration & Content Management](#8-clinic-administration--content-management)
   - 8.1 Clinic Analytics & Business Intelligence Dashboard
   - 8.2 User & Staff Management (RBAC Account Creation & Permissions)
   - 8.3 Managing Published Clinic Services & Pricing
   - 8.4 Managing Promotional Packages & Special Discounts
   - 8.5 Uploading & Publishing Clinic Organizational Charts
   - 8.6 Clinic Profile, Contacts & Color Theme Settings
   - 8.7 System Security, Audit Trail & Activity Logs
9. [Troubleshooting & Frequently Asked Questions (FAQ)](#9-troubleshooting--frequently-asked-questions-faq)
   - 9.1 Common Authentication & SMS OTP Questions
   - 9.2 Appointment Progression & Clinical Blocker Resolutions
   - 9.3 Inventory & Stock Level Questions
   - 9.4 SMS Notification Delivery Guidelines
10. [Document Version & Verification Summary](#10-document-version--verification-summary)

---

# 1. System Overview & Architecture

### 1.1 About MDCMS & Participating Clinics
The **Medical and Diagnostic Clinic Management System (MDCMS)** is a comprehensive, multi-facility clinical operations platform designed to coordinate outpatient medical care, clinical diagnostics, patient communication, and medical supply chain logistics.

The system natively hosts and custom-brands operations for two primary healthcare institutions:
1. **CABS Medical and Diagnostic Clinic:** Located at Bagasbas Road, Barangay VI, Daet, Camarines Norte. A specialized healthcare facility providing general consultation, rabies animal bite vaccination, colon hydrotherapy, ECG, and diagnostic imaging.
2. **Equal Diagnostic Laboratory:** A modern clinical laboratory providing complete diagnostic examinations, blood chemistry analysis, urinalysis, and structured laboratory reporting.

### 1.2 System Purpose and Core Capabilities
MDCMS replaces paper records, disconnected spreadsheets, and manual logbooks with a synchronized, real-time clinical database. Key operational capabilities include:
- **Centralized Electronic Health Registry:** Automated generation of standardized patient identification codes (`PAT<mmddyyyy><###>`), biographical tracking, and lifetime visit histories.
- **Interactive Multi-Step Appointment Scheduling:** Automated timeslot booking for patients and front-desk receptionists with live slot conflict detection and automatic SMS notification.
- **Clinical Quality Gates:** Protection mechanisms preventing appointment closure until mandatory clinical documentation (Rabies Charts, Hydrotherapy Session Sheets, or Lab Results) is validated and signed off.
- **Automated Anti-Rabies Vaccine Booster Scheduling:** Algorithmic calculation of Day 0, Day 3, Day 7, and Day 28 vaccination timelines with automated SMS reminder dispatch and an overdue dose tracking board.
- **Inventory & Supply Matrix:** Granular tracking of medical consumables, pharmaceuticals, reagents, and equipment, featuring a 31-day daily usage matrix and automated low-stock/expiry warnings.
- **Self-Service Patient Portal:** Patient account creation with SMS One-Time Password (OTP) verification, allowing clients to monitor upcoming appointments and retrieve validated diagnostic test results 24/7.

### 1.3 Target Audience and User Role Definitions

```
+----------------------------------------------------------------------------------------------------+
|                                    MDCMS ROLE PERMISSION HIERARCHY                                 |
+---------------+------------------------------------------------------------------------------------+
| Role Name     | Authorized System Responsibilities                                                |
+---------------+------------------------------------------------------------------------------------+
| Patient       | Public self-service booking, profile management, OTP verification, result viewing. |
| Administrator | Full system configuration, branding, staff accounts, analytics, website content.  |
| Doctor        | Patient consultation, clinical assessment, rabies charts, lab validation, orders.  |
| Nurse         | Patient triage, vital signs, walk-in registration, rabies doses, colon cleansing.  |
| Receptionist  | Appointment intake, schedule management, patient registration, phone verification. |
| Lab Tech      | Specimen processing, test value recording, result sheet completion, file uploads.  |
+---------------+------------------------------------------------------------------------------------+
```

- **Patient (Public / Client):** Authenticates via verified Philippine mobile numbers. Can book appointments, select promo discounts, review consultation history, and view/download laboratory reports.
- **Administrator (`admin`):** Holds unconstrained access to all clinic modules, user staff directories, business intelligence analytics, clinic identity branding, promotional campaigns, and security audit logs.
- **Doctor (`doctor`):** Manages clinical consultations, reviews patient medical histories, executes and signs anti-rabies vaccination treatment plans, reviews vital signs, and authorizes diagnostic reports.
- **Nurse (`nurse`):** Performs vital signs assessments, coordinates patient intake, registers walk-in patients, manages rabies vaccination follow-ups, and conducts colon hydrotherapy sessions.
- **Receptionist (`receptionist`):** Manages the clinic front desk, confirms or declines online appointment requests, schedules walk-ins, verifies patient contact information, and generates printed patient directories.
- **Laboratory Technician (`lab_tech`):** Handles specimen diagnostic workflows, enters clinical data into structured laboratory templates, uploads external imaging/PDF documents, and toggles patient portal result visibility.

### 1.4 Technical Requirements & Supported Web Browsers
- **Client Device Requirements:**
  - Desktop PC, Laptop, Tablet, or Smartphone with an active Internet or Local Area Network connection.
  - Minimum display resolution: 375px width (Mobile devices) up to 1920x1080 (High-definition desktop workstations).
- **Supported Web Browsers:**
  - Google Chrome (Version 90+) - *Recommended*
  - Mozilla Firefox (Version 88+)
  - Microsoft Edge (Version 90+)
  - Apple Safari (Version 14+)
  - Mobile Browsers: Chrome for Android, Safari for iOS
- **Peripheral Devices:**
  - Standard office laser or inkjet printer for physical patient records, medical certificates, and inventory reports (A4 or Letter size paper).
- **Communication Prerequisites:**
  - Valid Philippine mobile number (+639 / 09XXXXXXXXX) capable of receiving standard SMS text messages.

---

# 2. Patient Portal & Public Services Guide

```
+----------------------------------------------------------------------------------------------------+
|                                     PATIENT PORTAL USER JOURNEY                                    |
+----------------------------------------------------------------------------------------------------+
| [Visit Public Site] -> [Browse Services & Promos] -> [Book Appointment Online]                     |
|                                     |                                                              |
|                                     v                                                              |
| [Register Phone] ----> [Receive SMS OTP] ---------> [Verify Account & Login]                       |
|                                                             |                                      |
|                                                             v                                      |
| [View Diagnostic Results] <--- [Monitor Appointment Status] <--- [Patient Dashboard]              |
+----------------------------------------------------------------------------------------------------+
```

### 2.1 Public Landing Page & Services Discovery
- **Feature Name:** Public Clinic Web Portal
- **Purpose:** Enables prospective and existing patients to discover operating clinics, review medical service catalogs, examine promotional packages, view clinic contact details, and open the clinic organizational chart.
- **Access:** Direct browser navigation to the system root URL (`http://<server-domain>/index.php` or `http://<server-domain>/services.php`).
- **Prerequisites:** Any active web browser with internet connectivity.
- **Procedure:**
  1. Open the clinic homepage at `index.php`.
  2. Review the top navigation bar containing links for **Services**, **Promos**, **About**, and **Patient Portal**.
  3. Browse through the featured clinic cards displaying **CABS Medical and Diagnostic Clinic** and **Equal Diagnostic Laboratory**.
  4. Click on **Explore Services** to navigate to `services.php`.
  5. Use the clinic filter tabs at the top of the services catalog to alternate between CABS and Equal Diagnostic Laboratory.
  6. Review individual service cards displaying service title, procedural category, duration in minutes, and official pricing.
  7. If available, click **View Organizational Chart** to open an interactive modal displaying the clinic's certified medical and administrative staff hierarchy.
- **Expected Result:** The user can inspect all active clinical capabilities and choose whether to initiate an online appointment or log into their patient account.

`[Insert Figure 1: Public Clinic Landing Page showing Hero Section, Clinic Services, and Booking Link]`

---

### 2.2 Online Multi-Step Appointment Booking Wizard
- **Feature Name:** Online Appointment Booking
- **Purpose:** Allows patients to reserve medical consultations, diagnostic procedures, or laboratory tests online with real-time slot validation.
- **Access:** Click the **Book Appointment** button on the public homepage or navigate directly to `book-appointment.php`.
- **Prerequisites:** Patient must have a valid Philippine mobile number.
- **Procedure:**
  1. Open `book-appointment.php`.
  2. **Step 1: Select Clinic Branch:**
     - Click to select your designated healthcare facility (**CABS Medical and Diagnostic Clinic** or **Equal Diagnostic Laboratory**).
     - Notice that the interface accents and available services immediately adjust to match the selected clinic's branding.
  3. **Step 2: Choose Services & Promotions:**
     - Browse the service list and click the checkbox next to each required service. Multiple services can be combined into a single booking.
     - If an applicable promotional discount is active, select it from the promo dropdown to apply percentage or fixed price reductions.
  4. **Step 3: Select Date & Time Slot:**
     - In the dynamic appointment calendar, click on your desired visit date. Dates in the past or clinics' non-operating days are disabled.
     - The system queries slot availability via an asynchronous background call (`get_booked_slots`).
     - Choose from available morning or afternoon time slots (e.g., `08:00 AM`, `09:30 AM`, `02:00 PM`). Already booked slots are marked unavailable.
  5. **Step 4: Enter Patient Demographics:**
     - If you are logged into your Patient Portal account, your personal details (Full Name, Date of Birth, Gender, Civil Status, Address, Phone Number, and Email) are pre-filled automatically.
     - If booking as a guest, manually enter:
       - **First Name**, **Middle Name** (Optional), and **Last Name**
       - **Date of Birth** (YYYY-MM-DD)
       - **Gender** (Male / Female)
       - **Civil Status** (Single, Married, Divorced, Widowed, Other)
       - **Mobile Phone Number** (Must follow `09XXXXXXXXX` format)
       - **Email Address** (Optional)
       - **Address Details:** Street Address, Barangay, Municipality, and Province
       - **Reason for Visit / Clinical Notes:** Enter any symptoms or remarks for the clinic staff.
  6. Click **Confirm & Submit Booking**.
- **Expected Result:** The screen displays a confirmation alert with a temporary reference code (e.g., `APT20260215-001`). The appointment is placed in `Pending Review` status awaiting clinic reception staff verification. An SMS notification is queued for delivery.

`[Insert Figure 2: Online Multi-Step Appointment Booking Interface with Calendar and Time Slot Selector]`

---

### 2.3 Patient Account Registration & SMS OTP Verification
- **Feature Name:** Patient Portal Registration & Phone Verification
- **Purpose:** Establishes a verified, secure patient identity that connects all medical consultations, appointment records, and laboratory reports across all clinic branches under a single phone number.
- **Access:** Navigate to `patient-portal/register.php`.
- **Prerequisites:** A mobile device capable of receiving SMS messages in the Philippines.
- **Procedure:**
  1. Open `patient-portal/register.php`.
  2. Complete the registration form fields:
     - **Mobile Phone Number:** Enter an 11-digit mobile number beginning with `09` (e.g., `09171234567`).
     - **Password:** Enter a secure password of at least 8 characters.
     - **Confirm Password:** Re-type the password identically.
     - **First Name, Middle Name, Last Name:** Enter official legal names matching government identification.
     - **Date of Birth:** Select date from the date picker.
     - **Gender:** Select Male or Female.
     - **Civil Status:** Select Single, Married, Divorced, Widowed, or Other.
     - **Address:** Enter Street Address, City/Municipality, and Province.
     - **Notification Preferences:** Check the box to receive automated SMS appointment reminders.
  3. Click **Continue to Verification**.
  4. The system validates uniqueness, stores temporary registration data in session memory, generates a 6-digit cryptographic verification code (OTP), and transmits it via Semaphore SMS.
  5. The screen automatically redirects to `patient-portal/verify-otp.php` with an active 10-minute (600 seconds) countdown timer.
  6. Check your mobile device SMS inbox for a text from the clinic containing your 6-digit code.
  7. Enter the 6-digit code into the OTP input field and click **Verify & Complete Registration**.
  8. *Optional / Resend:* If the SMS does not arrive within 60 seconds, click **Resend Verification Code** to dispatch a new code.
- **Expected Result:** The system validates the OTP, creates a master record in `patient_portal_accounts`, automatically associates any existing clinic patient profiles sharing the identical mobile number, and signs the user into the Patient Portal Dashboard.

`[Insert Figure 3: Patient Registration Form with Philippine Mobile Number Format and Input Fields]`
`[Insert Figure 4: Patient OTP Verification Screen with Countdown Timer and Resend Option]`

---

### 2.4 Patient Authentication & Session Management
- **Feature Name:** Patient Portal Sign-In
- **Purpose:** Securely authenticates returning patients into their personal medical portal.
- **Access:** Navigate to `patient-portal/index.php`.
- **Prerequisites:** An existing, OTP-verified portal account.
- **Procedure:**
  1. Open `patient-portal/index.php`.
  2. Enter your registered **Mobile Phone Number** (e.g., `09171234567`).
  3. Enter your **Password**.
  4. Click **Sign In**.
- **Expected Result:** The system validates the bcrypt-hashed password, establishes a strictly isolated patient session (`$_SESSION['patient_logged_in'] = true`), clears any administrative session keys to prevent session leakage, updates `last_login`, and redirects to `patient-portal/dashboard.php`.
- **Important Note:** Entering an incorrect phone number or password displays a red error alert: *"Invalid phone number or password."*

---

### 2.5 Navigating the Patient Dashboard
- **Feature Name:** Patient Personal Dashboard
- **Purpose:** Serves as the patient's centralized command center for tracking appointments, viewing linked clinic patient codes, and monitoring upcoming clinical visits.
- **Access:** Automatically loaded after login, or via direct link `patient-portal/dashboard.php`.
- **Prerequisites:** Authenticated patient portal session.
- **Procedure:**
  1. Review the **Clinic Identity Badges** at the top of the dashboard. This section lists every clinic where you hold an active medical record along with your designated **Patient Code** (e.g., `PAT02152026001` at CABS Medical Clinic).
  2. **Filtering Appointments:**
     - Use the **Clinic Filter** dropdown to isolate appointments scheduled at CABS Medical Clinic or Equal Diagnostic Laboratory.
     - Use the **Status Filter** dropdown to filter appointments by status: *Pending Review*, *Confirmed*, *In Progress*, *Completed*, or *Cancelled*.
  3. **Reviewing Upcoming Schedule:**
     - Inspect the appointment cards showing the appointed date, time, clinical service name, attending physician (if assigned), and real-time status badge.
  4. **Booking Follow-Up Visits:**
     - Click the **Book New Appointment** button in the dashboard header to jump directly into the booking wizard with your personal information pre-loaded.
  5. **Signing Out:**
     - Click **Logout** in the navigation header to safely terminate your patient session (`patient-portal/logout.php`).

`[Insert Figure 5: Patient Portal Dashboard displaying Linked Clinic Records and Appointment History]`

---

### 2.6 Viewing and Downloading Diagnostic Test Results
- **Feature Name:** Patient Diagnostic Results Repository
- **Purpose:** Allows patients to view and review validated laboratory and diagnostic exam sheets published by clinical staff.
- **Access:** Click **My Results** in the patient portal navigation or open `patient-portal/results.php`.
- **Prerequisites:** Patient must have completed diagnostic tests that clinic staff have marked as `Completed` and explicitly toggled to `is_visible_to_patient = 1`.
- **Procedure:**
  1. Open `patient-portal/results.php`.
  2. Use the clinic dropdown filter to narrow results by clinic.
  3. Review the test results table, which displays:
     - **Test Date**
     - **Clinic Name**
     - **Service / Examination Name** (e.g., Blood Chemistry, Urinalysis, Chest X-Ray)
     - **Uploader / Attending Examiner**
     - **Result Format** (Structured Clinical Sheet or Attached PDF/Image)
  4. To inspect a structured result sheet, click **View Structured Result** to load `patient-portal/lab-result.php?id=<result_id>`.
  5. Review individual clinical parameters (e.g., Fasting Blood Sugar, Uric Acid, Cholesterol) along with their official standard reference intervals.
  6. To open an uploaded laboratory attachment (e.g., Ultrasound scan or scanned certificate), click **Download / View Attachment** to open the secure document in a new browser tab.
- **Expected Result:** The patient securely inspects their medical test findings without needing to visit the clinic in person. Draft or unverified results remain strictly hidden from this screen.

`[Insert Figure 6: Patient Diagnostic Results Repository showing Released Lab Reports]`

---

# 3. Administrative Portal Navigation & Security

```
+----------------------------------------------------------------------------------------------------+
|                                    STAFF LOGIN & WORKSPACE ROUTING                                 |
+----------------------------------------------------------------------------------------------------+
| [Staff Credentials (admin/login.php)] ------> [Authenticate & Resolve branch_id]                   |
|                                                       |                                            |
|                  +------------------------------------+------------------------------------+       |
|                  v                                                                         v       |
|   [Branch 2: CABS Medical Clinic]                                           [Branch 3: Equal Lab]  |
|   - Green Branding (#0a5c5c)                                                - Dark Green (#195b25) |
|   - Rabies Tracking Module Enabled                                          - Lab Result Templates |
|   - Colon Cleansing Module Enabled                                          - Specimen Processing  |
+----------------------------------------------------------------------------------------------------+
```

### 3.1 Staff Authentication & Branch Context
- **Feature Name:** Staff Administrative Sign-In
- **Purpose:** Authenticates administrative, medical, nursing, reception, and laboratory personnel into their assigned clinic branch workspace.
- **Access:** Navigate to `admin/login.php` or `admin/index.php`.
- **Prerequisites:** Valid staff account registered in the `users` database table.
- **Procedure:**
  1. Open `admin/login.php`.
  2. In the **Username or Email Address** field, enter your assigned administrative username or registered staff email.
  3. In the **Password** field, enter your password.
  4. Click **Sign In to System**.
  5. The backend (`Auth.php`) verifies user status (`is_active = 1`), evaluates the password hash, resolves the user's assigned `branch_id`, logs the authentication event into `activity_logs`, and establishes the staff session:
     - `$_SESSION['user_id']`: Primary staff record ID
     - `$_SESSION['role']`: Role string (`admin`, `doctor`, `nurse`, `receptionist`, `lab_tech`)
     - `$_SESSION['branch_id']`: Default clinic operating branch (e.g., `2` for CABS Clinic, `3` for Equal Diagnostic)
  6. The system automatically redirects the browser to `admin/dashboard.php`.
- **Expected Result:** The authenticated user arrives at the primary operational dashboard, customized with their facility's official colors, logo, and authorized module links.

`[Insert Figure 7: Staff Administrative Login Screen with Dynamic Clinic Identity]`

---

### 3.2 Dynamic Clinic Branding & Visual Themes
- **Feature Name:** Branch Context & Visual Theming Engine
- **Purpose:** Automatically adjusts the administrative user interface (colors, navigation styles, clinic headers, and document letterheads) based on the staff member's assigned facility.
- **Mechanism:** The helper `includes/clinic_helper.php` loads the active branch metadata and injects dynamic CSS variables into the page header:
  - `--clinic-primary`: Primary banner and sidebar background color (Default: `#0a5c5c` for CABS Clinic; `#195b25` for Equal Diagnostic).
  - `--clinic-accent`: Highlight and active button color (Default: `#0fa8a8` for CABS Clinic; `#71e600` for Equal Diagnostic).
  - `--dashboard-bg`: Content area background tint.
- **Expected Result:** Staff working at CABS Clinic see the teal/cyan identity, while personnel logged into Equal Diagnostic Laboratory see the specialized laboratory theme.

---

### 3.3 Operations Command Center (Dashboard Overview)
- **Feature Name:** Administrative Operations Dashboard
- **Purpose:** Delivers high-level operational situational awareness, schedule visibility, inventory alerts, and specialized clinical follow-up reminders.
- **Access:** Click **Dashboard** in the sidebar navigation or open `admin/dashboard.php`.
- **Prerequisites:** Authenticated staff session.
- **Components:**
  1. **Operational Metric Stat Cards:**
     - **TOTAL PATIENTS:** Active registered patients in the clinic branch.
     - **TODAY'S APPOINTMENTS:** Total visits scheduled for the current date, accompanied by upcoming visit counts.
     - **LOW STOCK ITEMS:** Count of inventory items whose current quantity has fallen to or below the minimum reorder threshold.
     - **ACTIVITY LOG:** Summary counter of operational actions logged today with a direct link to the audit log.
  2. **Today's Schedule Panel:**
     - Displays chronological visit cards showing appointment time, patient name, requested service, assigned branch tag, and status badge.
     - Includes a **View all** shortcut linking to the full scheduling module.
  3. **Inventory Alerts Panel:**
     - Displays real-time warnings for items with low stock or approaching expiration dates, showing current quantity, unit of measure, and minimum stock threshold.
  4. **Overdue Anti-Rabies Doses Board (CABS Clinic Branch 2 Only):**
     - Highlights rabies animal bite patients with scheduled Day 3, Day 7, or Day 28 vaccination comeback dates that have passed without recorded treatment.
     - Displays patient name, required dose label, days overdue, contact phone number, and a direct **Open Chart** action button.

`[Insert Figure 8: Administrative Main Dashboard highlighting Statistics Cards, Schedule, and Critical Alerts]`

---

### 3.4 Topbar Navigation, User Profile Menu & Secure Sign-Out
- **Feature Name:** Topbar Navigation & Profile Dropdown
- **Purpose:** Provides persistent real-time clock monitoring, mobile menu toggling, and quick access to staff account actions.
- **Access:** Present across the top header of all administrative pages.
- **Elements:**
  1. **Mobile Menu Toggle (Hamburger Icon):** Expands the sidebar on small screens.
  2. **Date & Time Display:** Real-time clock displaying the current day, date, and live operating time.
  3. **User Profile Pill (`tum-btn`):**
     - Shows staff initials badge, full name, and assigned role title.
     - Clicking the pill opens the User Actions dropdown menu:
       - **Activity Logs:** Direct link to review system-wide audit logs (`admin/activity-logs.php`).
       - **Clinic Settings (Admin Role Only):** Direct link to configure clinic parameters (`admin/settings.php`).
       - **Logout:** Terminates the administrative session (`admin/logout.php`), destroys session cookies, records the sign-out in `activity_logs`, and redirects to `admin/login.php`.

---

# 4. Patient Management (Records & Clinical Profiles)

```
+----------------------------------------------------------------------------------------------------+
|                                    PATIENT RECORD LIFECYCLE                                        |
+----------------------------------------------------------------------------------------------------+
| [Walk-in / Online Intake] ---> [Generate PAT<mmddyyyy><###>] ---> [Store Medical Background]       |
|                                                                                |                   |
|                   +------------------------------------------------------------+                   |
|                   v                                                            v                   |
| [Tab 1: Personal & Medical Info]       [Tab 2: Appointment History]   [Tab 3: Diagnostic Results]  |
| - Allergies, Chronic Illness           - Service & Physician Logs     - Lab Sheets & PDF Uploads   |
| - Vital Signs & Emergency Contact      - Direct Status Progression    - Portal Release Toggle      |
+----------------------------------------------------------------------------------------------------+
```

### 4.1 Viewing and Searching the Patient Registry
- **Feature Name:** Patient Registry Directory
- **Purpose:** Allows clinical staff to search, filter, and inspect the master index of registered patients.
- **Access:** Click **Patients** in the administrative sidebar or open `admin/patients/index.php`.
- **Prerequisites:** Staff login with any authorized role.
- **Procedure:**
  1. Open `admin/patients/index.php`.
  2. **Search Operations:** Enter a patient code (e.g., `PAT02152026001`), first name, last name, mobile phone number, or email into the search bar and press **Enter**.
  3. **Filter by Service:** Select a specific service category from the service filter dropdown to view only patients who have received that service.
  4. Review the tabular directory columns:
     - **Patient Code:** Official system identifier.
     - **Patient Name:** Legal full name with gender and age indicators.
     - **Contact:** Mobile number and email address.
     - **Portal Status:** Indicates whether the patient has an active linked patient portal account.
     - **Last Visit Date:** Date of most recent clinical encounter.
     - **Actions:** Quick links to **View Profile**, **Edit**, or **Print Patient Summary**.

`[Insert Figure 9: Master Patient Directory Table with Search Filters and Quick Action Buttons]`

---

### 4.2 Registering a New Patient (with Immediate Walk-in Option)
- **Feature Name:** Patient Registration & Walk-In Intake
- **Purpose:** Enrolls a new patient into the clinic registry and optionally generates an immediate walk-in appointment in `In Progress` status.
- **Access:** Click **Add Patient** in the patient directory or open `admin/patients/add.php`.
- **Prerequisites:** Receptionist, Nurse, Doctor, or Admin role.
- **Procedure:**
  1. Open `admin/patients/add.php`.
  2. Complete the **Personal Information** section:
     - **First Name**, **Middle Name**, and **Last Name** (Mandatory).
     - **Date of Birth** (Mandatory - calculates age automatically).
     - **Gender:** Select *Male* or *Female*.
     - **Civil Status:** Select *Single*, *Married*, *Divorced*, *Widowed*, or *Other*.
     - **Blood Type:** Select from *A+*, *A-*, *B+*, *B-*, *AB+*, *AB-*, *O+*, *O-*, or *Unknown*.
  3. Complete the **Contact Information** section:
     - **Mobile Phone Number:** Enter an 11-digit mobile number (`09XXXXXXXXX`).
     - **Email Address:** Optional.
     - **Address Details:** Street Address, Barangay, Municipality/City, Province, and Zip Code.
  4. Complete the **Emergency Contact** section:
     - Emergency Contact Name, Contact Phone Number, and Relationship.
  5. Complete the **Medical Background** section:
     - Known Drug or Food Allergies, Chronic Medical Conditions, and Current Medications.
  6. **Immediate Walk-In Service Selection (Optional):**
     - If the patient is physically present for immediate care, check the boxes for one or more services under **Walk-In Services**.
     - If an active promotion applies, select it from the **Promo Discount** dropdown.
  7. Click **Register Patient**.
- **Expected Result:**
  - The system generates a standardized patient code (`PAT<mmddyyyy><###>`) via database trigger.
  - The record is stored in `patients`.
  - If a portal account exists with the same phone number, the system automatically links `portal_account_id`.
  - If walk-in services were selected, an appointment is automatically created for today in `In Progress` status, and the user is redirected to the appropriate clinical form (Rabies Chart, Colon Cleansing, or Lab Form).

`[Insert Figure 10: Patient Registration Form with Walk-in Service Selection and Promo Tagging]`

---

### 4.3 Editing Patient Profiles & Demographics
- **Feature Name:** Patient Profile Modification
- **Purpose:** Updates existing patient biographical data, contact numbers, or medical notes.
- **Access:** In the patient registry or profile, click **Edit** or open `admin/patients/edit.php?id=<patient_id>`.
- **Prerequisites:** Authorized staff session.
- **Procedure:**
  1. Open `admin/patients/edit.php?id=<patient_id>`.
  2. Update any modified fields (e.g., new mobile number, updated address, newly diagnosed allergies).
  3. Toggle the **Active Status** checkbox if archiving an inactive record.
  4. Click **Update Patient Information**.
- **Expected Result:** The record updates in `patients`, an `UPDATE_PATIENT` event is recorded in `activity_logs`, and a green confirmation message is displayed.

---

### 4.4 Patient 360-Degree Profile (Info, Appointments & Diagnostic Files)
- **Feature Name:** Patient 360 Comprehensive Medical Profile
- **Purpose:** Consolidates all patient demographics, historical visits, clinical documents, and diagnostic test files into a single unified tabbed interface.
- **Access:** Click on any patient row in the registry or open `admin/patients/view.php?id=<patient_id>`.
- **Interface Structure:**
  1. **Patient Header Card:**
     - Displays patient legal name, patient code badge, age, gender, blood type, mobile number, address, and quick action links (**Edit Profile**, **Print Summary**, **Book Appointment**).
  2. **Tab 1: Personal & Medical Info (`tab=info`):**
     - Displays complete demographic information, emergency contacts, allergy warnings, chronic illness history, and medical background notes.
     - For CABS Clinic patients, includes quick action links to **Open Rabies Chart** or **Open Colon Cleansing Record**.
  3. **Tab 2: Appointments (`tab=appointments`):**
     - Lists all past and upcoming clinic visits with appointment dates, times, requested services, assigned physicians, status badges, and direct links to inspect appointment records.
  4. **Tab 3: Laboratory & Diagnostic Results (`tab=results`):**
     - **Uploaded Laboratory Results:** Table of uploaded PDF or image diagnostic reports with download links, upload timestamps, and deleting permissions.
     - **Direct File Upload Box:** Choose an appointment to associate, choose file (PDF, JPG, PNG up to 10 MB), enter a result title and remarks, check *Make visible to patient portal*, and click **Upload Result File**.
     - **Structured Equal Lab Sheets (Branch 3):** Lists completed Blood Chemistry or Urinalysis forms with an interactive toggle switch to publish or withdraw reports from the patient portal.

`[Insert Figure 11: Patient 360 Profile View showing Info, Appointments, and Laboratory Tabs]`

---

### 4.5 Generating Printable Patient Summaries and Master Directories
- **Feature Name:** Physical Documentation & Print Reports
- **Purpose:** Generates formatted physical copies of patient clinical summaries and master patient directories.
- **Access:** Click **Print Patient** in the patient profile, or **Print Directory** in the patient index.
- **Procedure for Individual Summary (`print-patient.php?id=<id>`):**
  1. From `admin/patients/view.php`, click **Print Summary**.
  2. A new browser tab opens loading `admin/patients/print-patient.php`.
  3. The page renders a formal clinic header, clinic logo, patient identification details, vital stats, allergy alerts, chronic illness list, and recent appointment visit logs.
  4. The browser's native print dialog opens automatically. Select your printer and click **Print**.
- **Procedure for Master Directory (`print-directory.php`):**
  1. From `admin/patients/index.php`, apply any search or service filters, then click **Print Directory**.
  2. A new browser tab opens loading `admin/patients/print-directory.php`.
  3. The page renders an official multi-page directory table of all matching patients with sign-off signature lines for the clinic medical director.

`[Insert Figure 12: Printable Patient Medical Record and Directory Print Preview]`

---

# 5. Appointment Scheduling & Clinical Workflow Management

```
+----------------------------------------------------------------------------------------------------+
|                                  APPOINTMENT STATE MACHINE & GATES                                 |
+----------------------------------------------------------------------------------------------------+
| [Patient Books Online]  -------------------------> [Pending Review]                                |
|                                                            |                                       |
| [Staff Confirms Booking] ------------------------> [Confirmed] <--- [Automated SMS Dispatched]     |
|                                                            |                                       |
| [Patient Arrives at Clinic] ---------------------> [In Progress]                                   |
|                                                            |                                       |
|                                                            v                                       |
|                                              <Clinical Gatekeeper Validation>                      |
|                                              - Rabies Service? Rabies Chart Saved?                 |
|                                              - Hydrotherapy? Consent Sheet Saved?                  |
|                                              - Equal Lab? Result Uploaded/Finished?                |
|                                                            |                                       |
|                                                            v                                       |
| [Validation Passes] -----------------------------> [Completed]                                     |
|                                                                                                    |
| [Patient No-Show / Declined] --------------------> [Cancelled] <--- [Cancellation SMS Sent]       |
+----------------------------------------------------------------------------------------------------+
```

### 5.1 Scheduling Management Overview & Status Filters
- **Feature Name:** Appointment Scheduling Management
- **Purpose:** Serves as the central operational hub for monitoring, filtering, and updating clinical visits.
- **Access:** Click **Scheduling** in the administrative sidebar or open `admin/appointments/index.php`.
- **Prerequisites:** Authorized staff session.
- **Procedure:**
  1. Open `admin/appointments/index.php`.
  2. Review the **Status Filter Tabs** along the top:
     - **All Appointments:** Comprehensive chronological register.
     - **Pending Review / Pending:** Online booking requests awaiting staff approval.
     - **Confirmed:** Approved appointments awaiting patient arrival.
     - **In Progress:** Patients currently undergoing clinical triage, examination, or treatment.
     - **Completed:** Finalized visits with completed clinical documentation.
     - **Cancelled:** Declined or retracted appointments.
  3. Use the **Date Range Filter** to narrow the view to today, this week, or a custom date range.
  4. Inspect individual table rows showing Appointment ID, Patient Name, Date & Time, Services, Doctor, and Quick Action buttons (**Approve**, **Start**, **Complete**, **View Details**).

`[Insert Figure 13: Scheduling Management Overview with Status Filter Tabs]`

---

### 5.2 Booking a Staff-Assisted Walk-in or Follow-up Appointment
- **Feature Name:** Staff Manual Appointment Booking
- **Purpose:** Allows front-desk staff to schedule appointments for walk-in patients or those booking by phone.
- **Access:** Click **New Appointment** in the scheduling screen or open `admin/appointments/add.php`.
- **Prerequisites:** Receptionist, Nurse, Doctor, or Admin role.
- **Procedure:**
  1. Open `admin/appointments/add.php`.
  2. **Select Patient:** Use the searchable patient dropdown to type the patient's name or code, then select their record.
  3. **Select Services:** Check the boxes for all services the patient requires.
  4. **Apply Promotion (Optional):** Select an active promotional discount from the promo dropdown if applicable.
  5. **Select Date & Time:** Choose the appointment date and select an available time slot.
  6. **Assign Doctor (Optional):** Select an attending physician from the staff dropdown.
  7. **Notes:** Enter any relevant patient symptoms, referrals, or clinical remarks.
  8. Click **Schedule Appointment**.
- **Expected Result:** The appointment is saved in `Confirmed` status. If the patient has a valid phone number, an automated confirmation SMS is sent via Semaphore SMS, and the schedule refreshes.

`[Insert Figure 14: Manual Staff Appointment Booking Form with Patient Search and Time Slot Selector]`

---

### 5.3 Reviewing and Approving Incoming Online Appointments
- **Feature Name:** Appointment Approval & Online Patient Intake
- **Purpose:** Evaluates pending appointments submitted through the public booking wizard, validates scheduling, automatically provisions patient records if needed, and dispatches SMS approvals.
- **Access:** Open `admin/appointments/view.php?id=<id>` or click **Approve** directly from the appointment index.
- **Prerequisites:** Appointment must be in `Pending Review` or `Pending` status.
- **Procedure:**
  1. Navigate to the appointment details page (`admin/appointments/view.php?id=<id>`).
  2. Inspect the booking details, requested service, date, time slot, and patient contact information.
  3. Click **Approve Appointment** (triggers `process-action.php?action=approve&id=<id>`).
  4. **Automated Patient Verification Logic:**
     - If the booking is already linked to an existing patient, its status transitions to `Confirmed`.
     - If the booking was made by a guest, the system checks whether the phone number matches an existing portal account or patient record. If found, it links the records.
     - If no match exists, the system automatically creates a new patient record with a generated patient code (`PAT<mmddyyyy><###>`), associates it with the appointment, and transitions the status to `Confirmed`.
  5. **Automated SMS Notification:** The system calls `sendAppointmentApproved()` to transmit an SMS notification confirming the approved date, time, and service name.
- **Expected Result:** The appointment status badge turns teal (`Confirmed`), the patient receives an SMS confirmation, and an audit entry is logged.

`[Insert Figure 15: Appointment Details View showing Workflow Action Buttons (Approve, Start, Complete, Decline)]`

---

### 5.4 Starting Services (In Progress Workflow)
- **Feature Name:** Appointment Clinical Service Intake
- **Purpose:** Marks the physical arrival and active clinical intake of a confirmed patient.
- **Access:** On the appointment details view, click **Start Service** (triggers `process-action.php?action=start&id=<id>`).
- **Prerequisites:** Appointment must be in `Confirmed` status and linked to a valid patient record.
- **Procedure:**
  1. Open the confirmed appointment view.
  2. Verify the patient has arrived at the clinic.
  3. Click **Start Service**.
- **Expected Result:** Appointment status transitions to `In Progress` (blue badge). The action bar updates with direct links to required clinical documentation:
  - If service is Rabies bite treatment: **Open Rabies Chart** link appears.
  - If service is Colon Hydrotherapy: **Open Patient Information & Consent** link appears.
  - If service is Diagnostic Laboratory: **Upload Laboratory Result** or **Open Lab Form** link appears.

---

### 5.5 Completing Appointments & Clinical Gatekeeper Validation
- **Feature Name:** Clinical Gatekeeper & Appointment Finalization
- **Purpose:** Marks an appointment as completed while enforcing clinical compliance rules before allowing closure.
- **Access:** Click **Complete Service** (triggers `process-action.php?action=complete&id=<id>`).
- **Prerequisites:** Appointment must be in `In Progress` status.
- **Clinical Compliance Gates (`appointmentCompletionBlocker`):**
  - **Rule 1 (CABS Anti-Rabies):** If the service name includes *rabies*, *anti-rabies*, *arv*, or *bite*, the system checks `rabies_charts` for a saved chart matching this patient and appointment date. If none exists, completion is blocked with the warning: *"Save the patient's rabies chart before completing this appointment."*
  - **Rule 2 (CABS Colon Hydrotherapy):** If the service name includes *colon*, *hydrotherapy*, or *cleansing*, the system checks `colon_cleansing_records` for a saved record. If none exists, completion is blocked with the warning: *"Save the patient information and consent record before completing this appointment."*
  - **Rule 3 (Equal Diagnostic Laboratory):** For Branch 3, the system checks that an official laboratory file has been uploaded to `patient_results` or that a structured `lab_result_sheets` entry has been marked `Completed`. If neither exists, completion is blocked with the warning: *"Upload the laboratory result file before completing this appointment."*
- **Procedure:**
  1. Complete all required clinical charts and test results as detailed in Section 6.
  2. Return to the appointment view page.
  3. Click **Complete Service**.
- **Expected Result:** The system validates that all clinical requirements are satisfied, updates appointment status to `Completed` (green badge), and logs the completion event in `activity_logs`.

---

### 5.6 Declining or Cancelling Appointments with SMS Alerts
- **Feature Name:** Appointment Cancellation & Rejection
- **Purpose:** Declines an unconfirmable online appointment or cancels an existing booking due to scheduling conflicts or patient request.
- **Access:** Click **Decline** or **Cancel** on the appointment page (triggers `process-action.php?action=decline&id=<id>`).
- **Procedure:**
  1. Open the appointment view.
  2. Click **Decline / Cancel Appointment**.
  3. When prompted, enter a reason for cancellation (e.g., *"Doctor unavailable due to emergency"* or *"Patient requested reschedule"*).
  4. Confirm the prompt.
- **Expected Result:** The appointment status updates to `Cancelled` (red badge). The system dispatches an SMS notification informing the patient that their appointment was cancelled and providing the clinic contact number for rescheduling.

---

# 6. Specialized Clinical Modules

```
+----------------------------------------------------------------------------------------------------+
|                                    SPECIALIZED CLINICAL MODULES                                    |
+-------------------------------------------------+--------------------------------------------------+
| CABS CLINIC SPECIALIZATIONS (Branch 2)          | EQUAL DIAGNOSTIC SPECIALIZATIONS (Branch 3)      |
+-------------------------------------------------+--------------------------------------------------+
| 1. Rabies Vaccination & Bite Care Management    | 1. Structured Blood Chemistry Analyzer Template  |
|    - Day 0 Intake, Bite Grading & Vitals        |    - Glucose FBS, Uric Acid, BUN, Creatinine     |
|    - Day 0, Day 3, Day 7, Day 28 Schedules      |    - Lipids, Liver Enzymes, Electrolytes, Thyroid|
|    - Overdue Dose Tracking & Automated SMS      | 2. Structured Urinalysis Diagnostic Sheet        |
| 2. Colon Hydrotherapy & Cleansing Records       |    - Physical, Chemical & Microscopic Casts/RBC  |
|    - Contraindications & Health Questionnaire   | 3. Diagnostic File Attachments (PDF / Imaging)   |
|    - Water Volume, Pressure & Session Logs      | 4. Patient Portal Result Publishing Engine       |
|    - Dual Printouts: Patient Info & Consent     | 5. Formal Laboratory Printout with Signatures    |
+-------------------------------------------------+--------------------------------------------------+
```

### 6.1 CABS Anti-Rabies Vaccination & Bite Care Management

#### 6.1.1 Creating & Managing Rabies Charts (Day 0 Intake)
- **Feature Name:** Anti-Rabies Clinical Treatment Chart
- **Purpose:** Comprehensive clinical recording for animal bite injuries, post-exposure prophylaxis (PEP), vital signs, wound assessment, and vaccine administration.
- **Access:** From a patient profile or appointment view, click **Open Rabies Chart** or open `admin/rabies/chart.php?patient_id=<id>&appointment_id=<apt_id>`.
- **Prerequisites:** CABS Medical Clinic (Branch 2); Doctor or Nurse role.
- **Procedure:**
  1. Open `admin/rabies/chart.php`.
  2. Complete **Section 1: Patient Background:**
     - Religion, Mother's Name, Father's Name, Spouse Name, and Spouse Contact Number.
  3. Complete **Section 2: Day 0 Incident & Wound Assessment:**
     - **Date & Time of Consultation**
     - **Nature of Injury (NOI):** Detailed description of the exposure incident.
     - **Place of Incident (POI), Date of Incident (DOI), Time of Incident (TOI)**
     - **Source of Injury (SOI):** Animal species (Dog, Cat, etc.).
     - **Exposure Category (EXO):** Category I (Touching/Feeding), Category II (Minor scratches/abrasions without bleeding), or Category III (Transdermal bites/scratches, licks on broken skin).
     - **Condition of Biting Animal (COB):** Alive, Dead, Rabid, Unknown.
     - **Circumstance of Animal (COA):** Provoked, Unprovoked.
  4. Complete **Section 3: Vital Signs:**
     - Temperature, Pulse Rate (HR), Respiratory Rate (RR), Blood Pressure (BP), Oxygen Saturation ($O_2$ Sat), and Body Weight (kg).
  5. Complete **Section 4: Biologicals & Medication Administration:**
     - **Equine Rabies Immunoglobulin (ERIG):** Dosage in mL, date given, and administering nurse/doctor name.
     - **Tetanus Toxoid (TT) & Anti-Tetanus Serum (ATS):** Dosage, status, and administration date.
     - **Antibiotics & Pain Relievers:** Prescribed medications, dosage, and duration in days.
     - **Observation Period:** Number of days to observe the biting animal.
  6. Complete **Section 5: Comeback Vaccination Schedule:**
     - The system automatically calculates and displays standard post-exposure comeback dates based on the initial Day 0 dose date:
       - **Day 0:** Date of initial dose.
       - **Day 3:** Day 0 + 3 days.
       - **Day 7:** Day 0 + 7 days.
       - **Day 28:** Day 0 + 28 days.
  7. Enter Physician and Nurse signatures in the verification section.
  8. Click **Save Rabies Chart**.
- **Expected Result:** The chart is saved to `rabies_charts`, enabling appointment completion for rabies services and activating vaccine reminder tracking.

`[Insert Figure 16: Rabies Dose Reminder Manager showing Upcoming and Overdue Vaccine Doses with SMS Triggers]`
`[Insert Figure 17: Comprehensive Anti-Rabies Vaccination Treatment Chart (Day 0 Intake and Vital Signs)]`

---

#### 6.1.2 Tracking Comeback Doses (Day 3, Day 7, Day 28)
- **Feature Name:** Rabies Follow-Up Dose Intake
- **Purpose:** Documents subsequent vaccination encounters when the patient returns for booster doses.
- **Procedure:**
  1. Open the existing rabies chart for the patient.
  2. Navigate to the relevant follow-up dose section (**Day 3 Dose Entry**, **Day 7 Dose Entry**, or **Day 28 Dose Entry**).
  3. Enter the consultation date and time, current wound healing status, observing nurse/doctor name, and any clinical notes.
  4. Click **Save Rabies Chart**.
- **Expected Result:** The comeback dose is recorded as completed, clearing any overdue alert for this dose on the clinic dashboard.

---

#### 6.1.3 Overdue Dose Monitoring & Automated SMS Reminders
- **Feature Name:** Rabies Dose Reminder Manager
- **Purpose:** Monitors immunization compliance, identifies overdue doses, and dispatches automated SMS reminders.
- **Access:** Click **Rabies Reminders** in the sidebar or open `admin/rabies/reminders.php`.
- **Procedure:**
  1. Open `admin/rabies/reminders.php`.
  2. Review the **Doses Due Tomorrow** panel. Click **Send SMS Reminders** to transmit reminder messages to all patients with doses scheduled for the following day.
  3. Review the **Overdue Doses Board** listing patients whose scheduled comeback dates have passed without an updated chart entry.
  4. Click **Send Manual SMS** next to any patient to send an immediate custom reminder text: *"Reminder from CABS Clinic: Your Day X anti-rabies vaccination is due. Please visit the clinic promptly."*
- **Expected Result:** SMS reminders are sent via Semaphore SMS and logged in `sms_notifications`.

---

#### 6.1.4 Printing Rabies Immunization Records & Certificates
- **Feature Name:** Printable Rabies Chart & Certificate
- **Purpose:** Generates a physical immunization record card and medical certificate for school, employment, or legal purposes.
- **Access:** On the rabies chart page, click **Print Rabies Chart** or open `admin/rabies/print.php?id=<chart_id>`.
- **Procedure:**
  1. Click **Print Rabies Chart**.
  2. A new browser tab opens with the formal anti-rabies treatment sheet, wound assessment diagram, immunization dose schedule, and physician signature block.
  3. Print the document via the browser's native print dialog.

`[Insert Figure 18: Printable Anti-Rabies Vaccination Chart and Medical Certificate]`

---

### 6.2 CABS Colon Hydrotherapy & Cleansing Records

#### 6.2.1 Clinical Intake & Contraindications Questionnaire
- **Feature Name:** Colon Hydrotherapy Intake & Assessment
- **Purpose:** Documents pre-treatment health evaluation and screens for clinical contraindications prior to colon cleansing procedures.
- **Access:** Click **Open Patient Information & Consent** on an appointment or patient profile, or navigate to `admin/colon-cleansing/form.php?patient_id=<id>`.
- **Prerequisites:** CABS Medical Clinic (Branch 2); Doctor or Nurse role.
- **Procedure:**
  1. Open `admin/colon-cleansing/form.php?patient_id=<id>`.
  2. Complete **Section 1: General & Lifestyle Evaluation:**
     - Patient Occupation, Daily Water Intake (glasses/day), Bowel Movement Frequency.
     - Lifestyle habits: Smoking (Yes/No), Alcohol Consumption (Yes/No), Herbal/Probiotic Supplements usage.
     - Previous hydrotherapy history and date of last session.
  3. Complete **Section 2: Contraindications & Medical History:**
     - Check all applicable conditions: Severe Cardiac Disease, Uncontrolled Hypertension, Aneurysm, Severe Anemia, GI Hemorrhage/Perforation, Severe Hemorrhoids, Diverticulitis, Ulcerative Colitis, Crohn's Disease, Cancer of the Colon, Recent Colon Surgery, Renal Insufficiency.
     - Document any other medical conditions or current medications in the text areas.
  4. Complete **Section 3: Reported Symptoms:**
     - Check all presenting symptoms: Constipation, Bloating, Gas, Headaches, Fatigue, Skin Problems, Halitosis (Bad Breath), Back Pain, Weight Issues.
  5. Record baseline vital signs: Blood Pressure, Body Weight, and Body Temperature.
  6. Click **Save Colon Cleansing Record**.

`[Insert Figure 19: Colon Hydrotherapy Assessment and Treatment Session Form]`

---

#### 6.2.2 Documenting Hydrotherapy Treatment Sessions
- **Feature Name:** Hydrotherapy Session Protocol Log
- **Purpose:** Records procedural parameters during each colon cleansing treatment.
- **Procedure:**
  1. In the colon cleansing form, scroll to **Treatment Sessions**.
  2. Enter the session details:
     - **Session Date & Time**
     - **Water Inflow Volume (Liters)**
     - **Water Pressure Level**
     - **Water Temperature ($^\circ C$)**
     - **Abdominal Massage Applied (Yes/No)**
     - **Waste Matter Characteristics Observed**
     - **Patient Tolerance & Post-Treatment Notes**
     - **Attending Therapist / Nurse Name**
  3. Click **Save Colon Cleansing Record**.
- **Expected Result:** The session data is stored in `colon_cleansing_records` as structured JSON, updating the patient's treatment history.

---

#### 6.2.3 Generating Patient Information & Legal Consent Printouts
- **Feature Name:** Printable Hydrotherapy Documentation
- **Purpose:** Generates physical legal consent agreements and treatment evaluation sheets for the patient's signature.
- **Access:** On the colon cleansing form, click the print action buttons:
  - **Patient Info:** Opens `admin/colon-cleansing/print.php?id=<record_id>&type=info`.
  - **Consent Form:** Opens `admin/colon-cleansing/print.php?id=<record_id>&type=consent`.
- **Procedure:**
  1. Click **Consent Form** to open the legal treatment agreement.
  2. Verify that the pre-printed contraindication disclosures, procedural explanation, risks, and benefits are rendered properly.
  3. Print the document and have the patient sign and date the physical copy.

`[Insert Figure 20: Printable Colon Cleansing Patient Information Sheet and Consent Form]`

---

### 6.3 Equal Diagnostic Laboratory Result Management

#### 6.3.1 Structured Laboratory Templates (Blood Chemistry & Urinalysis)
- **Feature Name:** Equal Diagnostic Structured Lab Templates
- **Purpose:** Provides structured data entry templates with pre-configured clinical reference intervals for clinical laboratory exams.
- **Access:** From an appointment or patient profile in Equal Diagnostic Laboratory (Branch 3), open `admin/lab-results/form.php?appointment_id=<id>&template=<template_key>`.
- **Supported Templates:**
  - `blood_chemistry`: Covers Glucose (FBS), Uric Acid, Urea/BUN, Creatinine, Total Cholesterol, HDL, LDL, VLDL, Triglycerides, SGOT/AST, SGPT/ALT, Sodium, Potassium, Ionized Calcium, Chloride, T3, T4, TSH, Total Protein, Albumin, HbA1c, FT3, and FT4.
  - `urinalysis`: Covers Physical/Chemical Examination (Color, Transparency, Reaction/pH, Specific Gravity, Albumin/Protein, Sugar/Glucose), Microscopic Findings (RBC, Pus Cells, Epithelial Cells, Casts, Crystals, Mucus Threads, Bacteria, Yeast), and Miscellaneous (Pregnancy Test, Lot No., Expiry).

`[Insert Figure 21: Equal Diagnostic Structured Laboratory Result Entry Form (Blood Chemistry / Urinalysis)]`

---

#### 6.3.2 Entering Test Findings, Reference Values & Verifications
- **Feature Name:** Lab Test Data Entry & Clinical Sign-Off
- **Purpose:** Records measured laboratory test values and documents professional review signatures.
- **Procedure:**
  1. Open the structured laboratory form.
  2. Verify patient demographics and enter the **Requesting Physician** name.
  3. Enter measured patient values into the corresponding test parameter fields. Notice that standard clinical reference ranges are displayed alongside each field for easy comparison.
  4. Enter staff sign-offs:
     - **Examined By:** Medical Technologist name.
     - **Validated By:** Senior Medical Technologist / Laboratory Supervisor.
     - **Pathologist:** Consulting Pathologist name.
  5. Select the report status:
     - **Draft:** Work in progress; remains private to laboratory staff.
     - **Completed:** Fully analyzed and verified result; eligible for patient portal release.
  6. Click **Save Laboratory Result**.
- **Expected Result:** The result is saved in `lab_result_sheets`, satisfying the clinical gatekeeper requirement for the associated appointment.

---

#### 6.3.3 Uploading Diagnostic File Attachments (PDF/Images)
- **Feature Name:** Diagnostic File Attachment Repository
- **Purpose:** Stores scanned lab result sheets, ultrasound images, ECG tracings, or external diagnostic reports.
- **Access:** Patient 360 Profile -> Tab 3: Laboratory (`admin/patients/view.php?id=<id>&tab=results`).
- **Procedure:**
  1. Under **Upload Laboratory Result File**, select the associated appointment from the dropdown.
  2. Click **Browse** and select a valid diagnostic document (PDF, JPG, or PNG up to 10 MB).
  3. Enter an optional result title and descriptive remarks.
  4. Check the **Make visible to patient portal** box if the document is ready for patient release.
  5. Click **Upload Result File**.
- **Expected Result:** The file is saved to the secure server directory (`uploads/`), registered in `patient_results`, and displayed in the results table.

---

#### 6.3.4 Publishing Lab Reports to the Patient Portal
- **Feature Name:** Portal Result Publishing Toggle
- **Purpose:** Controls the release of diagnostic reports to the patient portal, ensuring patients only see fully completed and verified findings.
- **Access:** Patient 360 Results Tab or Lab Result Sheet form.
- **Procedure:**
  - **For Structured Lab Sheets:** In `admin/lab-results/form.php`, select **Status: Completed** and check **Publish completed result to Patient Portal**, then click **Save Laboratory Result**. Alternatively, on the patient profile results tab, click the **Portal Visibility** toggle button next to any completed sheet.
  - **For Uploaded Files:** Check or uncheck the portal visibility toggle on the uploaded file row.
- **Expected Result:** When published (`is_visible_to_patient = 1`), the report appears immediately in the patient's personal portal under **My Results**. Unchecking visibility revokes patient access while keeping the file available in administrative records.

---

#### 6.3.5 Printing Official Laboratory Result Sheets
- **Feature Name:** Formal Laboratory Result Sheet Printout
- **Purpose:** Generates official diagnostic report printouts with reference ranges and professional medical signatures.
- **Access:** From the lab form, click **Print Result** or open `admin/lab-results/print.php?id=<result_id>`.
- **Procedure:**
  1. Open `admin/lab-results/print.php?id=<result_id>`.
  2. Verify the printed layout:
     - Equal Diagnostic Laboratory header with official contact numbers.
     - Patient identification block (Patient Code, Name, Age, Sex, Date, Requesting Doctor).
     - Test findings table with test parameter name, observed result, and reference range.
     - Signature lines for Medical Technologist, Reviewing Supervisor, and Pathologist.
  3. Print the document via the browser's native print dialog.

`[Insert Figure 22: Printable Official Laboratory Result Sheet with Reference Ranges and Signatures]`

---

# 7. Inventory & Medical Supply Chain Management

```
+----------------------------------------------------------------------------------------------------+
|                                    INVENTORY TRACKING WORKFLOW                                     |
+----------------------------------------------------------------------------------------------------+
| [Item Added & Minimum Stock Set]                                                                   |
|              |                                                                                     |
|              v                                                                                     |
| [Daily Usage Recorded via Modal] ---------> [Stock Automatically Deducted in Real Time]            |
|                                                              |                                     |
|                                                              v                                     |
|                                              <Automatic Stock Status Evaluation>                   |
|                                              - Current > Minimum: "In Stock" (Green)               |
|                                              - Current <= Minimum: "Low Stock" (Yellow)            |
|                                              - Current = 0: "Out of Stock" (Red)                   |
|                                              - Expiry <= 30 Days: "Expiring" (Orange)              |
|                                                              |                                     |
|                                                              v                                     |
| [Monthly Matrix Compilation] <------------- [Dashboard Alerts Triggered]                           |
+----------------------------------------------------------------------------------------------------+
```

### 7.1 Inventory Catalog, Stock Alerts & Expiry Monitoring
- **Feature Name:** Medical Inventory Management
- **Purpose:** Tracks stock levels of clinic consumables, medicines, vaccines, and diagnostic reagents, with automatic stock status and expiration warnings.
- **Access:** Click **Inventory** in the sidebar navigation or open `admin/inventory/index.php`.
- **Prerequisites:** Authorized staff session.
- **Components:**
  1. **Inventory Summary Metric Cards:**
     - **TOTAL ITEMS:** Total active inventory items registered in the clinic branch.
     - **LOW STOCK:** Items whose quantity is at or below their minimum reorder point.
     - **OUT OF STOCK:** Items with zero quantity remaining.
     - **EXPIRING SOON:** Items expiring within the next 30 days.
  2. **Filtering & Search Bar:**
     - Search by item name, item code, or description.
     - Filter by category (e.g., Medical Supplies, Pharmaceuticals, Laboratory).
     - Filter by status: *In Stock*, *Low Stock*, *Out of Stock*, or *Expiring*.
  3. **Inventory Items Table:**
     - Columns for Item Name, Code, Category, Stock on Hand, Unit of Measure, Unit Price, Status Badge, and Actions.
     - Status badges: `In Stock` (Green), `Low Stock` (Yellow), `Out of Stock` (Red), `Expiring` (Orange).

`[Insert Figure 23: Inventory Management Table with Status Badges and Quick Daily Usage Action]`

---

### 7.2 Adding New Inventory Items & Threshold Configuration
- **Feature Name:** New Inventory Item Intake
- **Purpose:** Enrolls a new medical item or pharmaceutical product into the inventory system.
- **Access:** Click **Add Item** in the inventory screen or open `admin/inventory/add.php`.
- **Procedure:**
  1. Open `admin/inventory/add.php`.
  2. Complete the required item fields:
     - **Item Code:** Unique item code (e.g., `MED-RAB-001`).
     - **Item Name:** Official product or generic name (e.g., *Speeda Rabies Vaccine 0.5mL*).
     - **Category:** Select from *Medical Supplies*, *Laboratory*, *Pharmaceuticals*, *Equipment*, or *Office Supplies*.
     - **Unit of Measure:** Unit designation (e.g., `vial`, `box`, `ampule`, `piece`, `set`).
     - **Current Stock:** Initial physical quantity on hand.
     - **Minimum Stock:** Threshold quantity that triggers a low-stock alert.
     - **Maximum Stock:** Upper storage capacity.
     - **Reorder Point:** Stock level that signals reordering.
     - **Unit Cost / Price:** Purchase cost and selling price per unit.
     - **Supplier Name & Contact:** Vendor contact information.
     - **Expiration Date:** Product expiration date (if applicable).
     - **Storage Location & Notes:** Storage shelf, cabinet, or refrigerator location.
  3. Click **Save Item**.
- **Expected Result:** The item is created in `inventory_items`, categorized, and begins monitoring stock levels automatically.

---

### 7.3 Editing Item Details & Stock Replenishment
- **Feature Name:** Inventory Item Editing & Stock Adjustments
- **Purpose:** Updates item parameters or records stock replenishment deliveries.
- **Access:** Click **Edit** on any inventory item row or open `admin/inventory/edit.php?id=<id>`.
- **Procedure:**
  1. Open `admin/inventory/edit.php?id=<id>`.
  2. To update item details: Modify description, supplier contact, minimum stock threshold, or location, then click **Update Item**.
  3. To record incoming stock replenishment (Stock In):
     - Scroll to **Add Stock / Replenishment**.
     - Enter the quantity received.
     - Select transaction type (*Purchase* or *Adjustment*).
     - Enter batch number, new expiration date, and delivery notes.
     - Click **Save Stock In**.
- **Expected Result:** The item's current stock increases by the entered quantity, its status recalculates, and a record is logged in `inventory_transactions`.

---

### 7.4 Logging Daily Item Consumption via Quick Modal
- **Feature Name:** Quick Daily Usage Logging Modal
- **Purpose:** Enables clinical staff to log used supplies and administered medicines directly from the inventory table without leaving the page.
- **Access:** On `admin/inventory/index.php`, click anywhere on an item's row to open the daily usage modal.
- **Procedure:**
  1. On the inventory table, click on the item you want to record usage for (e.g., *Syringe 3mL*).
  2. The **Record Daily Usage** modal opens displaying:
     - Item Name and Current Stock on hand.
  3. In **Quantity Used Today**, enter the number of units consumed.
  4. The modal dynamically calculates and displays the **Stock After Entry** preview in real time.
  5. Select the usage date (defaults to today).
  6. Enter optional notes (e.g., *"Anti-rabies vaccination Day 0 patients"*).
  7. Click **Save Daily Used**.
- **Expected Result:** An asynchronous AJAX request sends the data to `edit.php`. The system logs the consumption in `inventory_transactions` (`transaction_type = 'Usage'`), deducts the quantity from `current_stock`, updates the item's stock status, and refreshes the table row.
- **Input Validation:** The system prevents negative numbers or quantities exceeding the current stock on hand.

`[Insert Figure 24: Record Daily Usage Modal with Stock-After-Entry Calculation]`

---

### 7.5 Managing Inventory Categories
- **Feature Name:** Inventory Category Management
- **Purpose:** Organizes inventory items into clinical and administrative categories.
- **Access:** Click **Categories** in the inventory header or open `admin/inventory/categories.php`.
- **Procedure:**
  1. Open `admin/inventory/categories.php`.
  2. To create a category: Enter Category Name and Description, then click **Save Category**.
  3. To edit an existing category: Click **Edit**, update the category name or description, and click **Save**.
- **Expected Result:** The updated categories appear immediately in inventory dropdown filters across the system.

---

### 7.6 Monthly Consumption Matrix Report (31-Day Grid & Print)
- **Feature Name:** Monthly Inventory Consumption Matrix
- **Purpose:** Compiles a day-by-day consumption matrix for all inventory items across each day of the month (Days 1 through 31).
- **Access:** Click **Monthly Report** in the inventory header or open `admin/inventory/monthly-report.php`.
- **Procedure:**
  1. Open `admin/inventory/monthly-report.php`.
  2. Select the desired **Month** and **Year** using the dropdown filters.
  3. Filter by category if desired (e.g., view only *Medical Supplies*).
  4. Click **Generate Report**.
  5. Review the comprehensive consumption matrix table:
     - Columns: Item Name, Unit of Measure, Days 1 through 31 (each showing quantity consumed that day), and Total Monthly Consumption.
  6. Click **Print Monthly Matrix** to open a clean print view formatted for landscape documentation and audit review.

`[Insert Figure 25: Monthly Inventory Consumption Matrix Report showing Day-by-Day Item Usage]`

---

# 8. Clinic Administration & Content Management

```
+----------------------------------------------------------------------------------------------------+
|                                  ADMINISTRATIVE CONTROL MODULES                                    |
+-------------------------------------------------+--------------------------------------------------+
| 1. Business Intelligence & Financial Analytics  | 4. Website Services & Online Pricing Catalog     |
|    - Monthly Revenue & Appointment Trends       |    - Service CRUD, Portal Visibility, Thumbnails |
|    - Top Clinical Services & Status Distribution| 5. Website Promotional Packages & Discounts      |
| 2. User & Staff Management (RBAC)               |    - Percentage/Fixed Promos, Expiry Tracking    |
|    - Account Creation & Role Permissions        | 6. Organizational Structure Hierarchy Chart      |
| 3. Clinic Identity, Branding & Theming          |    - Upload Certified Org Chart & Toggle Portal  |
|    - Logo Upload, Address & Dynamic Color Theme | 7. Security Audit Trail & System Activity Logs   |
+-------------------------------------------------+--------------------------------------------------+
```

### 8.1 Clinic Analytics & Business Intelligence Dashboard
- **Feature Name:** Executive Analytics & Reports
- **Purpose:** Provides clinic administrators with real-time operational and financial insights.
- **Access:** Click **Analytics** in the sidebar navigation or open `admin/analytics/index.php`.
- **Prerequisites:** Administrator role (`admin`).
- **Components & Metrics:**
  1. **Date Range Filter:** Select custom start and end dates and click **Apply Filter** to recalculate all metrics. Click **Print** to generate a printed analytics summary.
  2. **Summary Metric Cards:**
     - **Revenue (This Month):** Total revenue calculated from completed appointments and associated service prices.
     - **Appointments (This Month):** Total visits across all statuses.
     - **Total Patients:** Total active patient records in the clinic branch.
     - **Low Stock Items:** Total inventory items requiring reordering.
  3. **Visual Data Visualizations (Chart.js):**
     - **Appointments Trend (Last 6 Months):** Line chart displaying monthly appointment volume trends over the past six months.
     - **Appointments by Status:** Doughnut chart illustrating the distribution of appointments (Completed, Confirmed, Cancelled, Pending).
     - **Top 5 Services:** Horizontal bar chart showing the most frequently requested clinical procedures.
     - **Revenue by Service:** Bar chart ranking clinical services by total revenue generated.

`[Insert Figure 26: Analytics Dashboard featuring Financial Statistics, Trend Charts, and Revenue by Service]`

---

### 8.2 User & Staff Management (RBAC Account Creation & Permissions)
- **Feature Name:** Staff Account & Role Administration
- **Purpose:** Manages staff access credentials, role assignments, and active account statuses.
- **Access:** Click **Users & Staff** in the sidebar or open `admin/users/index.php`.
- **Prerequisites:** Administrator role (`admin`).
- **Procedure:**
  1. Open `admin/users/index.php`.
  2. Review the staff directory table displaying Username, Full Name, Email, Assigned Clinic Branch, Role Badge, and Account Status.
  3. **Creating a New Staff Account:**
     - Click **Add New User** to open `admin/users/add.php`.
     - Enter Username, Work Email, Temporary Password, First Name, Last Name, and Phone Number.
     - Select Role: **admin**, **doctor**, **nurse**, **receptionist**, or **lab_tech**.
     - Click **Create User Account**.
  4. **Modifying an Existing Account:**
     - Click **Edit** on any user row (`admin/users/edit.php?id=<id>`).
     - Update name, contact details, role assignment, or enter a new password if resetting credentials.
     - Toggle the account status between Active and Inactive.
     - Click **Update User**.
- **Expected Result:** The staff account is created or updated, enforcing role-based permissions immediately on next sign-in.

---

### 8.3 Managing Published Clinic Services & Pricing
- **Feature Name:** Clinic Services Directory Management
- **Purpose:** Controls the services displayed to the public and made available for appointment booking.
- **Access:** Click **Services** under the Website section in the sidebar or open `admin/website-content/services.php`.
- **Procedure:**
  1. Open `admin/website-content/services.php`.
  2. Review active services grouped by category with their duration and pricing.
  3. **Add or Edit Service:**
     - Click **Add Service** or click the edit icon on an existing service card.
     - Enter Service Name (e.g., *Complete Blood Count*).
     - Select Category (*Consultation*, *Laboratory*, *Imaging*, *Procedure*, *Package*, *Other*).
     - Enter Base Price in Philippine Pesos (PHP).
     - Enter Duration in minutes (used for scheduling slot calculations).
     - Enter a public description explaining the procedure.
     - Toggle **Active Status** (enables/disables the service clinic-wide).
     - Toggle **Visible in Patient Portal** (controls appearance on public booking screens).
     - Upload an optional service image or thumbnail.
     - Click **Save Service**.
- **Expected Result:** The updated service catalog updates immediately across both the public website and the administrative booking dropdowns.

---

### 8.4 Managing Promotional Packages & Special Discounts
- **Feature Name:** Clinic Promotional Discounts
- **Purpose:** Manages promotional offers, package discounts, and special pricing campaigns.
- **Access:** Click **Promos** in the sidebar or open `admin/website-content/promos.php`.
- **Procedure:**
  1. Open `admin/website-content/promos.php`.
  2. Click **Add Promotion**.
  3. Enter Promotion Title (e.g., *Senior Citizen Diagnostic Wellness Package*).
  4. Enter promotional description and terms and conditions.
  5. Select discount type:
     - **Percentage Discount:** Enter percentage value (e.g., `20.00%`).
     - **Fixed Amount Discount:** Enter flat deduction in PHP (e.g., `₱150.00`).
  6. Set **Start Date** and **End Date** for promotion validity.
  7. Toggle **Featured Promo** to pin the offer prominently on the public homepage.
  8. Click **Save Promotion**.
- **Expected Result:** Active promotions appear in public promotional carousels and become selectable within the appointment booking wizard.

---

### 8.5 Uploading & Publishing Clinic Organizational Charts
- **Feature Name:** Clinic Organizational Chart Management
- **Purpose:** Allows administrators to upload and publish an official organizational structure chart on the clinic website.
- **Access:** Click **Organization** in the sidebar or open `admin/website-content/organizational-chart.php`.
- **Prerequisites:** Administrator role (`admin`).
- **Procedure:**
  1. Open `admin/website-content/organizational-chart.php`.
  2. Under **Upload Organizational Chart**, click **Browse** and select an organizational chart image (PNG, JPG, or WebP; maximum 5 MB).
  3. Check the **Make organizational chart visible on public website** box.
  4. Click **Save Organizational Chart**.
  5. To preview the published chart, click **Preview Public Display**.
  6. To unpublish the chart, uncheck the visibility box, or check **Remove chart image** and save.
- **Expected Result:** When enabled, the organizational chart modal becomes accessible to visitors on `services.php` and the public homepage via `org-chart-image.php`.

---

### 8.6 Clinic Profile, Contacts & Color Theme Settings
- **Feature Name:** Clinic Profile & Visual Theme Settings
- **Purpose:** Configures clinic identity information, official contact numbers, addresses, brand logos, and visual color themes.
- **Access:** Open topbar user menu -> Click **Clinic Settings**, or open `admin/settings.php`.
- **Prerequisites:** Administrator role (`admin`).
- **Procedure:**
  1. Open `admin/settings.php`.
  2. Complete the **Clinic Information** section:
     - Clinic Name and Tagline.
     - Physical Street Address and City/Municipality.
     - Contact Telephone/Mobile Numbers and Official Email Address.
  3. Complete the **Clinic Visual Branding** section:
     - **Primary Color:** Enter a hex color code (e.g., `#0a5c5c`) or use the color picker. Controls topbars, headers, and sidebar backgrounds.
     - **Accent Color:** Enter a hex color code (e.g., `#0fa8a8`). Controls buttons, active highlights, and badges.
     - **Dashboard Background Color:** Enter a hex color code (e.g., `#f4fafa`).
  4. Upload Clinic Official Logo:
     - Select a logo image file (PNG, JPG, or WebP; maximum 2 MB).
     - The logo is automatically converted and stored as an optimized base64 string.
  5. Click **Save Clinic Settings**.
- **Expected Result:** Session branding caches are cleared immediately, and all administrative and public pages update with the newly configured colors, logo, and contact information.

---

### 8.7 System Security, Audit Trail & Activity Logs
- **Feature Name:** Security Audit Trail & Activity Logs
- **Purpose:** Maintains a tamper-evident audit record of all significant actions performed within the system for compliance and security oversight.
- **Access:** Topbar user menu -> Click **Activity Logs**, or open `admin/activity-logs.php`.
- **Prerequisites:** Authorized staff session.
- **Procedure:**
  1. Open `admin/activity-logs.php`.
  2. Filter logs by specific staff user, action keyword (e.g., `LOGIN`, `CONFIRM_APPOINTMENT`, `UPDATE_PATIENT`), or date range.
  3. Inspect audit entries displaying:
     - **Timestamp:** Date and time of action.
     - **Staff Member:** User full name and role badge.
     - **Action Type:** Standardized action identifier.
     - **Description:** Summary of changes made (e.g., *"Confirmed appointment #42 for Complete Blood Count"*).
     - **IP Address & Client Info:** User's device IP and browser user-agent.
- **Expected Result:** Clinical supervisors and auditors can trace every record modification to its exact author, timestamp, and network origin.

---

# 9. Troubleshooting & Frequently Asked Questions (FAQ)

### 9.1 Common Authentication & SMS OTP Questions

**Q: I registered for the Patient Portal but did not receive the SMS verification code (OTP). What should I do?**
- Verify that your mobile number was entered in the correct 11-digit format beginning with `09` (e.g., `09171234567`). Numbers entered with country codes (`+63`) or missing digits will fail validation.
- Check that your mobile device has active cellular reception.
- On `patient-portal/verify-otp.php`, wait for the 60-second cooldown, then click **Resend Verification Code**.
- If the issue persists, contact clinic reception. Staff can verify your phone number and link your portal account manually.

**Q: When logging into the admin portal, the system returns an "Access Denied" or redirects to the login screen.**
- Ensure your caps lock key is off and verify your credentials.
- If your account was recently created, confirm with your clinic administrator that your account status is set to **Active** (`is_active = 1`).

---

### 9.2 Appointment Progression & Clinical Blocker Resolutions

**Q: Why does the system block me from completing an appointment with an error message?**
- The system includes a **Clinical Gatekeeper** feature that prevents appointment closure without required clinical records:
  - **For Rabies Services:** You must create and save a Day 0 Rabies Chart (`admin/rabies/chart.php`) for this patient before completing the visit.
  - **For Colon Hydrotherapy:** You must complete and save the Patient Information & Consent Form (`admin/colon-cleansing/form.php`).
  - **For Equal Diagnostic Laboratory:** You must upload a diagnostic result file or mark a structured laboratory test sheet as `Completed`.
- Once the required clinical document is saved, return to the appointment view and click **Complete Service**.

**Q: Can a declined appointment be reopened?**
- Once declined or cancelled, an appointment cannot transition back to Confirmed. A new appointment should be scheduled using the **New Appointment** button.

---

### 9.3 Inventory & Stock Level Questions

**Q: How do I resolve an item showing "Low Stock" or "Out of Stock"?**
- Navigate to `admin/inventory/edit.php?id=<item_id>`.
- Scroll to **Add Stock / Replenishment**.
- Enter the received quantity, batch number, and expiration date, then click **Save Stock In**. The stock will update immediately.

**Q: Can I enter negative stock or consume more units than currently recorded?**
- No. The system prevents negative stock balances. If physical inventory exceeds system inventory, perform a positive stock adjustment before logging daily usage.

---

### 9.4 SMS Notification Delivery Guidelines

**Q: Which operations automatically send SMS notifications to patients?**
- **Patient Registration:** One-Time Password (OTP) verification code.
- **Appointment Approval:** Confirmation text with appointment date, time, clinic name, and service.
- **Appointment Cancellation:** Notification of cancellation with clinic contact information.
- **Rabies Booster Reminder:** Automated SMS reminder sent one day prior to scheduled Day 3, Day 7, or Day 28 doses.

**Q: What happens if an SMS fails to send due to network issues?**
- The system logs the failure in `sms_notifications` with the error description from the SMS provider. The administrative interface displays a yellow alert: *"SMS was not sent: [error details]"*, but allows clinical and scheduling operations to proceed without interruption.

---

# 10. Document Version & Verification Summary

### 10.1 Implementation Verification Summary
This User Operations Manual was authored through direct static analysis of the MDCMS codebase and verified against production application code:
- **Database Architecture:** Verified against `database_schema.sql` (Tables: `branches`, `users`, `patient_portal_accounts`, `patients`, `sms_notifications`, `appointments`, `inventory_items`, `inventory_transactions`, `rabies_charts`, `colon_cleansing_records`, `lab_result_sheets`, `activity_logs`).
- **Authentication & Security:** Verified against `includes/Auth.php`, `patient-portal/index.php`, and `admin/login.php`.
- **Clinical Workflows:** Verified against `admin/appointments/process-action.php`, `admin/rabies/chart.php`, `admin/colon-cleansing/form.php`, and `admin/lab-results/form.php`.
- **Public & Patient Interfaces:** Verified against `book-appointment.php`, `services.php`, `index.php`, and `patient-portal/dashboard.php`.

### 10.2 Document Revision History

| Version | Date | Primary Author / Role | Summary of Changes |
|---|---|---|---|
| 1.0 | February 2026 | Antigravity AI Systems Documentation | Initial comprehensive user operations manual covering Patient Portal, Administrative Operations, Clinical Gatekeeper, Inventory Matrix, and Specialized Clinical Modules. |

---
*End of User Operations Manual — Medical and Diagnostic Clinic Management System (MDCMS)*

