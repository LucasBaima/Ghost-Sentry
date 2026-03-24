# Ghost-Sentry
Autonomous Deception Agent for Docker containers - Real-time threat detection and attacker profiling



# 🛡️ Ghost Sentry: Autonomous Deception Agent

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Status: Concept/Development](https://img.shields.io/badge/Status-In--Development-orange.svg)]()

**Ghost Sentry** is a high-performance, event-driven security agent designed for Docker environments. It shifts the paradigm from passive defense to **Cyber Counter-Intelligence** by deploying "intelligent bait" (honeypots) and profiling attackers in real-time.

---

## 🎯 The Real-World Pain
In modern Cloud-Native environments, the **Mean Time to Detect (MTTD)** a breach is often measured in weeks. Attackers who compromise a container often move laterally, exploring files and environment variables undetected. 

**Ghost Sentry solves this by:**
-   **Immediate Detection:** Using kernel-level events to catch intruders the millisecond they touch a bait file.
-   **Deep Profiling:** Moving beyond simple alerts to collect OSINT (Open Source Intelligence) and forensic data about the attacker.
-   **Resource Efficiency:** Built with C++ and event-driven logic to ensure near-zero CPU overhead.

---

## 🏗️ Architecture & Core Technologies

The system is designed with a modular approach to ensure scalability and security:

* **The Sentry (C++):** A lightweight agent that monitors the filesystem using `inotify` (Linux API). It avoids the pitfalls of CPU-heavy polling.
* **The Intelligence Engine (Python):** Orchestrates data collection from the sensor and triggers external OSINT APIs (e.g., AbuseIPDB, VirusTotal).
* **Docker Integration:** Seamlessly deploys as a sidecar or an internal agent to monitor sensitive paths (`/etc`, `.env`, `id_rsa`).

---

## 🚀 Key Features (Roadmap 2026/2027)
- [ ] **Real-time File Inotify:** Instant alerts on unauthorized access.
- [ ] **Automated Attacker Dossiê:** Automatic IP geolocation and threat history report.
- [ ] **Anti-Tampering:** Protection layers to prevent the agent from being killed by the attacker.
- [ ] **Smart Decoys:** AI-generated fake data to keep the attacker busy while we collect telemetry.

---

## 🛠️ Getting Started (WIP)

*Note: This project is currently under active development as part of a high-performance AI Infrastructure & Cybersecurity research.*

### Prerequisites
- Linux Kernel 5.0+
- Docker & Docker Compose
- GCC/G++ for compilation

---

## 👨‍💻 Author
**João Lucas de Oliveira Gonçalves Baima**
*Computer Science Student & Developer*

Looking to build impactful Open Source tools for the global security community.

---

## 📄 License
This project is licensed under the **GNU GPLv3 License** - see the [LICENSE](LICENSE) file for details.
