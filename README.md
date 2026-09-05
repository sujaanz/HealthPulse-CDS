# 🩺 HealthPulse (MediCase System)

### Smart Case-Taking & Clinical Decision Support (CDS) System

> **HealthPulse** is an advanced, ABDM-compliant Electronic Health Record (EHR) and Clinical Decision Support platform engineered for modern Outpatient Departments (OPDs). It bridges the gap between traditional clinical workflows and modern AI-driven healthcare intelligence.


## 🏗️ System Architecture & Workflow

The platform is built on a decoupled, modular architecture designed for high availability and low latency:

```text
 ┌────────────────────────┐         ┌────────────────────────┐         ┌────────────────────────┐
 │   Frontend (Next.js)   │ <-----> │   Backend (FastAPI)    │ <-----> │ Database / Local Store │
 │   - Role-Based UI      │         │   - Clinical Analysis  │         │   - Patient Records    │
 │   - Multilingual Rx    │         │   - ICD-11 & CDS Logic │         │   - Secure Audit Logs  │
 └────────────────────────┘         └────────────────────────┘         └────────────────────────┘

```

* **Frontend Tier:** Developed using **Next.js (React)** and styled with **Tailwind CSS**, delivering a lightning-fast, responsive user experience.
* **Backend Tier:** Powered by **Python FastAPI**, handling clinical safety checks, NLP keyword extraction, and automated decision-support logic.
* **Data Layer:** Secure state persistence combining robust client-side storage with encrypted session handling.

---

## ✨ Core Features & Modules

### 1. Multi-Role Access Control

* **Doctor Dashboard:** Real-time OPD queue sorting, live vitals management, and structured clinical case-taking.
* **Patient Portal:** Comprehensive medical history timeline, ABHA digital health card generation, and prescription downloading.
* **Admin Console:** Tamper-proof audit log tracking, role-based permission management, and system-wide configuration controls.

### 2. AI & Clinical Decision Support (CDS)

* **Automated Triage (NEWS2):** Real-time risk stratification (Stable, Moderate, Critical) based on patient vitals.
* **Differential Diagnosis Engine:** Suggests probable conditions mapped directly to **ICD-11** and **SNOMED CT** standards.
* **Safety Protocols:** Automated drug-allergy contraindication checks and weight-adjusted pediatric dosage calculations.
* **Pulmonary Vision:** AI-assisted chest X-ray scanning simulation for rapid thoracic analysis.

---

## 🛠️ Tech Stack

* **Frontend:** Next.js, React, Tailwind CSS, Lucide React Icons
* **Backend:** Python, FastAPI, Uvicorn, Pydantic
* **AI & Utilities:** Web Speech API, QRCodeSVG (Digital ID rendering)
* **Standards Compliance:** ABDM (Ayushman Bharat Digital Mission), FHIR R4 Interoperability

---

## 🚀 Getting Started & Installation

### Prerequisites

* Node.js (v18 or higher)
* Python (v3.9 or higher)

### 1. Backend Setup (Python FastAPI)

1. Navigate to your backend directory (or create a backend folder):
```bash
cd backend

```


2. Create and activate a virtual environment:
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

```


3. Install required Python packages:
```bash
pip install fastapi uvicorn pydantic axios

```


4. Run the backend server:
```bash
uvicorn main:app --reload --port 8000

```


*The backend will be live at `http://localhost:8000`.*

### 2. Frontend Setup (Next.js)

1. Open a new terminal and navigate to the frontend directory:
```bash
cd frontend

```


2. Install frontend dependencies:
```bash
npm install

```


3. Run the development server:
```bash
npm run dev

```


*Access the application in your browser at `http://localhost:3000`.*

---

## 🔑 Demo Access Credentials

| Role | Email Address | Password |
| --- | --- | --- |
| **Doctor** | `dr.ananya@healthpulse.com` | `doctor123` |
| **Patient** | `priya.das@healthpulse.com` | `patient123` |
| **Admin** | `admin@healthpulse.com` | `admin123` |

---

## 🎯 Future Roadmap

* [ ] Migration from local storage to **MongoDB Atlas / PostgreSQL** cloud database.
* [ ] Implementation of **JWT Authentication** and password encryption (Bcrypt).
* [ ] Automated **WhatsApp & SMS push notifications** for medication alarms and follow-ups.
