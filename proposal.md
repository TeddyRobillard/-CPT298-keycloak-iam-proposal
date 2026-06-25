# Project Proposal

## 1. Project Identification

•    Project Title: Keycloak IAM Solution
•    Course: CPT 298
•    Term: Summer 2026
•    Student Name(s): Jeremie Onanga, Theodore (Teddy) Robillard
•    Primary Contact:
•    Proposed Start Date: 06/04/2026
•    Proposed End Date: 07/05/2026

---

## 2. Project Selection & Motivation

Describe why you selected this project and why you are a good fit.
Include:
•    Personal or professional motivation
•    Alignment with career goals
•    Relevant interests or prior exposure
Project topic was suggested by Jeremie, and he has an interest in cybersecurity. 
Theodore has a background in networking. 

---

## 3. Problem Statement
cpt.internal lacks centralized IAM—each service manages its own accounts independently. This forces users to maintain separate credentials for every tool, makes provisioning and deprovisioning error-prone, prevents centralized auditing, and blocks consistent security policies. All cpt.internal users (students, instructors, admins) are affected. This fragmentation increases security risk, wastes operational resources, prevents students from learning enterprise IAM practices, and doesn't scale. Deploying a unified IAM solution like Keycloak addresses these gaps by centralizing authentication, enabling consistent policies, and providing comprehensive audit trails.

---

## 4. Proposed Solution Overview
We will deploy Keycloak as the centralized IAM solution for cpt.internal. It will act as the Identity Provider (IdP) for one integrated service, enabling SSO via OpenID Connect.
Core features
SSO for one internal service via OIDC
Centralized user/group management in a dedicated realm
Role-Based Access Control (RBAC)
Strong authentication policies (passwords, brute-force protection, sessions)
Audit logging
HTTPS via reverse proxy + TLS
PostgreSQL backend
Security audit (config review + automated scan)
Documentation in UVDesk and deployment guide
Explicit exclusions
LDAP/AD deployment from scratch
Self-service password reset
Modification of integrated services
Manual penetration testing of integrated services beyond the configuration audit
and as a stretch goal to implement MFA


## 5. Technical Stack & Tools

OS: Linux on cpt.internal VMs
Languages: Bash for scripts; Python for optional automation
Frameworks: Keycloak (container or distribution)
Database: PostgreSQL
Infrastructure: Docker, reverse proxy (Nginx or Caddy)
Tools: Git/GitHub, GitHub Issues, UVDesk, Discord, Keycloak admin console + REST API
For audit: OWASP ZAP, testssl.sh, nmap, Keycloak hardening guide


## 6. Prerequisite Knowledge & Skills
Jeremie Onanga:
Skills I already have

Linux system administration (Debian, Ubuntu, Arch), Cisco networking fundamentals (VLANs, ACLs, OSPF, NAT, EtherChannel), Python and Bash scripting, penetration testing basics,...
Skills I need to learn

OAuth 2.0 and OpenID Connect (authorization code flow, PKCE), SAML 2.0, JWT (structure, validation, attacks), Keycloak administration (realm setup, client configuration, policies, federation), LDAP basics, CVSS scoring.

Relevant coursework

CPT 201 (Linux administration), CPT 239 (Cisco networking), CPT 271 (Network Security), CPT 281 (Penetration Testing).
Prior projects
 Arch Linux Local AI Services Station (Ollama, Docker, systemd services), CPT 281 lab work.


 Teddy Robillard:
 
 Skills I have: 
  Linux skills (Debian), Cisco networking fundamentals (VLANs, ACLs, OSPF, NAT, EtherChannel), and Python and Bash scripting

 Skills I need: 
  OAuth 2.0 and OpenID Connect (authorization code flow, PKCE), SAML 2.0, JWT (structure, validation, attacks), Keycloak administration (realm setup, client configuration, policies, federation), LDAP basics, CVSS scoring.

---

## 7. Project Scope & Deliverables
MVP: 
Keycloak deployed with PostgreSQL and HTTPS
One realm configured with users, roles, and policies
One service integrated via OIDC, end-to-end validated
Audit logging enabled
Security audit report (config review + automated scan)
Documentation: README, deployment guide, UVDesk articles, admin runbook

Required outputs: 
GitHub repository
UVDesk articles
Security audit report
Final presentation

Stretch goals: 
MFA (TOTP) for admin accounts
Second service integration
LDAP/AD federation (if existing directory available)


## 8. Milestones & Timeline

- Phase 1: Research & Design 6/21/26 to 6/24/26
- Phase 2: Core Implementation 6/25/26 to 7/1/26
- Phase 3: Testing & Refinement 7/2/26 to 7/5/26
- Phase 4: Documentation & Presentation 7/5/26



---

## 9. Risks, Constraints & Dependencies

- July 5th is not very far out.
- We will probably need Admin excess
- to mitigate these problems we will work on this as a top priority  

---

## 10. Security, Ethics & Safety Considerations

- Authentication and authorization: Might be needed to set up 
- Data sensitivity: Might be needed to set up
- Network exposure: N/A
- Logging, monitoring, or automation impact: Might break some of this, but probably won't
- Ethical considerations: N/A


---

## 11. Team Structure (If Applicable)

Roles
Jeremie — Security & Integration Lead: threat model, Keycloak config (realm, policies, RBAC), audit logging, OIDC integration, security audit, coordination

Theodore — Infrastructure & Documentation Lead: Keycloak deployment, PostgreSQL, reverse proxy + TLS, network, documentation (README, deployment guide, UVDesk)

Communication
Weekly async Discord status update
at least 1 short call/week
GitHub Issues for tracking
Decisions in DECISIONS.md

Conflict resolution
Discussed at scheduled calls
Blockers unresolved within 24h → escalated to instructor

Workload distribution
Clear owner per deliverable, peer review
Weekly check for overload
Critical path drives priorities



## 12. Documentation & Knowledge Transfer Plan

 README, deployment guide, UVDesk articles, and admin runbook will all be used.


## 13. Faculty/cpt.internal Resources Requested


VM access + sudo (already provided)
Confirmation of OS and VM specs
Internal DNS support (e.g. keycloak.cpt.internal)
Connectivity between our VMs and target service
Service to integrate + admin credentials
Submission channel confirmation
Instructor availability for check-ins


## 14. Acknowledgement of Expectations
By submitting this proposal, I acknowledge that:
- This is a self-directed technical project
- I am responsible for research and troubleshooting
- Evaluation will consider process, documentation, and professionalism

**Signature (Name & Date):**

Student 1:  ____________________________ Date: _______________
Student 2:  Theodore Robillard Date: 6/21/2026
Student 3:  ____________________________ Date: _______________
Student 4:  ____________________________ Date: _______________

Instructor: ____________________________ Date: _______________
