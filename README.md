# Hi, I'm Bakary 👋

**DevSecOps Engineer | Security Engineer** · Birmingham, UK

I build security into the software delivery lifecycle, from code commit to cloud infrastructure. I think in systems: how things connect, where they break, and how to make them resilient.

My approach is practical and builder-focused. I don't just flag vulnerabilities. I design the pipelines, policies, and monitoring that prevent them, and then I test those controls to prove they actually fire. I'm passionate about helping engineering teams *understand* security rather than just comply with it.

---

### 🔐 Featured Work

**[SecureStack Platform](https://github.com/baks7101/securestack-platform)** · the security platform
A reusable GitHub Actions security pipeline that any repo can call, plus the AWS infrastructure it protects.
- **Pipeline:** Gitleaks, CodeQL, Semgrep (custom rules), Trivy SCA, dependency pin checks, Checkov IaC scanning, container scanning, AI governance checks, AI-BOM validation, OWASP ZAP DAST, and a security gate that reports every stage result
- **Supply chain:** SBOM generation (Syft, CycloneDX) with Grype vulnerability scanning
- **Infrastructure:** modular Terraform (VPC, EKS, security modules), Kubernetes hardening, OPA/Conftest policy checks, ArgoCD GitOps, Secrets Manager with External Secrets Operator
- **Detection and response:** Fluent Bit to OpenSearch SIEM, Prometheus and Grafana, GuardDuty to Lambda SOAR, Slack alerts on failed security gates
- **Governance:** finding severity policy, an incident response runbook based on NIST SP 800-61, and compliance mapping to ISO 27001, SOC 2, and NIST CSF

**[ai-vibecode-lab](https://github.com/baks7101/ai-vibecode-lab)** · the product it protects
A deliberately vulnerable Node.js patient triage API demonstrating the OWASP Top 10 for LLM Applications.
- Runtime prompt injection detection with LLM-Guard (fail-closed), instrumented with Prometheus metrics
- AI-BOM manifest checked against a security-team approved list on every PR, so unapproved models, frameworks, or MCP servers block the merge
- Calls SecureStack's pipeline via `workflow_call`, mirroring how a central security team serves product teams

**[SecureStack Threat Model](https://github.com/baks7101/securestack-platform/blob/main/security/docs/threat-model.md)** · the design-time view
A STRIDE threat model of the platform, written to decide which controls to build before building them.
- Maps the data flow from browser through the API to the database, Secrets Manager, and audit logging
- Covers all six STRIDE categories: spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege
- Ties each threat to the component it targets, the control that mitigates it, and whether that control is implemented or still planned

---

### 🧪 How I Test My Own Controls

Every control gets its own `test/*` branch that plants one vulnerability (a committed secret, a vulnerable dependency, an unapproved AI component) to prove the pipeline catches it and blocks the merge. Doing this found real problems I have since fixed:
- A security gate that could pass without checking every stage, and later one that silently never ran
- A Semgrep rule that missed a real hardcoded API key while flagging a harmless default
- A scanner that showed green because it never actually scanned anything, so I removed it and documented why

---

### 🛠️ Tools & Tech

`GitHub Actions` `Terraform` `AWS` `EKS` `Kubernetes` `ArgoCD` `Docker` `Node.js` `Python` `Semgrep` `CodeQL` `Gitleaks` `Trivy` `Checkov` `Syft` `Grype` `OWASP ZAP` `OPA/Conftest` `LLM-Guard` `Prometheus` `Grafana` `OpenSearch` `GuardDuty`

---

### 📜 Certifications

`CompTIA Security+` `AWS Cloud Practitioner` `HashiCorp Terraform Associate` `Google Cybersecurity Certificate` `Cyber Agoge DevSecOps` 

---

### 📫 Reach Me

- 💼 [LinkedIn](https://www.linkedin.com/in/bakary-sillah-4877ab124)
- 📧 bsillah15@gmail.com
- 🔍 Open to Security Engineer and DevSecOps roles in the UK
