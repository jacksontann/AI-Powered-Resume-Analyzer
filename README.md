# AI Powered Resume Analyzer

A full-stack web application that analyzes resumes using multiple AI providers and delivers detailed, section-by-section feedback to help users improve their chances of landing a job.

## Overview

Upload your resume and get instant feedback powered by OpenAI, Google Gemini, or a fully local AI model via Ollama — no data stored, no subscriptions required. The app evaluates your resume across multiple sections, scores it, checks ATS compatibility, and suggests roles that better match your profile.

## Features

- Multi-AI Support: Choose between OpenAI GPT, Google Gemini, or local Ollama models
- Section-by-Section Feedback: Detailed analysis across 8+ resume sections
- Smart Scoring: Weighted scoring that prioritizes work experience and projects
- ATS Compatibility Check: See how well your resume performs against applicant tracking systems
- Role Matching: Get suggestions for roles that better fit your background
- File Support: Upload PDF or DOCX files
- PDF Preview: Side-by-side resume viewer while reviewing feedback
- History: Save and revisit past analyses anytime

## Privacy & Security

- No data is stored on any server
- When using Ollama, everything runs locally on your machine — fully offline
- When using OpenAI or Gemini, only the resume text is sent to their APIs
- Analysis history is stored in your browser (localStorage) and can be cleared anytime
- API keys are never saved and are wiped on page refresh

## Prerequisites

- Python 3.9+
- Node.js 18+
- Ollama (optional, for local AI)

## Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/jacksontann/AI-Powered-Resume-Analyzer.git
cd AI-Powered-Resume-Analyzer
```

### 2. Backend

```bash
cd backend

# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start the server
uvicorn main:app --host 0.0.0.0 --port 8000
```

### 3. Frontend

```bash
cd frontend

npm install
npm run dev
```

Open http://localhost:3000 in your browser.

### 4. Local AI (Optional)

To use Ollama for fully offline analysis:

```bash
# Install Ollama from https://ollama.ai
ollama pull qwen2.5:14b
```

Then select **Local (Ollama)** as the AI provider in the app.

## License

This project is licensed under the MIT License.
