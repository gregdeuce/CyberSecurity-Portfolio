# Lab 1 — Classify the Controls

## Overview
This repository contains a revised Excel workbook for a cybersecurity lab on classifying security controls and mapping risks to mitigating controls.

## Files
- `Lab_1_Classify_the_Controls_Revised.xlsx` — workbook with three worksheets:
  - **Control Classification**: control descriptions, categories, types, and rationale.
  - **Risk Mapping**: risk scenarios, selected controls, and mapping explanations.
  - **Notes**: important classification and scope considerations.

## Results at a glance
| Control | Category | Type |
|---|---|---|
| Biometric badge reader at server room door | Physical | Preventive |
| Mandatory annual phishing awareness training | Managerial | Preventive |
| IDS on the DMZ | Technical | Detective |
| Automated nightly database backup script | Technical | Corrective / Recovery |

## Review notes
- **Backups:** The backup control is treated as corrective/recovery because it supports restoring data after an incident. Course taxonomies may label this differently.
- **Risk A:** A biometric reader at the server room door does not automatically prevent tailgating into the building. The relevant building entrance also needs appropriate access controls and anti-tailgating measures.
- **IDS:** An intrusion detection system detects and alerts; it does not ordinarily block traffic. Prevention may require an IPS or firewall rule.
- **Ransomware recovery:** Backups should be isolated or immutable where feasible, protected from unauthorized modification, and tested regularly.

## Purpose
This workbook demonstrates basic control classification and risk-to-control reasoning. It is a learning artifact, not a formal security assessment or compliance determination.

## Suggested GitHub repository structure
```text
lab-1-classify-the-controls/
├── Lab_1_Classify_the_Controls_Revised.xlsx
└── README.md
```

## How to use
1. Upload both files to the same GitHub repository.
2. Keep the workbook and README in the repository root for easy access.
3. If you later add evidence screenshots, place them in a folder such as `screenshots/` and reference them from this README.
