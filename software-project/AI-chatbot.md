---
title: AI-chatbot
parent: Projects
layout: default
nav_order: 5
permalink: /software-project/AI-chatbot/
---

# 🤖 PartSelect Parts Assistant (LLM-Assisted)

An AI-powered **conversational appliance repair assistant** designed to help users  
**diagnose issues, confirm part compatibility, and follow correct installation steps**
for dishwashers and refrigerators.

Unlike traditional chatbots, this system uses **deterministic dialog routing**
with **selective LLM augmentation**, ensuring reliability and preventing dialog drift.
<img src="/serenaintech/assets/images/partselect.png" alt="Innocube screenshot" style="width: auto; max-height: 300px; margin: 0 1.5rem 1rem 0;" />


---

## 🎥 Demo Video

Watch a full walkthrough of the system, including troubleshooting and installation flows:

👉 **YouTube Demo**:
<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe src="https://youtu.be/-WGu6BZnxb0" 
          style="position:absolute;top:0;left:0;width:100%;height:100%;" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>
</div>
---

## 🔧 Tech Stack

- TypeScript
- Node.js
- Rule-based dialog state machine
- Groq LLM API (optional, fallback-only)
- REST-style backend API

---

## ⚙️ Features

- Guided, multi-turn troubleshooting flows
- Part ↔ model compatibility confirmation
- Step-by-step installation guidance
- Intent stickiness (prevents intent stealing)
- Appliance pinning across turns
- Optional LLM fallback for ambiguous user input
- Demo support for order flow and human handoff

---

## 🚀 Architecture Overview

### High-Level Flow

Frontend
→ message + history
→ router.ts (main dialog brain)

### Core Router Responsibilities

- Intent inference
- Appliance pinning (dishwasher / refrigerator)
- Dialog state tracking
- Intent stickiness across short replies

### Routing Strategy

- **Deterministic dialog flows** (default)
- **LLM fallback (Groq)** only when rule-based parsing fails

> **Key design principle:**  
> The LLM never decides the dialog flow.  
> It is only used to parse ambiguous natural language when rules fail.

---

## 🧠 Core Concepts

### 1. Intent Stickiness (No Intent Stealing)

Short or ambiguous replies like:

- `yes`
- `panel`
- `clamps`
- `side`
- `humming`

are **consumed by the current dialog state**, rather than being reclassified as new intents.

This prevents classic chatbot failures such as:

> User: *“clamps”*  
> Bot: *“Here’s a replacement pump.”*

---

### 2. Appliance Pinning

Once inferred, the appliance type remains pinned across turns:

User: My dishwasher isn’t draining
User: yes
User: humming

The system continues the **dishwasher drain diagnostic flow**
without requiring the user to restate context.

---

### 3. Explicit Dialog State Machine

The router tracks fine-grained awaiting states such as:

- `pump_sound`
- `dishwasher_drain_speed`
- `install_step`
- `panel_still_wont_drop_yesno`
- `clamp_type`
- `connector_moving_or_stuck`

Each user message is first handled by the **current awaiting state**
before any re-routing logic is applied.

---

## ⚡ Where the LLM Is Used (Intentionally Limited)

The Groq LLM is **not used to “chat”**.

It is only invoked when:
- The system expects a specific semantic classification
- Rule-based parsing returns `unknown`

### Example

User input:

“It makes a weird buzzing noise”

- Rule-based parser → `unknown`
- Groq fallback → `"humming"`

This allows the dialog flow to continue  
**without granting control of routing decisions to the LLM**.

---

## 📂 Project Structure

src/
├─ router.ts          # main dialog router & state machine
├─ groqHelpers.ts     # narrow LLM helpers (classification only)
├─ tools.ts           # demo tools (compatibility, lookup, guides)
├─ types.ts           # ChatRequest / ChatResponse / Intent


---

## 🔗 GitHub Repository

Explore the source code and documentation for the Othello Game:

[👉 View on GitHub](https://github.com/Serena6688/InstalilyAIcase)
---