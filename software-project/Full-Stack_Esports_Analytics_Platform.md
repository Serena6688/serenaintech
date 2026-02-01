
---
title: Nexus: Full-Stack Esports Analytics Platform
parent: Intelligent Systems
layout: default
nav_order: 6
permalink: /software-project/nexus-esports-analytics/
---

# 🎮 Nexus: Full-Stack Esports Analytics Platform

<img src="/serenaintech/assets/images/nexus.png" alt="Nexus Esports Analytics Platform screenshot" style="width: auto; max-height: 300px; margin: 0 1.5rem 1rem 0;" />

An **end-to-end full-stack analytics platform** for professional esports, enabling
interactive exploration of **Valorant** and **League of Legends** data across players,
teams, maps, agents/champions, and match performance.

---

## 🎯 Project Overview

Nexus was built to transform **raw esports match data** into **actionable, interactive analytics**
through a cleanly separated **frontend–backend–data** architecture.

The system integrates a **React frontend** with a **Node.js + Express backend**, exposing
REST APIs backed by **SQL-based analytics queries** over structured esports datasets.
Users can analyze individual games as well as **cross-game team performance**
within a unified interface.

---

## 🎥 Demo & Live App

- ▶️ **YouTube Walkthrough**
<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe src="https://www.youtube.com/watch?v=pxF6IQOMXqA" 
          style="position:absolute;top:0;left:0;width:100%;height:100%;" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>
</div>

---

## 🔧 Tech Stack

**Frontend**
- React (JavaScript)
- CSS (dark-theme UI)
- Reusable components and multi-page analytics views

**Backend**
- Node.js
- Express
- REST APIs with filtering, pagination, and aggregation

**Data**
- Structured esports datasets (Valorant & League of Legends)
- SQL queries for analytics logic

---

## ⚙️ Key Features

### 🎮 Valorant Analytics
- Map pick & ban rate analysis
- Agent specialists and detailed player statistics
- Clutch performance leaders (e.g. 1v5 scenarios)
- Tournament match records with flexible filters  
  (tournament, stage, match type, teams)

---

### 🐉 League of Legends Analytics
- Top champions per lane
- Dragon control statistics
- Unexpected loss detection  
  (e.g. games with gold lead > 3000 but still lost)
- Full match records with MVP / SVP data

---

### 🏆 Cross-Game Team Rankings
- Combined win rates across Valorant + League of Legends
- Dedicated team comparison and ranking views

---

## 🚀 Architecture Overview

### High-Level Structure

Client (React)
→ REST API calls
→ Server (Node.js + Express)
→ SQL queries over structured datasets

### Design Highlights

- Clear separation of frontend, backend, and data layers
- Backend endpoints encapsulate analytics and aggregation logic
- Frontend focuses on visualization and user interaction
- SQL used directly for performant filtering and computation

---

## 📂 Project Structure

5500FINALPROJECT/
│
├── client/                  # React frontend
│   └── src/
│       ├── components/      # Reusable UI components
│       └── pages/           # Home, Valorant, LoL, Teams, Matches, etc.
│
├── server/                  # Backend (Node.js + Express)
│   ├── sql/                 # SQL analytics queries
│   ├── routes.js            # API routes
│   ├── db.js                # Database connection
│   ├── server.js            # Server entry point
│   └── .env                 # DB configuration
│
├── datasets/                # Esports datasets (Valorant & LoL)
└── README.md

---

⸻

🔗 GitHub Repository

Explore the full source code and documentation:

[👉 View on GitHub](https://github.com/Serena6688/5500finalproject)

---

