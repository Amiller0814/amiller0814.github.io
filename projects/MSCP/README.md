# MedSecure Cloud Platform (MSCP)
### GRC Portfolio Project | Azure Healthcare Security Architecture

**Author:** Ashley Miller  
**Frameworks:** NIST SP 800-53 Rev 5 | HIPAA / HITECH | NIST RMF  
**Platform:** Microsoft Azure  
**Status:** Active — Artifacts Completed  

---

## Project Overview

The MedSecure Cloud Platform (MSCP) is a fictional Azure-hosted healthcare platform designed to demonstrate applied GRC, security architecture, and ISSO competencies. The platform simulates a real-world healthcare environment providing secure storage, processing, and transmission of electronic Protected Health Information (ePHI) for healthcare providers — supporting patient data management, appointment scheduling, and secure provider-patient communication.

This project was built to produce professional-grade GRC artifacts that reflect the documentation standards expected of an Information System Security Officer (ISSO) operating under the NIST Risk Management Framework.

---

## Platform Architecture

The MSCP Azure architecture includes the following components:

| Layer | Components |
|---|---|
| Identity & Access | Microsoft Entra ID, MFA, RBAC, Privileged Identity Management (PIM) |
| Core Services | Azure App Service, Azure API Management |
| Data & Storage | Azure SQL Database, Azure Blob Storage, Azure Key Vault |
| Security & Monitoring | Microsoft Sentinel (SIEM), Microsoft Defender for Cloud |
| Compliance | Azure Policy, Azure Monitor, Diagnostic Logging |
| Third-Party Integration | Vendor API Gateway, BAA-covered integrations |

---

## Security Control Coverage

Controls documented span **6 security domains** aligned to NIST SP 800-53 Rev 5 and HIPAA/HITECH:

| Domain | Controls Covered |
|---|---|
| Identity & Access Management | IA-2, AC-2, AC-3, AC-6, IA-5 |
| Audit & Logging | AU-2, AU-6, AU-12 |
| System Monitoring | SI-4 |
| Cryptographic Protection | SC-12, SC-13 |
| Configuration Management | CM-2, RA-5, CA-7 |
| Third-Party & Remote Access | SA-9, AC-17 |

---

## Project Deliverables

### ✅ 1. Azure Architecture Diagram
Visual representation of the MSCP platform architecture across all security layers including identity, data, monitoring, and third-party integration boundaries.

### ✅ 2. Security Control Matrix
Excel workbook mapping 16 NIST SP 800-53 Rev 5 controls to HIPAA citations, implementation details, architecture layers, evidence artifacts, and effectiveness ratings across 6 security domains.

**File:** `MSCP_Control_Matrix_v2.xlsx`

### ✅ 3. Gap Analysis Summary
Structured analysis identifying partially effective controls, associated risks if left unaddressed, prioritized recommendations, and implementation guidance for remediation.

Controls with identified gaps: AC-6, AC-2, AU-6, SI-4, CM-2, RA-5, CA-7

**File:** `MSCP_Gap_Analysis_Risk_Register.xlsx` (Tab 1)

### ✅ 4. Risk Register
Formal risk register derived from gap analysis findings with likelihood, impact, and risk level ratings, remediation recommendations, and traceability back to originating NIST controls.

7 risks documented — 5 High, 2 Medium

**File:** `MSCP_Gap_Analysis_Risk_Register.xlsx` (Tab 2)

### ✅ 5. Plan of Action & Milestones (POA&M)
RMF Step 5 compliant POA&M tracking 10 findings across 3 tabs — Cover, Tracker, and Summary Dashboard. Findings mapped to NIST SP 800-53 controls, HIPAA citations, risk ratings, milestones, responsible POC, and remediation status.

| Risk Level | Count |
|---|---|
| 🚨 Critical | 1 |
| 🔴 High | 5 |
| 🟡 Moderate | 4 |

**File:** `MSCP_POA&M_v2.xlsx`

---

## Key Findings

**MSCP-010 — CRITICAL:** No formal incident response plan exists for the platform. Highest priority remediation item requiring development of a full IR plan aligned to NIST SP 800-61.

**MSCP-001 — HIGH:** MFA not enforced for all privileged and remote access accounts, violating HIPAA §164.312(d) Person Authentication requirements.

**MSCP-009 — HIGH:** Just-in-Time (JIT) access not enabled for administrative accounts. Remote administrative access paths undocumented and not time-limited.

---

## Skills Demonstrated

- NIST SP 800-53 Rev 5 control selection, implementation documentation, and effectiveness assessment
- HIPAA / HITECH compliance mapping and gap identification
- Azure cloud security architecture documentation
- GRC artifact development (control matrix, gap analysis, risk register, POA&M)
- RMF Step 5 POA&M lifecycle management
- Risk identification, rating, and remediation planning

---

## Tools & Technologies

Microsoft Azure | Microsoft Entra ID | Microsoft Sentinel | Microsoft Defender for Cloud | Azure Policy | Azure Key Vault | NIST SP 800-53 | HIPAA/HITECH | NIST RMF | Excel (openpyxl)

---

*Part of the Ashley Miller GRC & Cybersecurity Portfolio*  
*[← Back to Portfolio](../../README.md)*
