
# 🏗️ MVP Architecture – AI-Assisted Job Tracker

This document describes the **high-level architecture** of the AI-Assisted Job Tracker MVP.  
The goal is to keep the system **simple, modular, and easy to explain in interviews**, while still being realistic and production-oriented.

---

## 🎯 Architecture Goals

- Simple and modular design
- Easy to explain to recruiters and interviewers
- AI used only where it adds real value
- Clear separation between frontend, backend, AI logic, and database

---

## 🧱 High-Level Architecture

```

React Frontend
↓  (REST APIs)
FastAPI Backend
↓
AI Processing Layer
↓
PostgreSQL Database

```

### Overview

- **Frontend** handles user interaction and UI
- **Backend** manages APIs, authentication, and business logic
- **AI layer** assists with resume parsing and job matching
- **Database** stores users, resumes, jobs, and applications

---

## 🖥️ Frontend – React

### Responsibilities

- User authentication (Login / Register)
- Resume upload (PDF)
- Display ranked job matches
- Track application status

### Key Pages

- Login / Register
- Resume Upload
- Job Match Dashboard
- Application Tracker (Applied / Interview / Offer)

### Why React?

- Component-based architecture
- Fast development and scalability
- Industry-standard frontend framework

---

## ⚙️ Backend – FastAPI

### Responsibilities

- Expose REST APIs
- Handle authentication using JWT
- Accept and process resume uploads
- Execute AI matching logic
- Communicate with the database

### Core API Modules

```

/auth          → login, register
/resume        → upload and parse resume
/jobs          → store and fetch job data
/matching      → calculate job match score
/applications  → track application status

````

### Why FastAPI?

- High performance
- Clean and readable code
- Automatic API documentation (Swagger / OpenAPI)

---

## 🤖 AI Processing Layer (Inside Backend)

AI is **not a separate microservice** in the MVP.  
It runs inside the backend as a **logical processing layer** to keep the system simple and explainable.

---

### 1️⃣ Resume Parsing

The system extracts structured information from uploaded resumes:

- Skills
- Education
- Experience level

**Example Output:**

```json
{
  "skills": ["Python", "SQL", "Power BI"],
  "experience": "Fresher"
}
````

---

### 2️⃣ Job Description Processing

* Clean and normalize job description text
* Extract required skills
* Convert text into embeddings to capture semantic meaning

---

### 3️⃣ Job Matching Logic (Explainable)

#### Step 1: Rule-Based Filtering

* Location
* Experience level
* Job type

#### Step 2: AI-Based Scoring

* Compare resume data with job descriptions
* Generate a **match score (0–100%)**

> AI ranks jobs, but the final decision is always made by the user.

---

## 🗄️ Database – PostgreSQL

### Main Tables

#### users

* id
* name
* email
* password_hash

#### resumes

* user_id
* skills
* raw_text

#### jobs

* company
* role
* location
* description

#### applications

* user_id
* job_id
* status
* notes

### Why PostgreSQL?

* Reliable and production-ready
* Strong relational structure
* Easy to query and scale

---

## 🔁 End-to-End Data Flow

```
User uploads resume
        ↓
Backend parses resume (AI)
        ↓
Jobs fetched from database
        ↓
Rule-based filtering
        ↓
AI match score calculation
        ↓
Ranked jobs sent to frontend
        ↓
User tracks applications
```

---

## 🔐 Security (MVP Level)

* Password hashing
* JWT-based authentication
* Resume file type validation
* Secrets managed using environment variables

---

## 🎤 Interview Explanation (Quick Pitch)

> “I designed a simple full-stack architecture where React handles the UI, FastAPI manages APIs and security, and AI is used only for resume parsing and job ranking. I apply rule-based filters first and then use AI for scoring, which keeps the system reliable and explainable.”

---

## 📌 Why This Architecture Works for an MVP

* Easy to implement and maintain
* Easy to extend in future
* AI is controlled, not overused
* Clear and understandable for recruiters

---

## 🚀 Next Steps

* Implement resume parsing logic
* Build job matching algorithm
* Create FastAPI backend skeleton
* Design React dashboard UI

```

---

## ✅ What you should do NOW

1. Paste this into `docs/02-architecture.md`
2. Commit with message:
```

Add MVP architecture documentation

```
3. Push to GitHub

---

## 🔥 You are doing this the RIGHT way

This repo now shows:
- Product thinking
- System design skills
- AI maturity
- Professional documentation


