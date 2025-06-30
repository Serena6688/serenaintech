---
title: Http Server
parent: Projects
layout: default
nav_order: 4
permalink: /software-project/http-server/
---

# 🌐 Multithreaded HTTP Server

A low-level C++ web server built from scratch using POSIX sockets and pthreads.

---

## 🔧 Tech Stack

- C++
- POSIX Sockets (`<sys/socket.h>`, `<arpa/inet.h>`)
- pthreads

---

## ⚙️ Features

- Handles multiple simultaneous connections via threading
- Serves static files (HTML, CSS, etc.)
- Implements a basic HTTP 1.0 protocol
- Graceful shutdown and error handling

---

## 🚀 Architecture Overview
<img src="/serenaintech/assets/images/httpserver.png" alt="HTTP Server picture" style="width: 300px; height: auto; float: left; margin: 0 1.5rem 1rem 0;" />

- One listener thread for incoming connections
- Request-handling worker threads for each connection
- Static content served from `/public` folder

---

## 🔗 GitHub Repository

Explore the source code and documentation for the Othello Game:

[👉 View on GitHub](https://gitfront.io/r/Serena6688/hzsX5mNJwGBk/Multi-Threaded-HTTP-Server-Search-Engine-C-POSIX/)
---