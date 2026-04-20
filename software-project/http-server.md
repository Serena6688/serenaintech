---
title: Http Server
parent: Systems & Infrastructure
layout: default
nav_order: 4
permalink: /software-project/http-server/
---

# 🌐 Multithreaded HTTP Server
<img src="/serenaintech/assets/images/httpserver.png" alt="HTTP Server picture" style="width: 600px; height: auto; margin: 0 1.5rem 1rem 0;" />

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
  <img src="/serenaintech/assets/images/http1.png" alt="HTTP Server picture" style="width: 600px; height: auto; margin: 0 1.5rem 1rem 0;" />
  <img src="/serenaintech/assets/images/http2.png" alt="HTTP Server picture" style="width: 600px; height: auto; margin: 0 1.5rem 1rem 0;" />

---
