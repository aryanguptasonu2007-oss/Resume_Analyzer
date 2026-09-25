# ResumeIQ 🚀

### AI-Powered Resume Analyzer & Job Matching System

ResumeIQ is a web-based application that analyzes resumes and helps users understand how well their resume matches a specific job description.

It automatically extracts information from a resume, detects technical skills, evaluates resume quality, compares the resume with job requirements, identifies missing skills, and provides recommendations for improvement.

---

## ✨ Features

- 📄 Upload resumes in **PDF or DOCX** format
- 🔍 Automatically extract resume text
- 🧠 Detect technical skills using an NLP-based skill knowledge base
- 📊 Calculate an overall resume score
- 🎯 Match resumes with specific job descriptions
- 📈 Calculate job matching percentage using **TF-IDF and Cosine Similarity**
- ✅ Identify matching skills
- ❌ Identify missing skills
- 💪 Show resume strengths
- ⚠️ Highlight areas for improvement
- 📋 Provide resume recommendations
- 💻 Clean and responsive user interface

---

## 🛠️ Technologies Used

### Frontend
- React
- Vite
- JavaScript
- HTML
- CSS

### Backend
- Python
- FastAPI

### NLP & Machine Learning
- Scikit-learn
- TF-IDF
- Cosine Similarity
- Rule-based skill extraction

### Resume Processing
- PyMuPDF
- python-docx

---

## 🏗️ System Architecture 

```
                 ┌─────────────────────┐
                 │      User           │
                 │ Upload Resume +     │
                 │ Job Description     │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   React Frontend    │
                 │     + Vite          │
                 └──────────┬──────────┘
                            │
                         REST API
                            │
                            ▼
                 ┌─────────────────────┐
                 │    FastAPI Backend  │
                 └──────────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
        Resume Parser   Skill Analyzer   Resume Analyzer
              │             │             │
              └─────────────┼─────────────┘
                            ▼
                 ┌─────────────────────┐
                 │   Job Matcher       │
                 │ TF-IDF + Cosine     │
                 │    Similarity       │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Analysis Results  │
                 │                     │
                 │ Score               │
                 │ Job Match           │
                 │ Skills              │
                 │ Missing Skills      │
                 │ Strengths           │
                 │ Improvements        │
                 └─────────────────────┘

```
### Project Structure
```
resumeiq/
│
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
│
├── backend/
│   ├── main.py
│   ├── resume_parser.py
│   ├── skill_analyzer.py
│   ├── analyzer.py
│   ├── matcher.py
│   ├── skills.json
│   └── requirements.txt
│
├── public/
├── package.json
├── vite.config.js
└── README.md
