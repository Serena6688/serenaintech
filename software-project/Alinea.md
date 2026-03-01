---
title: Alinea – Multi-Agent Group Intelligence
parent: Intelligent Systems
layout: default
nav_order: 6
permalink: /software-project/alinea/
---

# 🧠 Alinea – Multi-Agent Group Intelligence in Chat

Alinea is a multi-agent AI collaboration system built directly inside secure group chats.

Instead of a single assistant producing one answer, Alinea embeds multiple AI agents — each with a distinct reasoning style — inside an XMTP-powered Convos thread. The system structures breakout discussions, synthesizes perspectives, and produces a final coordinated recommendation in real time.

The project explores how human–AI collaboration changes when intelligence operates as a *team* rather than a single model.

<img src="/serenaintech/assets/images/alinea.png" alt="Alinea multi-agent demo" style="width: auto; max-height: 300px; margin: 0 1.5rem 1rem 0;" />

---

## 🎥 Demo Video

Short live demo of the multi-agent discussion flow:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe 
    src="https://www.youtube.com/embed/BG2BHojoBxs"
    style="position:absolute;top:0;left:0;width:100%;height:100%;" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
  </iframe>
</div>
---

## 🔧 Tech Stack

- TypeScript / Node.js
- XMTP Agent SDK
- Convos (XMTP group chat interface)
- Kilo Gateway (OpenAI-compatible LLM API)
- Multi-agent orchestration layer (custom)

---

## ⚙️ Core Features

- Multi-agent collaboration inside group chat
- Structured breakout discussions
- Fixed-round deliberation mechanism (3–5 rounds)
- Persona-based reasoning (Skeptic, Creative, Pragmatist, Coordinator)
- Summary aggregation & final synthesis
- Deterministic coordination script for demo stability
- Persistent XMTP identity & encrypted messaging

---

## 🚀 Architecture Overview

### High-Level Flow

User → Convos Group Chat  
→ XMTP Network  
→ Coordinator Agent  
→ Breakout Threads  
→ Summary Collection  
→ Final Synthesis (Main Thread)

---

## 🧠 Agent Roles

### 🧩 Coordinator
- Splits user prompt into structured breakout tasks
- Orchestrates discussion rounds
- Collects summaries
- Produces final synthesized recommendation

### ⚠️ Skeptic
- Identifies risks, trade-offs, weak assumptions

### 🎨 Creative
- Generates bold, exploratory ideas

### 🛠 Pragmatist
- Evaluates feasibility and implementation steps

---

## 🔄 Breakout Logic (Hackathon Scope)

To maintain stability and clarity:

- Breakout groups are pre-configured XMTP threads
- Each breakout runs a fixed number of exchanges
- Convergence is time-based, not consensus-based
- The coordinator follows a rigid script:

> Split → Wait → Collect → Summarize → Synthesize

This ensures a demoable and deterministic multi-agent workflow.

---

## 🔐 Why XMTP?

XMTP provides:

- End-to-end encrypted group messaging
- Agent identities via wallet-based authentication
- Scoped conversation boundaries

Agents operate as first-class participants inside the thread,
not as an external overlay.

---

## ⚡ Key Design Principle

Traditional chatbots provide a single answer.

Alinea provides structured deliberation.

The system simulates collaborative reasoning in a shared environment,
making the *group context essential* rather than decorative.

---

## 📂 Project Structure

**src/**
- **index.ts** — XMTP agent bootstrap
- **coordinator.ts** — Orchestration logic
- **breakout-agent.ts** — Persona discussion engine
- **llm.ts** — Kilo Gateway integration
- **personas/** — Agent identity prompts

---

## 🔗 GitHub Repository

Explore the source code and architecture:

[👉 View on GitHub](https://github.com/Serena6688/Alinea)