---
layout: page
title: Network Systems Projects
description: A collection of systems-level projects focused on network communication, protocol design, and processor architecture
img: /assets/img/netsys/netsys.png
importance: 5
category: School
---

## Project Overview

This page highlights a series of systems-level projects that demonstrate practical applications of networking principles, socket programming, server design, distributed systems, and low-level computer architecture.  
These projects span C and C++ implementations and cover a wide range of communication models and system interactions — from client-server protocols and web servers to HTTP proxies and processor modeling.

---

## UDP Client-Server File Transfer

**Role:** Systems Developer  
**Tech:** C, UDP, Sockets, Stop-and-Wait Protocol  
**Duration:** Jan 2024 – May 2024

- Designed a **UDP-based client-server system** replicating core FTP functionalities.
- Supported file upload, download, and listing with robust error handling.
- Built a **reliable UDP layer** using stop-and-wait, ACKs, retransmissions, windowing, and flow control.
- Optimized for high-volume transfers exceeding 100MB with 99%+ data integrity.

---

## Multi-threaded TCP Web Server

**Role:** Systems Developer  
**Tech:** C, TCP, Threads, HTTP  
**Duration:** Jan 2024 – May 2024

- Created a **multi-threaded TCP web server** to handle simultaneous client connections.
- Implemented **HTTP parsing and response generation**, enabling dynamic web content delivery.
- Used **thread synchronization** to manage concurrent sessions and minimize latency.
- Achieved high throughput and stability under concurrent request load.

---

## HTTP Proxy Server with Filtering and Caching

**Role:** Systems Developer  
**Tech:** C++, HTTP, Proxy Architecture  
**Duration:** Jan 2024 – May 2024

- Developed an **HTTP proxy server** that relays and filters client requests.
- Added a **caching layer** to store frequently accessed content and reduce bandwidth usage.
- Integrated **URL filtering and request transformation** to modify content for low-resource clients or block restricted sites.

---

## Distributed File System (DFS)

**Role:** Systems Developer  
**Tech:** C++, Sockets, Redundant Storage  
**Duration:** Jan 2024 – May 2024

- Built a **distributed file system** supporting redundancy across four servers.
- Implemented **file chunking and replication** to ensure 100% recovery from single-node failure.
- Handled client-server communication, enabling reliable file upload and download with fault tolerance.

---

## RISC-V Processor Modeling in CodAL

**Role:** Computer Architect  
**Tech:** CodAL, RISC-V, Pipeline Architecture  
**Duration:** Jan 2024 – May 2024

- Modeled a **cycle-accurate RISC-V processor** with support for core instruction types: R, I, branching, and memory ops.
- Implemented **forwarding logic and pipeline hazard resolution** for optimal throughput.
- Verified ALU and memory modules for correctness and performance.
- Simulated execution timing to ensure architectural integrity under instruction pressure.

---

## Technical Focus Areas

- **Networking Protocols:** TCP, UDP, Stop-and-Wait, Windowing, ACKs  
- **Server Architecture:** Multi-threaded design, client management, request parsing  
- **Distributed Systems:** Fault tolerance, file replication, redundancy  
- **Proxy & Caching:** HTTP filtering, content transformation, latency reduction  
- **Computer Architecture:** ISA modeling, pipelining, forwarding, cycle accuracy  
- **Languages & Tools:** C, C++, CodAL, Sockets, Threads, Git, Make

---

## Project Diagrams

<div class="row justify-content-center">
  <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/netsys/dfs.png" title="UDP diagram" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/netsys/multi.png" title="UDP diagram" class="img-fluid rounded z-depth-1"%}
  </div>
</div>
<br><br>
<div class="row justify-content-center">
  <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/netsys/udp.png" title="UDP diagram" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/netsys/proxy.png" title="UDP diagram" class="img-fluid rounded z-depth-1"%}
  </div>
</div>
<br><br>