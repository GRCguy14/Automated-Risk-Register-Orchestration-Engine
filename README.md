# Automated Risk Register Orchestration Engine (ARROE)

An enterprise-grade GRC Risk Register automation project built on ServiceNow.  
The system ingests risk data from an ISO 27001-aligned ISMS risk register (CSV import), automatically calculates Inherent Risk Scores, enforces predefined risk rating thresholds, and assigns globally unique risk IDs for audit traceability.  

---

## Documentation
Full project documentation with detailed explanations:  
👉 [ARROE_Documentation.pdf](./Automated Risk Register Orchestration Engine (ARROE) (1).pdf)

---

## Architecture / Flow
- Trigger: Risk Created or Updated  
- Calculate Inherent Score (Likelihood × Impact)  
- Auto-assign Risk Rating thresholds:  
  - ≤ 8 → Acceptable  
  - 9–11 → Management Review  
  - ≥ 12 → Unacceptable – Must Treat  
- Update Risk Record  

![Flow Diagram](./https://github.com/GRCguy14/Automated-Risk-Register-Orchestration-Engine/blob/main/Screenshots/Flow-architecture.png.png)   

---

## Import Process
- Source: CSV → [NimbusTech_Risks.csv](./NimbusTech_Risks.csv)  
- Staging: `u_risk_import`  
- Transform Map: Coalesced on `Name`  
- Outcome: Updates existing risks or inserts new risks if missing  

---

## Screenshots / Evidence
- Risk Register CSV (source data)  
- Imported data in ServiceNow  
- Flow Designer automation (full diagram)  
- Risk Register list with Inherent Score, Risk Rating, Number  

*(Add these screenshots into the repo under `/screenshots/` and link them here.)*  

---

## Features
- Automated **Inherent Score calculation**  
- Automated **Risk Rating assignment**  
- **Duplicate prevention** using Coalesce  
- **Global unique risk numbering** (`NT-ISMS-RR0001`)  
- Traceability to ISO 27001 SoA controls  

---

## Portfolio Value
- Demonstrates **ServiceNow GRC automation skills**  
- Aligns with **ISO 27001 risk management** practices  
- Showcases ability to combine **governance frameworks** with **enterprise tool configuration**  

