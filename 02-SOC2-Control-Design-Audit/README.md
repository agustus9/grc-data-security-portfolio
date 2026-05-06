# 🛡️ SOC 2 Type II Control Design & Evidence Lifecycle

## 📋 Business Scenario & Objective
To satisfy third-party risk assessments, the organization undergoes an annual **SOC 2 Type II** audit evaluating the **Security** Trust Services Criteria.

**The Challenge:** Transitioning the enterprise from reactive evidence collection to a continuous state of compliance monitoring.
**The Solution:** I served as the principal owner for the end-to-end SOC 2 audit lifecycle, converting raw technical logs into verified audit artifacts.

---

## 🛠️ Implementation & Technical Controls

### 1. Access Control Evidence Mapping
Using **Microsoft Entra ID** and **Active Directory**, I gathered point-in-time and historical artifacts to validate our core identity controls:

```text
[Terminated Worker HR Event] ──> [SailPoint/Entra ID Revocation] ──> [Entra Sign-in Logs Output]
                                                                                │
                                                                                ▼
                                                                  [Verified Access Revocation Log]
```

* **Joiner/Leaver Validation:** Extracted user creation logs and immediate termination reports from **Entra ID** to prove zero-day access revocation.
* **Role-Based Provisioning:** Audited RBAC groups to verify no users were granted standing administrative access.

### 2. Operational Control Evidence
* **Vulnerability Scanning:** Extracted reports from **Qualys VMDR** to prove all systems are scanned weekly and high-risk items are patched within SLA.
* **Incident Log Triage:** Pulled incident response reports from **ServiceNow** to document that security incidents follow the SANS/NIST containment playbook.

---

## 📉 Business Value & Risk Reduction
* **100% Audit Adherence:** Completed the SOC 2 Type II assessment with zero major exceptions.
* **Automated Evidence Generation:** Reduced engineering overhead by using continuous monitoring tools to capture security events.
