RecruitAI - Automated Resume Screening & Candidate Shortlisting System
ReactTypeScriptViteTailwindCSSGoogle Gemini

An AI-powered web application designed for HR departments, recruiters, and talent acquisition teams to scan, parse, evaluate, score, and shortlist candidate resumes against customizable job specifications using NLP (Natural Language Processing) algorithms and Large Language Models (LLMs).

🔥 Key Features
1. 📄 Multi-Format Resume Parser & Bulk Importer
Format Support: Direct browser parsing for PDF, DOCX, and TXT files using pdfjs-dist and mammoth.
Entity Extraction: Automatically extracts candidate names, contact details, years of experience (YOE), education levels, and explicit technical skills.
Sample Candidate Pool: Includes a one-click loader with pre-configured realistic candidate resumes across Engineering, Product, and Data Science.
2. 🧠 Hybrid NLP & LLM Evaluation Engine
TF-IDF & Cosine Similarity: Computes text similarity overlap between job descriptions and resume contents.
Skill Matrix Matching: Evaluates mandatory core skills vs optional preferred skills with synonym detection (React ↔ React.js, Python ↔ Python3, LLM ↔ Large Language Models).
Experience & Education Scoring: Evaluates years of experience against target requirements and assesses degree levels (Bachelor's, Master's, Ph.D.).
Red Flag Detector: Identifies missing core mandatory skills and experience deficits.
Optional Google Gemini API: HR managers can supply a Gemini API Key to run qualitative AI evaluations, executive summaries, and custom interview questions.
3. 📊 Shortlist Dashboard & Analytics
Fit Score Badges: Displays match percentage (0–100%) and shortlisting status (Top Shortlist, Strong Match, Potential Match, Unsuitable).
Search & Filtering: Search by name, role, or skill; filter by shortlist status; sort by Fit Score, Experience, or Alphabetical.
Visual Analytics: Interactive Recharts visualizations including score distribution histograms and core skill coverage radar charts.
4. 🔍 Deep-Dive Resume Inspector & Keyword Highlighter
Color-Coded Highlights: View resume text with matched skills highlighted in emerald green and missing core requirements in rose red.
Score Breakdown: Inspect granular sub-scores (Skill Fit %, Experience Match %, Education Fit %, Cosine Similarity %).
AI Interview Questions: Tailored technical and behavioral questions generated specifically for the candidate's profile.
5. ⚖️ Side-by-Side Candidate Comparison Matrix
Compare up to 4 candidates side-by-side across key metrics (Match Score, YOE, Education, Core Skill Coverage, Key Strengths, Actions).
6. ⚙️ Customizable HR Scoring Weights & Policy
Tune relative weight sliders:
Technical Skills Fit Weight (default: 40%)
Years of Experience Weight (default: 30%)
Education & Degree Level Weight (default: 15%)
NLP Keyword Overlap Weight (default: 15%)
Auto-Shortlist Score Cutoff Threshold (default: 75%)
7. ✉️ Automated Candidate Outreach & Exporter
Email Generator: Auto-generate personalized Interview Invitations or Polite Rejection emails with 1-click clipboard copy.
Export Options: Export shortlisted candidate records to CSV or JSON.
🛠️ Tech Stack & Libraries
Frontend: React 19 + TypeScript + Vite
Styling: Tailwind CSS v4 + Lucide React Icons + Glassmorphism UI
Data Visualization: Recharts
Document Extractors: pdfjs-dist (PDF text extraction), mammoth (DOCX extraction)
AI / NLP: Direct REST integration with Google Gemini API (gemini-2.5-flash) + Custom TF-IDF Cosine Similarity Engine
🚀 Quick Start Guide
Prerequisites
Node.js (v18+)
npm or yarn
Installation Steps
Clone or Extract Repository:

bash

git clone <repository-url>
cd LLM
Install Dependencies:

bash

npm install
Start Development Server:

bash

npm run dev
Open your browser and navigate to: 👉 http://localhost:5173/

Build for Production:

bash

npm run build
📂 Project Architecture

LLM/
├── src/
│   ├── components/
│   │   ├── Navbar.tsx                # Header, job switcher, tab navigation, action buttons
│   │   ├── JobRequirementForm.tsx    # Job specification builder & template loader
│   │   ├── ResumeUploader.tsx        # Drag & drop upload & sample loader
│   │   ├── Dashboard.tsx             # Candidate shortlist grid & toolbar
│   │   ├── CandidateCard.tsx         # Score card widget with quick actions
│   │   ├── CandidateDetailModal.tsx  # Deep-dive inspector with keyword highlighter
│   │   ├── CandidateComparison.tsx   # Side-by-side candidate comparison matrix
│   │   ├── WeightingSettings.tsx     # HR weight slider controls & shortlist cutoff
│   │   ├── EmailGeneratorModal.tsx   # Automated outreach email builder
│   │   └── AnalyticsCharts.tsx       # Recharts bar & radar charts
│   ├── types/
│   │   └── resume.ts                 # TypeScript interfaces for Job, Candidate, Score, Evaluation
│   ├── utils/
│   │   ├── nlpEngine.ts              # Core NLP TF-IDF, Cosine Similarity & Skill Matcher
│   │   ├── geminiApi.ts              # Google Gemini LLM API integration helper
│   │   ├── fileParsers.ts            # PDF, DOCX, and TXT browser extractors
│   │   ├── mockData.ts               # Pre-populated job specifications & sample resumes
│   │   └── exportUtils.ts            # CSV & JSON exporter helpers
│   ├── App.tsx                       # Main state container
│   ├── main.tsx                      # Application entry point
│   └── index.css                     # Tailwind CSS & glassmorphism theme
├── package.json
├── vite.config.ts
└── README.md
💡 How to Use
Select or Create a Job Profile:

Use the top dropdown to switch between active job roles (Senior Full Stack AI Engineer, Product Manager, Data Scientist) or click Edit Job Profile to build a custom job description.
Upload Resumes:

Drag & drop PDF/DOCX/TXT files into the upload area or click Load Sample Candidate Pool for instant evaluation.
Inspect Candidates:

Click Resume & Analysis on any candidate card to view sub-scores, executive summary, strengths/gaps, and color-coded resume keyword highlights.
Compare Candidates:

Click the scale icon on 2 to 4 candidates to open the Side-by-Side Matrix.
Tune HR Weightings:

Click HR Weights to adjust score weights according to your hiring policy.
Outreach & Export:

Click the mail icon to generate personalized outreach emails or click Export Shortlist to download candidate data in CSV/JSON format.
📜 License
This project is open-source and available under the 
MIT License
.
