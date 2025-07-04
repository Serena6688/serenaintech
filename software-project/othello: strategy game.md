---
title: Othello Game
parent: Projects
layout: default
nav_order: 3
permalink: /software-project/othello/
---

# ♟ Othello: AI Strategy Game
<img src="/serenaintech/assets/images/othelle.png" alt="Othelle picture" style="width: auto; max-height: 300px; margin: 0 1.5rem 1rem 0;" />

A modern take on the classic strategy board game, powered by artificial intelligence.

---

## 🎯 Project Overview

This project involved building a fully functional Othello game, integrating AI algorithms with a user-friendly JavaFX GUI. The core objective was to implement intelligent computer players using game theory algorithms and seamlessly connect them with the GUI for interactive gameplay.

---

## 🔧 Tech Stack

-   Java, JavaFX for GUI 
-   Minimax and Alpha-Beta Pruning algorithms for AI 
-   MVC design pattern (initially Strategy Pattern, but evolved)
-   CSS and FXML for enhanced GUI

---

## 🎮 Key Features

-   Interactive UI with: 
  - Legal move hints; 
  - Time Remaining feature 
-   Clean visual design with a calming "deep green" color scheme 
-   Responsive board

---

## 🤖 AI Strategy

The AI employs the **Minimax algorithm** to evaluate board states and select optimal moves. **Alpha-Beta pruning** is used to reduce computation and improve efficiency. The project also explored Monte Carlo Tree Search (MCTS) and a Custom (Randomized Negamax) algorithm.

---

## 🎨 GUI Enhancements

The GUI was significantly enhanced using CSS for styling (colors, fonts, spacing) and FXML for layout. This allowed for a separation of UI design from game logic. A "Time Remaining" feature was added to increase the game's strategic depth.

---

## 🧪 Testing

Testing was conducted throughout the development process, including mocking the game and comparing it with online Othello games.

---
## 🔗 GitHub Repository

Explore the source code and documentation for the Othello Game:

[👉 View on GitHub](https://github.com/cit5940-25sp/cit-5940-final-project-lpb)
---

## 🎥 Demo Video

Here’s a quick walkthrough of the Othello Game:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe src="https://www.youtube.com/embed/jNO9I22km8I" 
          style="position:absolute;top:0;left:0;width:100%;height:100%;" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>
</div>
---