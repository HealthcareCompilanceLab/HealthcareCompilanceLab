<p align="center">
  <img src="https://www.news-medical.net/image-handler/ts/20240308012538/ri/750/src/images/Article_Images/ImageForArticle_24645_17099223367073417.jpg" alt="Healthcare Compliance Checker" width="850">
</p>

<h1 align="center">🏥 Healthcare Compliance Lab</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Project-Healthcare%20Data%20Security-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Cybersecurity%20%26%20Compliance-teal?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Frameworks-HIPAA%20%7C%20PHIPA%20%7C%20NIST-purple?style=for-the-badge" />
</p>

<p align="center">
  <em>Transforming healthcare security through compliance automation, risk assessment, and data protection.</em>
</p>

<p align="center">
  <a href="#about-this-project">About</a> •
  <a href="#project-overview">Overview</a> •
  <a href="#why-this-project-matters">Motivation</a> •
  <a href="#how-the-tool-works">Method</a> •
  <a href="#standards-and-control-mapping">Controls</a> •
  <a href="#project-status">Status</a> •
  <a href="#weekly-milestones">Milestones</a> •
  <a href="#group-roles-and-responsibilities">Team</a>
</p>

---

## About This Project

<p align="right">
  <img src="https://media.tenor.com/1S7bWTL8VWMAAAAi/abster-coded.gif" alt="Coding GIF" width="320">
</p>

We are fourth-year Information Sciences students at **Sheridan College** with a strong interest in cybersecurity, compliance, and healthcare data protection. As part of our capstone project, we are developing the **Healthcare Data Security Compliance Checker** to connect academic learning with a practical healthcare security challenge.

The project is designed as a proof-of-concept that helps evaluate whether important security safeguards are in place in healthcare environments. It does not process or store live patient health information. Instead, it focuses on security-related indicators, compliance validation, and evidence-based reporting.

### Team Members
- **Hartej Singh Dhanjal** — Project Manager
- **Carleen Gyamfi** — Research & Compliance Lead
- **Kasinadhan Udayakumar** — Technical Lead

---

## Project Overview

The Healthcare Data Security Compliance Checker is intended to help healthcare organizations assess whether core technical safeguards are properly implemented. The tool reviews selected system configurations and security practices and compares them against expected healthcare security controls.

The system monitors security-related metadata such as:

- Login attempts
- MFA status
- Role-based access status
- Audit log availability
- Encryption status
- Backup protection
- Suspicious access indicators

The tool then generates reports that show:

- Risk level
- Compliance gaps
- Evidence collected
- Remediation recommendations

---

## Why This Project Matters

Healthcare organizations handle sensitive personal health information, which means even small weaknesses in access control, logging, or encryption can create serious privacy and security risks. This project addresses the gap between high-level regulatory expectations and the technical checks used in real systems.

The project is especially relevant for smaller healthcare organizations that may not have access to large enterprise compliance platforms. A lightweight validation tool can help them understand control gaps and prioritize corrective actions.

---

## How the Tool Works

The current prototype is a rule-based compliance checker written in Python. It evaluates predefined technical controls using system input data and weighted scoring logic.

The tool currently includes checks for:

- MFA
- TLS/HTTPS
- Audit logging
- Encrypted backups
- Password policy strength

The system also includes:

- A control bank
- Attack detection logic
- Risk scoring
- HTML report generation
- Scenario-based testing

The output is designed to be useful for both technical users and non-technical healthcare staff by combining plain-language summaries with more detailed technical findings.

---

## Standards and Control Mapping

The project uses healthcare security frameworks as reference points for mapping technical checks to regulatory expectations. These include **HIPAA**, **PHIPA**, **ISO/IEC 27001**, and **NIST SP 800-53A**.

A key design goal in Phase 2 is to map each technical control to an understandable compliance category such as:

- Access control
- Transmission security
- Audit controls
- Contingency planning
- Risk detection and response

### Example Control Map

| Tool Check | Category | Related Standard | Evidence Needed | Risk |
|---|---|---|---|---|
| MFA enabled for admin accounts | Access Control | HIPAA Technical Safeguards / NIST Access Control | Screenshot or configuration showing MFA enabled | High |
| Audit logging enabled | Audit Controls | HIPAA Audit Controls / NIST logging controls | Log settings, sample audit log | Medium / High |
| TLS/HTTPS enabled | Transmission Security | HIPAA Transmission Security | HTTPS certificate, TLS settings | High |
| Backups encrypted | Contingency Planning | HIPAA backup/security practices | Backup policy or configuration | High |
| Failed login detection | Detect / Respond | NIST CSF Detect / Respond | Login logs or alert records | Medium / High |

---

## Phase 1 Completion

During Phase 1, we completed the original project idea, proposal, research, prototype concept, and early implementation. The proposal identified the gap between regulatory requirements and real-world technical implementation in healthcare cybersecurity.

We also reviewed how **HIPAA**, **PHIPA**, **ISO/IEC 27001**, and **NIST SP 800-53A** can support structured evaluation of healthcare security controls.

Our initial Python prototype already evaluates selected controls including:

- MFA
- TLS/HTTPS
- Audit logging
- Encrypted backups
- Password policy strength

Phase 1 also included scenario testing. In Week 14, the prototype was tested by changing user responses across access control, encryption, audit logging, backup protection, and suspicious activity indicators to see how the system reacted under stronger and weaker compliance conditions.

---

## Phase 2 Direction

As we move into Phase 2, the goal is to improve the prototype into a more complete and evidence-based compliance checker.

Planned improvements include:

- Expanding the control bank with more detailed fields such as control ID, category, expected value, evidence, risk level, and remediation.
- Mapping each technical check to healthcare security areas in a more structured way.
- Improving the questionnaire so it can be used by both healthcare staff and technical users.
- Adding explanations for common cyber risks such as weak passwords, missing MFA, failed logins, suspicious IP activity, missing logs, and unencrypted backups.
- Strengthening the system diagram and documentation.
- Updating GitHub on a weekly basis.

---

## Project Status

The project is currently in the refinement stage. Phase 1 is complete, and Phase 2 focuses on improving the prototype’s usability, documentation, mapping accuracy, and reporting quality.

The next version of the system should be more organized, more evidence-based, and easier to understand from both a compliance and technical perspective.

---

## Features Completed

- Initial project proposal and scope definition.
- Prototype concept and control bank design.
- Basic Python compliance logic.
- Checks for MFA, TLS/HTTPS, audit logging, encrypted backups, and password strength.
- Weighted risk scoring.
- HTML reporting.
- Scenario-based testing.

---

## Features Still in Progress

- Expanded control bank with regulatory mapping.
- More accurate HIPAA, PHIPA, and NIST alignment.
- Background monitoring logic.
- Suspicious activity detection.
- Improved questionnaire for healthcare and non-technical users.
- Plain-language reporting improvements.
- System architecture diagram.
- Weekly GitHub documentation updates.

---

## Known Issues and Limitations

- The current prototype is still a proof-of-concept and not a production-ready compliance platform.
- The tool does not collect or store live PHI, so it evaluates security posture rather than actual clinical records.
- Some control-to-standard mappings still need refinement.
- Background monitoring may remain limited until Phase 2 is further developed.
- Testing scenarios may not yet represent every real-world healthcare environment.

---

## Weekly Milestones

**Subject to change based on professor feedback and requirements**

| Week | Planned Milestone | Evidence |
|---|---|---|
| 1 | Submit revised project plan and update GitHub README | Revised plan report, README link |
| 2 | Update system architecture diagram and finalize Phase 2 scope | Diagram, GitHub update |
| 3 | Improve questionnaires | UI screenshots |
| 4 | Expand control bank with regulatory mappings | Updated control bank / JSON |
| 5 | Add HIPAA / PHIPA / NIST mapping to each major control | Mapping table + documentation |
| 6 | Build background monitoring logic for access events | Code commit, test data |
| 7 | Add suspicious activity detection: failed logins, unusual access, missing MFA | Alert screenshots, test results |
| 8 | Improve scoring system by category and severity | Sample reports |
| 9 | Improve plain-language and technical report output | HTML / PDF report screenshots |
| 10 | Test multiple healthcare scenarios | Testing notes, screenshots |
| 11 | Prepare final report, slides, and demo script | Draft report and slides |
| 12 | Finalize project, GitHub, final demo, and submission | Final repository and presentation |

---

## Group Roles and Responsibilities

| Member | Role | Responsibilities |
|---|---|---|
| Carleen | Research and Compliance Lead | HIPAA / PHIPA / NIST mapping, documentation, testing scenarios, report writing |
| Kasi | Technical and Prototype Lead | Code implementation, Streamlit interface, monitoring logic, report generation |
| Hartej | Project Management and Presentation Lead | Weekly coordination, GitHub evidence, slides, diagrams, integration support |

---

## Collaboration

We are open to collaboration on:

- Healthcare compliance and security projects
- HIPAA / NIST implementation guidance
- Compliance automation tools
- Healthcare data governance initiatives
- Security research and proof-of-concepts

---

## Links and Resources

- Repository: [healthcare-compliance-checker](https://github.com/HealthcareCompilanceLab/healthcare-compliance-checker)
- Project documentation: add your documentation link here
- System architecture diagram: add your diagram link here
- Demo video or screenshots: add your demo link here
- Planning notes: add your planning document link here

---

<p align="center">
  <img src="https://img.shields.io/badge/Healthcare%20Security-My%20Passion-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open%20to%20Opportunities-Yes-brightgreen?style=for-the-badge" />
</p>

<p align="center">
  <strong>⭐ If you find our work valuable, please consider giving it a star! ⭐</strong>
</p>

**Last updated:** 2026-05-10

*Building safer, more compliant healthcare systems, one project at a time.*
