# EcoForge AI: Autonomous E-Waste Triage & Campus Circular Hardware Forge ⚡

[![UN SDG 12](https://img.shields.io/badge/UN%20SDG-12%3A%20Responsible%20Consumption-emerald)](https://sdgs.un.org/goals/goal12)
[![Program](https://img.shields.io/badge/1M1B-IBM%20SkillsBuild%20Internship-blue)](https://skillsbuild.org)
[![Model](https://img.shields.io/badge/IBM%20Granite-3.0--8B--Instruct-purple)](https://www.ibm.com/granite)
[![Orchestrator](https://img.shields.io/badge/Orchestrator-IBM%20Bob%20Multi--Agent-teal)](https://github.com/i-am-bee)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

> **"Mine silicon, not landfills."**  
> An autonomous multi-agent decision-support framework designed for university campuses. EcoForge AI inspects discarded institutional hardware, enforces statutory safety standards (**CPCB E-Waste Rules 2022 Schedule II RoHS** and **IEEE Standard 1874-2018**), and salvages functional microcontrollers and power ICs to supply student robotics, IoT, and electric vehicle research at **Vellore Institute of Technology (VIT Bhopal)**.

---

## 📌 Project Identification
* **Developer:** Aisha Ifrah (B.Tech Computer Science Engineering with AI & ML, VIT Bhopal)
* **Program:** 1M1B – IBM SkillsBuild AI for Sustainability Virtual Internship (July–Sep 2026, in collaboration with AICTE)
* **Primary SDG:** **SDG 12: Responsible Consumption & Production** (Target 12.4 & 12.5)
* **Secondary SDGs:** **SDG 11** (Sustainable Cities & Campuses), **SDG 9** (Industry, Innovation & Infrastructure)
* **Live Web App:** [https://ecoforge-ai.vercel.app](https://ecoforge-ai.vercel.app)
* **Presentation Deck:** [Google Slides Presentation](https://docs.google.com/presentation/d/1rHoR_410dFzuigZc4Q3-l2Gkg-OgTx-9-dkam6lsRvg/edit)
* **Technical Blueprint:** [Project Documentation](https://docs.google.com/document/d/1tiQ5738FnKrHgVPkyNAWuNtJrY6fZgWDjw94d-gu2Vc/edit)

---

## 🎯 The Problem: The Institutional Silicon Crisis
1. **Premature Bulk Shredding:** Educational institutions discard hundreds of kilograms of obsolete networking equipment, server blades, and lab instrumentation annually. Traditional recyclers shred these units whole, destroying 100% operational microcontrollers and voltage regulators.
2. **Student Component Shortages:** Student engineering teams face procurement delays and high costs for basic silicon parts.
3. **Hazardous Informal Desoldering:** Manual harvesting in ill-equipped spaces exposes student makers to toxic lead solder fumes and lithium thermal fires.

---

## 💡 The Solution: Reverse-BOM Micro-Harvesting & Circular Supply Chain
Unlike generic consumer recycling apps that merely advise users which trash can to use (*"put in blue bin"*), **EcoForge AI** solves what happens next:
* **Silkscreen OCR Diagnostics:** Translates board part numbers into a hierarchical **Reverse-BOM**.
* **Chemical Safety Firewall:** Automatically checks RoHS thresholds (Lead $< 0.1\%$, Cadmium $< 0.01\%$) and isolates swollen batteries into dry-sand bins.
* **Campus Requisition Matcher:** Semantically connects harvested components with active student project backlogs.
* **Avoided Carbon Ledger:** Tracks embodied carbon avoided ($\approx 1.42\text{ kg CO}_2\text{e}$ per IC).

---

## 🏗️ System Architecture

```
[ Discarded Hardware PCB Intake ]
               │
               ▼
   [ Visual Silkscreen OCR / Telemetry ]
               │
               ▼
  ╔═══════════════════════════════════════════════════════════╗
  ║          IBM BOB MULTI-AGENT ORCHESTRATOR                ║
  ║                                                           ║
  ║  1. Component Triage Agent (IBM Granite 3.0-8B-Instruct)  ║
  ║     └── Reverse-BOM Extraction (QFN, SOIC, TSSOP)         ║
  ║                                                           ║
  ║  2. Chemical & Hardware Safety Auditor                    ║
  ║     └── RAG: CPCB 2022 Schedule II & IEEE 1874-2018       ║
  ║     └── RoHS Lead & Cadmium Threshold Checks              ║
  ║                                                           ║
  ║  3. Campus Inventory Matcher                              ║
  ║     └── ChromaDB Vector Store: Student Requisition Search ║
  ║                                                           ║
  ║  4. Circular Credit Dispatcher                            ║
  ║     └── Carbon Ledger: 1.42 kg CO2e / IC Avoided          ║
  ║     └── Mint Verified Campus Circular Credits             ║
  ╚═══════════════════════════════════════════════════════════╝
               │
               ▼
   [ Deterministic JSON Schema Guardrails (Pydantic) ]
               │
               ▼
 ┌───────────────────────────────────────────────────────────┐
 │ Approved: Student Research Labs (Maker Space AB-1, RIS)   │
 │ Supervised: Fume Hood Desoldering (Pre-2006 Leaded Solder)│
 │ Rejected: Class-D Dry Sand Quarantine (Thermal Hazard)    │
 └───────────────────────────────────────────────────────────┘
```

---

## 🚀 Interactive Web Application Features

1. **Live Classifier Studio:** Quick-select chips for real institutional scrap:
   * *TP-Link Wi-Fi Router* $\rightarrow$ MediaTek MT7628 SoC, Winbond Flash, MP1482 Buck Regulator
   * *Dell Server SMPS (750W)* $\rightarrow$ UCC28950 PWM Controller, IRFB4110 MOSFETs
   * *Swollen Drone LiPo Battery* $\rightarrow$ Immediate Class-D Dry Sand Bin Quarantine
   * *1998 Lab Oscilloscope* $\rightarrow$ Non-RoHS Sn60Pb40 Leaded Solder Safety Protocol
2. **Live "IBM Bob" Terminal Trace:** Real-time console logs displaying inter-agent reasoning and schema verification.
3. **Statutory Standards Explorer:** Instant retrieval of CPCB 2022 rules and IEEE 1874 metrics.
4. **Campus Circular Ledger:** Audit table tracking batch intake across VIT Bhopal departments.
5. **Deterministic JSON Guardrails:** Enforces Pydantic data contracts to eliminate hallucinations.

---

## 📦 Repository Structure

```
├── index.html              # Standalone web app (Tailwind CSS, dark mode, interactive terminal)
├── ecoforge_prototype.py   # Multi-agent Python prototype with Pydantic guardrails & CPCB RAG
├── vercel.json             # Static deployment configuration for Vercel
├── .gitignore              # Git ignore configuration
└── README.md               # Complete project documentation
```

---

## 🛠️ Local Installation & Quickstart

### 1. Run the Web Application
Double-click `index.html` in any modern web browser or start a local Python HTTP server:
```bash
python3 -m http.server 8000
```
Open [http://localhost:8000](http://localhost:8000) in your browser.

### 2. Run the Multi-Agent Python Prototype
```bash
# Install Pydantic (if not already installed)
pip install pydantic

# Execute the triage testbench
python3 ecoforge_prototype.py
```

---

## 📜 Regulatory Standards Cited
* **CPCB E-Waste (Management) Rules, 2022 (Schedule II):** Ministry of Environment, Forest and Climate Change (MoEFCC), Govt. of India.
* **IEEE Standard 1874-2018:** IEEE Standard for Component Reusability Screening in Personal Computers.
* **IS 13252 / Battery Waste Management Rules 2022:** Indian Bureau of Standards electrical and thermal safety guidelines.

---

## ⚖️ Responsible AI Framework
* **Safety First:** Strict rejection protocol for swollen lithium cells and toxic dielectric capacitors.
* **Deterministic Guardrails:** Zero-hallucination Pydantic models prevent false pinouts and fire risks.
* **Hardware Equity:** Democratizes silicon access for under-funded student research teams.
* **Transparency:** Complete logging of reasoning steps and standard citations.

---

## 🎓 Acknowledgements
Built under the mentorship of the **1M1B Foundation** and **IBM SkillsBuild**, in collaboration with the **All India Council for Technical Education (AICTE)**.
