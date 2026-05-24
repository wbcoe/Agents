# 📌 README – AI Job Description Extractor using n8n + Groq + Google Sheets

## Overview

This workflow automates the extraction of structured recruitment information from uploaded **Job Description (JD) files**. The workflow processes the document using **Groq LLM**, identifies relevant hiring attributes, and stores the extracted information in **Google Sheets** for analysis and tracking.

The goal is to convert **unstructured job descriptions → structured hiring data** automatically.

---

## Workflow

```text
Upload JD File
      │
      ▼
Extract Text from Document
      │
      ▼
Process Content using Groq AI
      │
      ▼
Identify Hiring Attributes
(Company, Skills, Experience, Location, etc.)
      │
      ▼
Format Structured Output
      │
      ▼
Append Data into Google Sheets
```

---

## Features

* Upload job description files directly
* AI-powered extraction using Groq
* Converts unstructured recruitment data into structured records
* Automatically appends extracted information into Google Sheets
* Supports recruitment analytics and hiring pipelines
* Reduces manual screening effort

---

## Tech Stack

* **n8n** — Workflow orchestration
* **Groq API** — LLM processing & extraction
* **Google Sheets** — Structured data storage
* **File Upload Input** — JD ingestion

---

## Extracted Fields

The workflow extracts information such as:

* Company Name
* Required Skills
* Location
* Experience Level
* Remote / On-site status
* Job Type
* Easy Apply availability
* Additional hiring attributes (if present)

---

## Example Input

**Uploaded File:**

```text
job description copied from linkedin
```

Contains multiple job descriptions similar to:

```text
Company: xyz

Looking for professionals with expertise in Computer Vision,
Robotics, Artificial Intelligence, Python, OpenCV, ROS,
Deep Learning, Object Detection and LiDAR.

Experience: Experienced
Location: Remote
Job Type: Freelance


Company: abc

Required skills:
Python, Machine Learning, Deep Learning,
Data Science, AI

Location: India
Experience Level: PhD
Job Type: Full-time
Remote role
```

---

## Example Output (Stored in Google Sheet)

| Company                  | Skills                                                                                                                                                                             | Location | Experience Level | Remote | Job Type  | Easy Apply |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | ---------------- | ------ | --------- | ---------- |
| xyz        | Computer Vision, Robotics, Artificial Intelligence, Computer Science, Electronics, Python, C++, OpenCV, ROS, SLAM, LiDAR, Deep Learning, Object Detection, Segmentation, 3D Vision | Remote   | Experienced      | Yes    | Freelance | No         |
| abc | Python, ML, DL, Data Science, AI                                                                                                                                                   | India    | PhD              | Yes    | Full-time | No         |

---

## Output Behaviour

For every uploaded JD file, the workflow:

1. Reads and extracts text from the document
2. Sends extracted content to Groq LLM
3. Identifies structured hiring attributes
4. Formats extracted information into tabular data
5. Appends new rows automatically to Google Sheets

No existing records are overwritten.

---

## Use Cases

Suitable for:

* Recruitment automation
* Hiring analytics
* Job market research
* Talent intelligence datasets
* Candidate matching systems
* ATS preprocessing pipelines

---

## Example Google Sheet Structure

Recommended columns:

| Company | Skills | Location | Experience Level | Remote | Job Type | Easy Apply |
| ------- | ------ | -------- | ---------------- | ------ | -------- | ---------- |

Additional fields can be added depending on requirements.

---

## Future Improvements

Potential enhancements:

* Resume ↔ JD matching
* Candidate scoring
* Skill gap analysis
* Email notifications
* Dashboard integration
* ATS integration
* Multi-sheet categorization

---

## Outcome

This workflow transforms raw job descriptions into **structured recruitment intelligence**, helping teams analyze hiring requirements faster and maintain searchable hiring datasets automatically.

---

### Built With

**n8n + Groq + Google Sheets** for AI-powered recruitment automation.
