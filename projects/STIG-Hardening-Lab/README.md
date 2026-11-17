# STIG Hardening Home Lab

**Windows Server 2022 + RHEL 9 | DISA STIGs | SCC | STIG Viewer | Nessus**

> 🚧 **Status: In progress.** Phase 1 (building the VMs) is underway. Results, screenshots, and artifacts get added as each phase is finished.

## Overview

This hands-on lab copies the configuration compliance work an ISSO does on a DoD system. Two target systems are built from a clean install, scanned against the current DISA STIGs, and remediated. Then they're rescanned to measure the improvement. Any findings that can't be fixed get documented the same way they would be in a real RMF package: through a POA&M and a risk acceptance memo.

**Goal:** Show the full STIG lifecycle, from baseline to checklist to remediation to validation to documentation, using the same tools DoD programs use.

## Lab Environment

| Component | Details |
|---|---|
| Hypervisor | VMware Workstation Pro 26H1 |
| Network | Isolated NAT network (VMnet8), not exposed to the internet |
| Target 1 | `LAB-WS2022`: Windows Server 2022 Standard (Desktop Experience), 4 GB RAM, 2 vCPU |
| Target 2 | `lab-rhel9`: Red Hat Enterprise Linux 9 (Server with GUI), 4 GB RAM, 2 vCPU |
| Compliance tools | DISA SCAP Compliance Checker (SCC), STIG Viewer 3 |
| Vulnerability scanning | Tenable Nessus Essentials (credentialed scans) |
| Remediation | DISA GPO package, LGPO, OpenSCAP (RHEL 9 STIG profile), manual configuration |

## Methodology

| Phase | Activity | Status |
|---|---|---|
| 0 | Lab setup: hypervisor, network, STIG and tool downloads | ✅ Complete |
| 1 | Build target VMs, patch them, and take "before" snapshots | 🔄 In progress |
| 2 | Baseline SCC and Nessus scans | ⬜ Not started |
| 3 | STIG Viewer checklists and manual review of "Not Reviewed" items | ⬜ Not started |
| 4 | Remediation (GPOs and OpenSCAP, plus manual fixes for CAT I findings) | ⬜ Not started |
| 5 | Rescan and before/after comparison | ⬜ Not started |
| 6 | Artifacts: POA&M and risk acceptance/deviation memo | ⬜ Not started |

## Results

*To be filled in after Phases 2 and 5.*

| System | Metric | Baseline | After Remediation |
|---|---|---|---|
| LAB-WS2022 | SCC compliance score | — | — |
| LAB-WS2022 | Open CAT I / II / III | — / — / — | — / — / — |
| lab-rhel9 | SCC compliance score | — | — |
| lab-rhel9 | Open CAT I / II / III | — / — / — | — / — / — |

## Repository Structure

```
STIG-Hardening-Lab/
├── README.md
├── screenshots/        # SCC summaries, STIG Viewer, Nessus results
├── checklists/         # Exported STIG Viewer checklists (.cklb), sanitized
├── reports/            # SCC and Nessus summary reports, sanitized
└── artifacts/          # POA&M and risk acceptance memo
```

## Key Takeaways

*To be written after the lab is finished. Planned topics:*

- STIG compliance (SCC) vs. vulnerability scanning (Nessus/ACAS): what each one tells you
- Why automated scans leave "Not Reviewed" items, and how manual checks close them
- Choosing which findings to remediate and which to accept, and how to document that risk decision

## Skills Demonstrated

`DISA STIGs` · `SCAP / SCC` · `STIG Viewer` · `Nessus` · `Group Policy` · `OpenSCAP` · `Windows Server hardening` · `RHEL hardening` · `POA&M development` · `Risk acceptance` · `NIST SP 800-53 CM-6`

---

*Lab environment only. No production or government systems or data are used.*
