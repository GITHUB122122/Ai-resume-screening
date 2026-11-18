# AI Resume Screening & Applicant Tracking System

An AI-powered recruitment automation workflow built using **n8n, Google Gemini, Google Drive, Google Docs, Google Sheets, and Gmail**. The system automates resume collection, candidate information extraction, AI-based evaluation, applicant classification, and email notifications.

## 🚀 Project Overview

This project streamlines the initial recruitment process by automatically processing job applications and evaluating candidates against a job description.

When a candidate submits the application form with their resume, the workflow extracts relevant information, generates a candidate summary, evaluates their suitability using Google Gemini AI, and assigns an application status based on the evaluation score.

## ⚙️ Workflow

1. **Application Submission:** Candidates submit their personal details and PDF resume through an n8n form.
2. **Resume Upload:** The uploaded resume is stored in Google Drive.
3. **Information Extraction:** Google Gemini extracts personal and professional details, including education, skills, experience, contact information, and job history.
4. **Candidate Summarization:** Extracted information is combined and converted into a structured candidate profile summary.
5. **Job Description Retrieval:** The workflow retrieves the relevant job description from Google Docs.
6. **AI Evaluation:** Google Gemini compares the candidate profile against the job requirements and generates a suitability score and evaluation.
7. **Candidate Classification:** Based on the score, candidates are automatically categorized:
   - **Shortlisted:** Score above 7
   - **Maybe:** Score from 5 to 7
   - **Ignored:** Score below 5
8. **Applicant Tracking:** Candidate details, scores, status, and AI assessments are stored in Google Sheets.
9. **Email Notifications:** Gmail automatically sends status-based email notifications to candidates.

## 🛠️ Technologies Used

- **n8n** – Workflow automation
- **Google Gemini AI** – Resume information extraction, summarization, and candidate evaluation
- **Google Drive** – Resume storage
- **Google Docs** – Job description storage
- **Google Sheets** – Applicant tracking and evaluation records
- **Gmail** – Automated candidate notifications

## 📋 Requirements

- n8n account or self-hosted n8n instance
- Google account
- Google Gemini API key
- Google Drive, Google Docs, Google Sheets, and Gmail access

## 🔧 Setup Instructions

1. Clone or download this repository.
2. Open your n8n instance.
3. Import `AI-Resume-Screening-Workflow.json`.
4. Configure your own Google Gemini credentials.
5. Connect your Google Drive, Google Docs, Google Sheets, and Gmail accounts.
6. Replace the placeholder Google Drive folder ID, Google Docs document ID, and Google Sheets document ID with your own IDs.
7. Configure the job description in Google Docs.
8. Save and activate the workflow.
9. Open the generated n8n form URL and submit a test application.

## 📊 Applicant Classification

| Evaluation Score | Application Status |
|---|---|
| Above 7 | Shortlisted |
| 5–7 | Maybe |
| Below 5 | Ignored |

## 🔒 Security & Privacy

- API credentials and account connections are not included in this repository.
- Configure your own credentials inside n8n.
- Do not upload real candidate resumes, personal information, API keys, or credentials to a public repository.
- AI-generated evaluations should be reviewed by a human recruiter before making hiring decisions.

## 📌 Future Improvements

- Support for multiple job openings.
- Improved candidate ranking and filtering.
- Recruitment analytics dashboard.
- Interview scheduling automation.
- Human review and approval before sending candidate decisions.

---

**Note:** This project is intended to automate and assist the initial resume screening process. AI-generated scores and classifications should support, not replace, human recruitment decisions.
