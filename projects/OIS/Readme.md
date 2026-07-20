# Operation Iron Shield (OIS)
### DoD RMF Authorization Package | GRC Portfolio Project

**Author:** Ashley Miller  
**Frameworks:** NIST SP 800-53 Rev 5 | NIST RMF | FISMA | FedRAMP | 32 CFR Part 2002 | DoDI 8510.01  
**Platform:** AWS GovCloud  
**Classification:** Unclassified — Portfolio Demonstration Project  
**Status:** Active — Artifacts In Development  

---

## Project Overview

Operation Iron Shield (OIS) is a fictional DoD program supporting a web-based case management system that processes and stores Controlled Unclassified Information (CUI). The system is hosted on AWS GovCloud and accessed by 47 government users across three locations — Washington D.C., San Antonio TX, and a remote workforce.

This project demonstrates the full NIST Risk Management Framework (RMF) authorization lifecycle for a DoD information system — from initial system categorization through control implementation documentation. All artifacts follow federal authorization package standards and reflect real-world ISSO documentation practices.

---

## Scenario

> You have been assigned as the ISSO for OIS-CMS. The system has been operational for two years supporting 47 DoD users across three locations processing CUI case records on AWS GovCloud. The system has never undergone a formal RMF authorization. Your mission is to build the authorization package and get the system to an ATO.

---

## System Profile

| Field | Value |
|---|---|
| System Name | Operation Iron Shield Case Management System |
| System Abbreviation | OIS-CMS |
| Unique Identifier | OIS-CMS-001 |
| System Type | Major Application |
| Operating Environment | AWS GovCloud (FedRAMP High) |
| Data Classification | Controlled Unclassified Information (CUI) |
| Impact Level | MODERATE — per FIPS 199 |
| Control Baseline | NIST SP 800-53 Rev 5 Moderate |
| User Population | 47 DoD Government Users |
| Locations | Washington D.C. \| San Antonio TX \| Remote Workforce |
| System Status | Operational — Authorization Pending |

---

## AWS Architecture

| Component | AWS Service | Security Function |
|---|---|---|
| Web Application | AWS Elastic Beanstalk | Hosts the internet-facing case management application |
| Database | Amazon RDS | Stores CUI case records encrypted at rest |
| Encryption | AWS Key Management Service (KMS) | Manages encryption keys for data at rest and in transit |
| Audit Logging | AWS CloudTrail | Immutable audit record of all API calls and system activity |
| Monitoring & Alerting | AWS CloudWatch | Real-time system health monitoring and threshold alerting |
| Network Security | AWS VPC \| Security Groups \| WAF | Network boundary protection and malicious traffic filtering |
| Identity & Access | AWS IAM | Infrastructure-level identity and access management |

---

## FIPS 199 Security Categorization

| Security Objective | Rating | Rationale |
|---|---|---|
| Confidentiality | MODERATE | Unauthorized disclosure of CUI could harm individuals, damage agency operations, or compromise national security activities |
| Integrity | MODERATE | Unauthorized modification of case records could result in incorrect decisions being made on corrupted government data |
| Availability | MODERATE | 47 DoD users across three locations depend on the system for mission-critical functions — extended outage disrupts operations |
| **Overall Categorization** | **MODERATE** | High water mark across all three objectives per FIPS 199 methodology |

---

## Applicable Compliance Frameworks

| Framework | Applicability |
|---|---|
| FISMA | Foundational federal law requiring information security programs for all federal systems |
| NIST SP 800-37 Rev 2 | Defines the six-step RMF process governing this authorization package |
| FIPS 199 | Establishes the security categorization methodology — system categorized as Moderate |
| FIPS 200 | Establishes minimum security requirements for Moderate impact systems |
| NIST SP 800-53 Rev 5 | Provides the Moderate control baseline implemented by OIS-CMS |
| FedRAMP | Governs cloud service authorization — OIS-CMS hosted on AWS GovCloud FedRAMP High |
| 32 CFR Part 2002 | Establishes CUI handling, safeguarding, and dissemination requirements |
| DoDI 8510.01 | Implements RMF for DoD IT including eMASS authorization package requirements |

---

## Authorization Package Deliverables

### ✅ 1. System Security Plan (SSP)
Eight-section federal SSP documenting the complete security posture of OIS-CMS including system identification, FIPS 199 categorization, system architecture, AWS inherited controls, system interconnection policy, compliance framework stack, and five control implementation statements.

**Controls Documented:** AC-2 \| IA-2 \| AU-2 \| SC-8 \| IR-4

**File:** `OIS_CMS_SSP_v1.docx`

### 🔄 2. Security Control Traceability Matrix (SCTM)
Spreadsheet mapping all applicable NIST SP 800-53 Rev 5 Moderate baseline controls to their implementation status, control type (inherited/hybrid/system-specific), responsible owner, and evidence artifacts.

**File:** [OIS_CMS_SSP_v1.docx](./OIS_CMS_SSP_v1.docx)

### 🔄 3. Plan of Action and Milestones (POA&M)
RMF Step 5 compliant POA&M tracking all identified control weaknesses with risk ratings, remediation owners, milestone steps, and projected completion dates.

**File:** `OIS_CMS_POAM_v1.xlsx` — Coming Soon

### 🔄 4. ATO Recommendation Memo
Formal memorandum summarizing the security posture of OIS-CMS and providing an authorization recommendation to the Authorizing Official.

**File:** `OIS_CMS_ATO_Memo_v1.docx` — Coming Soon

---

## Control Implementation Summary

| Control | Family | Type | Status |
|---|---|---|---|
| AC-2 | Access Control — Account Management | Hybrid | ✅ Documented |
| IA-2 | Identification & Authentication | Hybrid | ✅ Documented |
| AU-2 | Audit & Accountability — Event Logging | Hybrid | ✅ Documented |
| SC-8 | System & Communications — Transmission Protection | Hybrid | ✅ Documented |
| IR-4 | Incident Response — Incident Handling | System-Specific | ✅ Documented |

---

## Key Security Decisions

**Why Moderate and not High:**
OIS-CMS processes CUI but the potential impact of a confidentiality, integrity, or availability failure — while significant — does not rise to the level of loss of life, major financial damage, or catastrophic national security harm required for a High categorization under FIPS 199.

**Why AWS GovCloud:**
AWS GovCloud holds a FedRAMP High authorization providing OIS-CMS with a strong inherited control foundation for physical security, infrastructure protection, and core cloud service security — significantly reducing the system-specific control burden while meeting DoD cloud hosting requirements.

**Why no interconnections at launch:**
OIS-CMS launched with a self-contained boundary to minimize initial attack surface and risk exposure. A pending Active Directory interconnection will be governed by a fully executed ISA and MOU with verification of the connecting system's active ATO and current security assessment results before implementation.

---

## Skills Demonstrated

- NIST RMF lifecycle execution — Steps 1 through 5
- FIPS 199 security categorization with mission impact analysis
- AWS GovCloud shared responsibility model and inherited control analysis
- Federal SSP authorship — eight sections to federal documentation standard
- NIST SP 800-53 Rev 5 control implementation statement development
- DoD compliance framework stack — FISMA through DoDI 8510.01
- System interconnection governance — ISA and MOU requirements
- Incident response lifecycle — NIST SP 800-61 Rev 2 alignment
- CUI handling requirements — 32 CFR Part 2002

---

## Tools & Technologies

AWS GovCloud \| AWS IAM \| AWS CloudTrail \| AWS CloudWatch \| AWS KMS \| AWS WAF \| AWS VPC \| NIST SP 800-53 Rev 5 \| NIST RMF \| FISMA \| FedRAMP \| 32 CFR Part 2002 \| DoDI 8510.01

---

*Part of the Ashley Miller GRC & Cybersecurity Portfolio*  
*[← Back to Portfolio](../../README.md)*
