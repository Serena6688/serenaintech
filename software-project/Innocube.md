---
title: Survey Platform
parent: Projects
layout: default
nav_order: 4
permalink: /software-project/innocube/
---

# 🧠 Innocube: Intelligent Survey Analytics Platform
<img src="/serenaintech/assets/images/innocube.png" alt="Innocube screenshot" style="width: auto; max-height: 300px; margin: 0 1.5rem 1rem 0;" />

A full-stack data intelligence platform that transforms raw survey results into interactive analytics dashboards — powered by AI, data visualization, and automation.

---

## 🎯 Project Overview

**Innocube** is a lightweight yet intelligent web application designed to **analyze large-scale consumer survey data** in real time.  
It automatically cleans uploaded Excel files, extracts structured insights, and visualizes demographics, brand preference, and purchasing power distributions — all within an interactive dashboard.

The project combines **data engineering, Flask-based back-end design, and modern web visualization**, offering an end-to-end data analytics workflow.

---

## 🔧 Tech Stack

- **Backend:** Python (Flask, SQLAlchemy, Pandas)
- **Frontend:** HTML, JavaScript, Chart.js, Bootstrap
- **Database:** SQLite / PostgreSQL (containerized)
- **Deployment:** Docker, Docker Compose, Nginx (optional for production)
- **Data Processing:** Pandas + OpenPyXL for intelligent Excel ingestion

---

## ⚙️ Core Features

- 📊 **Automated Data Parsing:** Upload raw survey Excel sheets; the app auto-detects demographic, location, and purchasing power fields.
- 🧩 **Dynamic Dashboard:** Real-time visualizations of age, gender, and purchasing power distributions.
- 🧠 **Smart Data Cleaning:** Handles mixed-language column names, missing values, and inconsistent data formats.
- 🌐 **Modular API Architecture:** RESTful endpoints for analytics, survey management, and data export.
- 🗂️ **Seamless Extensibility:** Easy integration with cloud databases or BI dashboards (e.g., Power BI, Tableau).

---

## 💡 System Architecture

The system follows a **Model-View-Controller (MVC)** architecture:
- **Model:** SQLAlchemy ORM managing surveys, respondents, and analytics results
- **View:** Responsive web UI with real-time Chart.js rendering
- **Controller:** Flask routes handling uploads, parsing, and analytics computation

---

## 📈 Data Intelligence

Innocube’s analytics engine automatically:
- Generates **demographic breakdowns** (Age, Gender, Region)
- Aggregates **purchasing power** segments into actionable visual insights
- Supports future extensions like **AI-driven clustering, sentiment analysis**, and **predictive modeling**

---

## 🧪 Testing & Validation

- Verified across multiple Excel formats (`.xlsx`, `.csv`)
- Robust handling of 100K+ record datasets
- Unit testing for upload endpoints, schema validation, and aggregation logic

---

## 🔗 GitHub Repository

Explore the full implementation and documentation on GitHub:  
[👉 View on GitHub](https://github.com/Serena6688/innocube2)

---

## 🎥 Demo Video

Watch the demo walkthrough of Innocube’s intelligent analytics dashboard:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe src="https://www.youtube.com/embed/jyrr1nZk5WA" 
          style="position:absolute;top:0;left:0;width:100%;height:100%;" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>
</div>

---

## 🌟 Impact

Innocube streamlines consumer insight analysis by reducing manual Excel processing time from hours to minutes.  
It bridges the gap between **raw data** and **strategic decision-making**, making it ideal for research teams, marketing analysts, and data-driven organizations.

---