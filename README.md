---

# Apollo HR Automation & Careers Page

**AI-powered candidate screening, centralized application intake, and automated HR workflows**

This repository contains the **prototype implementation** of Apollo’s HR Automation System and Careers Page workflow, designed to streamline the hiring process, reduce manual workload, and provide a more professional candidate experience.

---

## 📌 Project Overview

This project replaces the old Outlook-based application intake (applications arriving randomly by email) with a **centralized careers page** where candidates can browse open positions, read descriptions, and submit their applications directly.

Once an application is submitted:

1. The workflow triggers automatically
2. Candidate data is extracted and stored
3. AI-powered evaluation is performed
4. HR receives structured results
5. Candidate is processed through the next stages

The system is fully functional as a **prototype**, and requires production-level configurations before deployment.

---

## 🧩 Key Components

### **1. Careers Page**

A simple, clean page where candidates can:

* View all open positions
* See role descriptions
* Submit applications directly
* Trigger the automation instantly

This page can be deployed on:
`careers.apollo-gs.com`

---

### **2. HR Automation Workflow (n8n)**

The hiring workflow performs:

#### **Application Intake**

* Triggers on new form submission
* Extracts CV + candidate information
* Stores files in structured directories

#### **AI-Powered Screening**

* CV parsing
* Candidate scoring
* Role fit evaluation
* Summary generation
  (Current prototype uses OpenAI GPT-4o-mini)

#### **Database Update**

* Sends structured candidate data to Notion

#### **Notification Flow**

* Sends summary + next steps to HR
* Organizes candidate progress

---

## 🛠️ Tools & Integrations Used

| Component                     | Purpose                            |
| ----------------------------- | ---------------------------------- |
| **n8n**                       | Workflow automation engine         |
| **Career Page**               | Candidate interface                |
| **Google Drive (prototype)**  | Temporary file storage             |
| **Notion**                    | Candidate tracking database        |
| **OpenAI API (prototype)**    | AI evaluation & scoring            |
| **Microsoft Teams**           | Interview scheduling notifications |

> ⚠️ **Note:** Production deployment should use

* Internal or open-source AI models (Ollama, Llama, etc.)
* Secure storage such as AWS S3
* Company-managed Notion authentication
* Dedicated n8n instance
  For compliance + privacy.


## ⚙️ Deployment Requirements (Production)

Before going live, these adjustments are required:

### **Storage**

Replace Google Drive → **AWS S3** or internal storage.

### **AI Models**

Replace OpenAI → **self-hosted or open-source** AI models:

* Llama 3
* Mixtral
* Qwen2
* Local inference via Ollama or AWS Bedrock

### **Authentication**

Use secure company credentials, not temporary tokens.

### **Hosting**

* Deploy career page on **careers.apollo-gs.com**
* Host workflow on a secure n8n instance
* Add HTTPS + DNS routing

---

## 📊 Workflow Diagram (High-Level)

```
Candidate → Careers Page → Submit Form
    ↓
Trigger Workflow (n8n)
    ↓
CV + Data Extraction
    ↓
AI Evaluation & Scoring
    ↓
Store Candidate Data (Notion)
    ↓
Notify HR
    ↓
Set Next Steps (Interview, Rejection, Hold)
```

---

## 🗒️ Notes for Developer Team

This prototype demonstrates:

* End-to-end automation
* AI evaluation with structured scoring
* Full replacement for email-based intake
* A scalable workflow design

What remains:

* Deployment configuration
* Secure storage and AI hosting setup
* Final UI design for the careers page

---

## 🙋‍♂️ Author

**Furkan Çinko**
Process Automation & AI Intern
Apollo Green Solutions
2025

---


