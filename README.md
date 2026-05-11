# 🏥 Healthcare Compliance Lab

<h1 align="left">
  <span style="color:#44AEFB;">Healthcare Compliance Lab</span>
</h1>

<h3 align="left">
  <span style="color:#44AEFB;">Healthcare Compliance & Cybersecurity Specialist</span>
</h3>

<p align="center">
  <em>Transforming healthcare security through compliance automation, risk assessment, and data protection.</em>
</p>

<p align="center">
  <a href="#about-this-project">About</a> •
  <a href="#project-overview">Overview</a> •
  <a href="#phase-1-completion">Phase 1</a> •
  <a href="#phase-2-direction">Phase 2</a> •
  <a href="#weekly-milestones">Milestones</a> •
  <a href="#group-roles">Team</a>
</p>

---

<p align="center">
  <a href="https://github.com/HealthComplianceLab/healthcare-compliance-checker">
    <img src="https://www.news-medical.net/image-handler/ts/20240308012538/ri/750/src/images/Article_Images/ImageForArticle_24645_17099223367073417.jpg" alt="Healthcare Compliance Checker" width="750">
  </a>
</p>

## About This Project

<p align="right">
  <img src="https://media.tenor.com/1S7bWTL8VWMAAAAi/abster-coded.gif" alt="Coding GIF" width="320">
</p>

We are fourth-year Information Sciences students at **Sheridan College** with a strong interest in cybersecurity, compliance, and healthcare data protection. As part of our capstone project, we are developing the **Healthcare Data Security Compliance Checker** to connect academic learning with a real-world healthcare security challenge.

The project explores how healthcare compliance frameworks such as **HIPAA**, **PHIPA**, **ISO/IEC 27001**, and **NIST SP 800-53A** can support practical technical validation. Our goal is to demonstrate how security controls, compliance requirements, and risk assessment can work together to improve the protection of sensitive healthcare information.

### Team Members
- **Hartej Singh Dhanjal** — Project Manager
- **Carleen Gyamfi** — Research & Compliance Lead
- **Kasinadhan Udayakumar** — Technical Lead

## Project Overview

The Healthcare Data Security Compliance Checker has been developed to help healthcare organizations evaluate whether important technical safeguards are properly implemented. The tool does **not** process or store live patient health information.

Instead, it checks whether selected system configurations and security practices align with healthcare security expectations. The tool runs in the background while healthcare professionals access PHI systems and collects security-related metadata such as:

- Login attempts
- MFA status
- Role-based access status
- Audit log availability
- Encryption status
- Backup protection
- Suspicious access indicators

It then evaluates these signals against healthcare security control requirements and generates plain-language and technical reports showing:

- Risk level
- Compliance gaps
- Evidence
- Remediation recommendations

## Core Safeguard Areas

- Access control
- Encryption and transmission security
- Logging and audit controls
- Backup and contingency planning

## Phase 1 Completion

During Phase 1, we completed the original project idea, proposal, research, prototype concept, and early implementation. The project proposal identified the gap between regulatory requirements and real-world technical implementation in healthcare cybersecurity.

We also outlined how frameworks such as **HIPAA**, **PHIPA**, **ISO/IEC 27001**, and **NIST SP 800-53A** support structured evaluation of healthcare security controls.

Our group also developed an initial Python-based prototype. The prototype already evaluates selected controls including:

- MFA
- TLS/HTTPS
- Audit logging
- Encrypted backups
- Password policy strength

The current code uses:

- A control bank
- System data
- Weighted risk scoring
- Attack detection logic
- HTML report generation

Phase 1 also included testing different scenarios. In Week 14, the prototype was tested by changing user responses across access control, encryption, audit logging, backup protection, and suspicious activity indicators to evaluate how the system behaved under stronger and weaker compliance conditions.

## Feedback Received

As we move forward in the Spring/Summer 2026 semester, we are focusing on improving the project's technical and compliance alignment.

The main feedback provided by Professor Syed Tanbeer was to:

- Explain how configurations are evaluated against HIPAA and NIST.
- Map configurations to real standards.
- Make the system accessible to medical staff.
- Include awareness of common cyberattacks.
- Create an overall system diagram.

## Example Control Map

| Tool Check | Category | Related Standard | Evidence Needed | Risk |
|---|---|---|---|---|
| MFA enabled for admin accounts | Access Control | HIPAA Technical Safeguards / NIST Access Control | Screenshot or configuration showing MFA enabled | High |
| Audit logging enabled | Audit Controls | HIPAA Audit Controls / NIST logging controls | Log settings, sample audit log | Medium / High |
| TLS/HTTPS enabled | Transmission Security | HIPAA Transmission Security | HTTPS certificate, TLS settings | High |
| Backups encrypted | Contingency Planning | HIPAA backup/security practices | Backup policy or configuration | High |
| Failed login detection | Detect / Respond | NIST CSF Detect / Respond | Login logs or alert records | Medium / High |

## Phase 2 Direction

Throughout Phase 2, we plan to address this feedback by:

- Expanding the control bank so each check includes a control ID, category, expected value, risk level, remediation, and regulatory mapping.
- Mapping each technical check to healthcare security areas such as access control, transmission security, audit controls, and contingency planning.
- Improving the questionnaire so the tool can be used by non-technical healthcare staff as well as IT and security users.
- Adding a section that explains common cybersecurity risks such as weak passwords, missing MFA, failed login attempts, suspicious IP activity, missing audit logs, and unencrypted backups.
- Updating GitHub weekly.

## Project Purpose

The tool is designed as a lightweight background monitoring and compliance support system for healthcare environments, especially smaller or privately funded healthcare organizations that may not have access to expensive enterprise compliance platforms.

The system will not collect or store PHI. Instead, it will monitor security-related access events, user activity patterns, configuration evidence, and control status while healthcare professionals access PHI systems.

Under PHIPA in Ontario, health information custodians must take reasonable steps to protect personal health information against theft, loss, unauthorized use or disclosure, and unauthorized copying, modification, or disposal. NIST SP 800-66 Rev. 2 is also useful because it helps organizations understand HIPAA Security Rule safeguards for protecting ePHI, regardless of the organization’s structure or method of implementation.

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
| 8 | 
