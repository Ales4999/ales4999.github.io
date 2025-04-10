---
layout: page
title: Cybersecurity
description: Coursework in system vulnerabilities, web security, and real-world exploitation
img: /assets/img/cyber/cyber.png
importance: 7
category: School
---

## Course Overview

**CSCI 3403: Introduction to Computer Security** is an upper-division course at the University of Colorado Boulder focused on real-world security threats and mitigation techniques.  
It covered system vulnerabilities, web-based attacks, cryptographic protocols, and the ethical responsibilities of security professionals.

---

## Topics Covered

- **CIA Triad: Confidentiality, Integrity, Availability**  
  Explored the foundational model of cybersecurity that underpins all secure systems. We examined how system design and policy decisions influence each of the three pillars and how attackers exploit trade-offs between them.

- **Authentication, Authorization, and Access Control**  
  Studied various methods for verifying user identity (e.g., passwords, tokens), controlling access (e.g., ACLs, RBAC), and enforcing privilege separation to minimize attack surfaces in modern applications.

- **Cryptographic Concepts & Algorithms**  
  Covered the basics of cryptography, including symmetric encryption (AES), public-key cryptography (RSA), hashing (SHA-2), digital signatures, and the role of key exchange protocols (Diffie-Hellman, TLS).

- **Secure Password Handling**  
  Learned about best practices for storing user credentials securely using hashing algorithms with salting (e.g., bcrypt), as well as common mistakes that lead to credential leaks.

- **Web Security Vulnerabilities**  
  Investigated a range of web-based threats including:
  - **Cross-Site Scripting (XSS)**: Reflected, stored, and DOM-based variants.
  - **SQL Injection**: Manipulating database queries through unsanitized input.
  - **Cross-Site Request Forgery (CSRF)**: Exploiting trust in the authenticated user.
  - **Content Injection**: Misuse of dynamic web content rendering.

- **Network Security Protocols**  
  Explored how secure communication is achieved through protocols like TLS/SSL, HTTPS, and secure email standards (e.g., PGP). Studied the use and configuration of firewalls and VPNs to prevent external breaches.

- **Software Vulnerabilities & Exploitation**  
  Covered low-level software bugs and how they are exploited, including:
  - **Buffer overflows**
  - **Format string vulnerabilities**
  - **Race conditions**
  - **Improper error handling**
  Emphasis was placed on writing secure C code and analyzing real-world exploits.

- **Threat Modeling and Security Audits**  
  Learned structured techniques for identifying and prioritizing risks in systems. Practiced modeling attack vectors, estimating impact, and identifying weak points during software design and review.

- **Ethical Hacking & Responsible Disclosure**  
  Discussed the role of ethical hackers, how bug bounty programs work, and the legal/ethical boundaries of penetration testing. Emphasized responsible communication of vulnerabilities and coordination with vendors.


---

## Key Projects

### Lab 4: Cross-Site Scripting (XSS)  
- Analyzed and exploited multiple levels of XSS vulnerabilities in a test e-commerce site.  
- Bypassed defenses such as tag filtering and input sanitization.  
- Demonstrated both **reflected** and **stored XSS** by injecting JavaScript payloads to perform unauthorized actions.  
- Learned how real-world flaws are introduced and how to properly sanitize user input.

### Lab 5: Server-Side Injection  
- Performed a series of **SQL injection attacks** against a vulnerable MariaDB-powered website.  
- Bypassed login authentication, extracted admin credentials, and queried credit card data.  
- Explored **PHP injection** to gain file system access and execute code on the server.  
- Gained practical insight into how unvalidated input can escalate into full system compromise.

### Lab 6: Bug Bounty Report  
- Participated in a mock **bug bounty challenge**, selecting a real-world or personal site for testing.  
- Used tools like **Burp Suite** to probe for input sanitization, XSS, and CSRF vulnerabilities.  
- Practiced **safe and ethical penetration testing** by adhering to public program scopes and creating a formal security report.

---

## Tools & Skills Gained

- Programming: C, Python, Bash  
- Tools: Wireshark, Burp Suite, GDB, MariaDB sandbox  
- Skills: SQL injection, XSS exploitation, vulnerability discovery, ethical disclosure  
- Concepts: Threat modeling, secure software design, real-world attack mitigation

---

## Reflection

This course provided hands-on experience with common vulnerabilities and helped me build a **security-first mindset** when developing software.  
It reinforced the importance of **thinking like an attacker** to write code that defends against the unexpected, and taught me how to conduct both theoretical analysis and practical exploits responsibly.