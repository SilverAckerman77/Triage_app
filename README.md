# 🏥 Triage AI Navigator  
**Multimodal Clinical Decision Support for Rural Healthcare**

---

## 📌 Overview

**Triage AI Navigator** is a Streamlit-based clinical decision support system designed to assist **rural healthcare workers** in early patient triage when specialist access is limited.

The system combines:
- **Vital sign trend analysis**
- **Rule-based clinical thresholds**
- **Guided triage workflow**
- **QR-based clinician handoff**

to provide a **defensible, explainable care pathway** rather than a black-box diagnosis.

Developed for **GRASP 2026**.

---

## 🎯 Problem Statement

Rural and semi-urban healthcare settings often face:
- Shortage of medical specialists
- Delayed escalation of deteriorating patients
- Lack of continuous vital trend monitoring
- Poor handoff between first responders and clinicians

This leads to **missed early warning signs** and **avoidable complications**.

---

## 💡 Solution

Triage AI Navigator acts as a **clinical bridge** by:
- Tracking vital sign trends over time
- Detecting early deterioration using slope-based analysis
- Flagging red-zone clinical thresholds
- Routing patients to the correct specialist
- Generating QR-based summaries for clinician review

⚠️ The system **does NOT diagnose**.  
It assists in **prioritization and escalation decisions**.

---

## 🧠 Core Features

### ✅ Guided Triage Workflow
- Step-by-step assessment (registration → vitals → context → summary)
- Prevents unsafe skipping of steps

### 📈 Trend-Aware Monitoring
- Uses **linear slope analysis** (NumPy polyfit)
- Detects deterioration even before hard thresholds are crossed

### 🚨 Risk Stratification
- Monitors:
  - Heart Rate
  - SpO₂
  - Pain Score
- Flags:
  - Worsening trends
  - Critical red-zone thresholds

### 📸 Conditional Wound Analysis
- Image upload only triggered for:
  - Wound/Skin issues
  - Fever/Infection cases

### 🧾 Explainable Risk Output
- Clear “Why this was flagged” reasoning
- Clinician-friendly explanations

### 🔗 Clinician Data Bridge
- QR code summarizing:
  - Patient details
  - Status
  - Specialist routing
  - Latest vitals
  - Image availability

---

## 🧑‍⚕️ Supported Clinical Domains

- Wound / Skin conditions  
- Chest pain  
- Breathing issues  
- Fever / Infection  
- Neurological symptoms  

---

## 🛠️ Tech Stack

- **Frontend & App Logic:** Streamlit  
- **Data Processing:** NumPy, Pandas  
- **Image Handling:** Pillow  
- **QR Generation:** qrcode  

---

## 📂 Project Structure

Triage_app/
├── streamlit_app.py        # Main Streamlit application
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
├── LICENSE                 # Open-source license
└── .devcontainer/          # Codespaces configuration

