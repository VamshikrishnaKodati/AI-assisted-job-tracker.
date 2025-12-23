# 🤖 AI-Assisted Job Tracker

An AI-assisted web application that helps job seekers automatically match, track, and manage job applications using resume parsing and intelligent job ranking.

This project focuses on **AI-assisted decision support**, not blind automation, keeping the system explainable, reliable, and user-controlled.

---

## 📌 Problem Statement

Job searching today is manual, repetitive, and inefficient—especially for freshers and early-career professionals.

Common challenges include:
- Searching multiple job portals daily
- Applying to irrelevant jobs
- No clear insight into job–skill match
- Poor tracking of applications and interview progress
- Difficulty understanding skill gaps

---

## 🎯 Solution Overview

The AI-Assisted Job Tracker acts as a **personal job assistant** that:
- Parses resumes to extract skills
- Matches jobs using AI-assisted similarity scoring
- Ranks jobs by relevance
- Tracks applications in an ATS-style dashboard

AI is used as a **support tool**, while final decisions remain with the user.

---

## 🧠 Key Features (MVP)

- Resume upload and skill extraction
- Job relevance scoring (0–100%)
- Rule-based filtering (location, experience)
- Ranked job dashboard
- Application status tracking (Applied / Interview / Offer)

---

## 🏗️ System Architecture (MVP)
React Frontend
↓ REST API
FastAPI Backend
↓
AI Logic (Resume Parsing & Matching)
↓
PostgreSQL Database

---

## 🧰 Tech Stack

- **Frontend:** React
- **Backend:** FastAPI (Python)
- **Database:** PostgreSQL
- **AI/NLP:** Resume parsing & text similarity
- **Auth:** JWT-based authentication

---

## 📂 Project Structure

ai-assisted-job-tracker/
├── frontend/
├── backend/
├── docs/
│ ├── 01-idea.md
│ ├── 02-architecture.md
│ ├── 03-ai-design.md
│ └── interview-notes.md
└── README.md

---

## 🚧 Project Status

🟡 MVP in progress  
- [x] Idea & architecture design  
- [ ] Resume parsing module  
- [ ] Job matching logic  
- [ ] Dashboard UI  
- [ ] Cloud deployment  

---

## 🎓 Learning Outcomes

- AI-assisted full stack development
- Resume parsing and NLP basics
- Backend API design with FastAPI
- Explainable system architecture
- Using AI responsibly in real projects

---

## 📣 Interview Pitch (One Line)

> “I built an AI-assisted job tracking system that parses resumes, ranks jobs using NLP-based similarity scoring, and tracks applications through an ATS-style dashboard, with full end-to-end documentation.”

