# Land-Registration-Project
A secure, geo-enabled Land Registration Management Information System (LRMIS) built with FastAPI and MongoDB to track land applications, manage geospatial parcels, and coordinate field surveys.
# Land Registration Management Information System (LRMIS)

LRMIS is a secure, geo-enabled platform designed to manage land registration, validate property ownership records, track surveyor tasks, and handle official land certificate issuance[cite: 5]. 

Instead of simple document uploads, this system enforces a strict legal workflow, checks ownership data, supports geospatial parcel mapping using GeoJSON, and maintains immutable audit logs[cite: 5].

---

## 🛠️ Technology Stack
- **Backend:** FastAPI (Python)[cite: 5]
- **Database:** MongoDB + PyMongo (utilizing 2dsphere spatial indexes)[cite: 5]
- **Frontend:** Streamlit / React / Vue / Angular[cite: 5]
- **Maps:** OpenStreetMap + Leaflet[cite: 5]

---

## 👥 Team & Responsibilities

Our team consists of three developers, each responsible for a core module of the system[cite: 5]:

### 1. Land Application Management — Huthefa Abuznaid
* Implements CRUD operations, pagination, and sorting for land applications[cite: 5].
* Enforces the core state machine workflow: `submitted` ➡️ `pre_checked` ➡️ `survey_required` ➡️ `surveyed` ➡️ `legal_review` ➡️ `approved` ➡️ `certificate_issued` ➡️ `closed`[cite: 5].
* Manages parcel details with GeoJSON and records application events in performance logs[cite: 5].

### 2. Applicant Portal & Profiles — Osama Bairate
* Manages profiles for citizens, lawyers, companies, and surveyors[cite: 5].
* Enables applicants to submit applications, upload supporting documents, track status timelines, and submit objections[cite: 5].
* Integrates notification stubs (Email/SMS simulation)[cite: 5].

### 3. Surveyors, Registrar & Assignment — Shouibe Awidate
* Manages surveyor profiles, schedules, coverage zones, and workload metrics[cite: 5].
* Implements an automatic surveyor assignment engine based on location matching, availability, and active workload[cite: 5].
* Tracks field survey milestones and handles registrar review actions[cite: 5].

### 4. Interactive Map & Analytics Dashboard (Joint Collaboration)
* Built a live map using OpenStreetMap and Leaflet to display parcel boundaries, pending applications, and surveyor tasks[cite: 5].
* Developed real-time business dashboards tracking KPI metrics like backlog, average processing time, and surveyor workloads using MongoDB aggregation pipelines[cite: 5].

---

## 🔄 System Workflow

1. **Submission:** An applicant uploads documents and specifies their parcel coordinates on a map[cite: 5].
2. **Pre-Check:** Land authority staff verify applicant details and paperwork[cite: 5].
3. **Field Survey:** The system auto-assigns a surveyor based on zone and availability[cite: 5]. The surveyor conducts a physical check and uploads report metadata[cite: 5].
4. **Legal Review & Approval:** The registrar reviews the legal documentation, handles any third-party objections, and grants approval[cite: 5].
5. **Certification & Closure:** The system generates ownership certificate metadata with a QR verification code, and closes the request[cite: 5].
Team Member
Huthefa Abuznaid – Land Application Management  Osama Bairate – Applicant Portal & Profiles  Shouibe Awidate – Surveyors, Registrar & Assignment  
