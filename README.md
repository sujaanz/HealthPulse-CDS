---

# HealthPulse / MediCase • Smart Case Taking & Clinical Decision Support (CDS) System

HealthPulse is an advanced, ABDM-compliant Electronic Health Record (EHR) and Clinical Decision Support system designed to streamline OPD case-taking, triage stratification, and multilingual prescription workflows for modern healthcare institutions.

---

## 🏗️ System Architecture & Workflow

The application follows a modern decoupled architecture:

```text
 ┌────────────────────────┐         ┌────────────────────────┐         ┌────────────────────────┐
 │   Frontend (Next.js)   │ <-----> │   Backend (FastAPI)    │ <-----> │ Database / Local Store │
 │   - Role-Based UI      │         │   - Clinical Analysis  │         │   - Patient Records    │
 │   - Multilingual Rx    │         │   - ICD-11 & CDS Logic │         │   - Secure Audit Logs  │
 └────────────────────────┘         └────────────────────────┘         └────────────────────────┘

```

1. **Client Tier (Frontend):** Built with Next.js (React) and Tailwind CSS, featuring role-based dashboards for Doctors, Patients, and Administrators.
2. **Service Tier (Backend / AI Mock):** Handles clinical keyword parsing, safety checks (drug-allergy interactions), and medical intelligence processing.
3. **Data Tier:** LocalStorage persistence combined with secure state management for seamless offline/online clinical operations.

---

## ✨ Key Features

* **Multi-Role Portal:** Separate tailored dashboards for Doctors, Patients, and System Administrators.
* **Smart Case-Taking & Triage:** NEWS2-based automated triage stratification (Stable, Moderate, Critical) alongside voice dictation and speaker diarization.
* **Multilingual Prescriptions:** Real-time prescription generation and text-to-speech reading in Bengali (বাংলা), Hindi (हिन्दी), and English.
* **Clinical Safety & CDS:** Automated checks for drug-allergy contraindications and pediatric dose calculations.
* **ABDM / ABHA Compliance:** Integrated digital health ID card views, QR kiosk fast-track check-ins, and FHIR R4 interoperability formatting.

---

## 🚀 Getting Started & Installation

### Prerequisites

* Node.js (v18 or higher)
* Python (v3.9 or higher, optional for backend services)

### Frontend Setup

1. Clone the repository and navigate to the project directory:
```bash
cd frontend

```


2. Install dependencies:
```bash
npm install

```


3. Run the development server:
```bash
npm run dev

```


4. Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔑 Demo Access Credentials

* **Doctor Portal:** `dr.ananya@healthpulse.com` | Password: `doctor123`
* **Patient Portal:** `priya.das@healthpulse.com` | Password: `patient123`
* **Admin Console:** `admin@healthpulse.com` | Password: `admin123`
