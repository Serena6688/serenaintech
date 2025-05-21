---
title: Http Server

layout: default

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

- One listener thread for incoming connections
- Request-handling worker threads for each connection
- Static content served from `/public` folder

---

## 🔗 GitHub Repository

Explore the source code and documentation for the Othello Game:

[👉 View on GitHub]( https://github.com/upenn-systems/25sp-cit5950-serena6688-junxiangli31415926-searchserver)
---