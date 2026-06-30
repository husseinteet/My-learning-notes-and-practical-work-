# Alert Reporting, Escalation & Communication

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Core Idea

Alert triage does not end after deciding whether an alert is a **True Positive** or **False Positive**. SOC analysts must also document their findings, communicate with the appropriate teams, and escalate serious incidents when additional investigation or remediation is required.

Good reporting and communication ensure that important information is not lost and allow senior analysts to respond quickly to real threats.

---

## The SOC Alert Workflow

A typical SOC investigation follows this workflow:

1. Receive a new alert.
2. Perform alert triage.
3. Classify the alert.
4. Write an investigation report.
5. Close the alert or escalate it to L2.
6. Continue incident response if required.

Most alerts are resolved by **SOC L1**, while only a small percentage require escalation to higher-level analysts.

---

## Alert Reporting

Alert reporting is the process of documenting the investigation and recording the analyst's findings before closing or escalating an alert.

A good report provides enough information for another analyst to understand what happened without repeating the investigation.

### Why Reporting Matters

| Purpose | Description |
|---|---|
| **Provide Context** | Helps L2 analysts quickly understand the investigation. |
| **Maintain Records** | Investigation notes remain available even after logs expire. |
| **Improve Analysis** | Writing reports encourages analysts to think critically about their conclusions. |

---

## Writing a Good Alert Report

Most SOC teams recommend using the **Five Ws** method when writing reports.

| Question | Description |
|---|---|
| **Who** | Which user or account was involved? |
| **What** | What suspicious activity occurred? |
| **When** | When did the activity happen? |
| **Where** | Which device, IP address, or application was affected? |
| **Why** | Why was the alert classified as True or False Positive? |

A clear and structured report makes investigations easier for everyone involved.

---

## Alert Escalation

Alert escalation is the process of transferring an alert from an L1 analyst to a more experienced analyst for additional investigation or response.

Escalation ensures that serious threats receive the attention they require.

---

## When Should an Alert Be Escalated?

Escalation is recommended when:

- The alert indicates an active cyberattack.
- Additional investigation is required.
- Remediation actions are needed.
- Other departments must be involved.
- The analyst is unsure how to classify the alert.

Asking for help is always better than incorrectly closing a legitimate attack.

---

## Escalation Workflow

A standard escalation process looks like this:

1. Complete the initial investigation.
2. Write a detailed report.
3. Set the correct verdict.
4. Assign the alert to the L2 analyst.
5. Notify L2 if the incident is urgent.

L2 analysts will continue the investigation using the information provided in the report.

---

## Communication in the SOC

SOC analysts regularly communicate with different departments during investigations.

Examples include:

- IT Operations
- Human Resources
- Management
- Legal teams
- System Owners

Good communication helps analysts verify suspicious activity and coordinate incident response.

---

## Common Communication Scenarios

| Situation | Recommended Action |
|---|---|
| L2 analyst is unavailable during a critical incident | Contact L2 first, then L3, then your manager if necessary. |
| User account appears compromised | Contact the user using a trusted communication method, not the compromised account. |
| Large number of alerts appear simultaneously | Prioritize alerts and inform the L2 analyst. |
| You realize you misclassified an alert | Immediately notify your L2 analyst. |
| SIEM logs are unavailable or incomplete | Investigate what you can and report the issue to the SOC Engineer or L2. |

---

## Communication Best Practices

- Keep reports clear and concise.
- Include only verified information.
- Explain your reasoning.
- Never make assumptions without evidence.
- Notify senior analysts immediately when necessary.
- Document every important action.

---

## Lab Highlights

| Question | Answer |
|---|---|
| Escalation Process | **Alert Escalation** |
| Investigation Documentation | **Alert Reporting** |
| User Who Leaked the Document | **m.boslan@tryhackme.thm** |
| Suspicious Email Sender | **support@microsoft.com** |
| Current L2 Analyst | **E.Fleming** |

---

## Challenge Flags

| Challenge | Flag |
|---|---|
| Alert Report | `THM{nice_attempt_faking_microsoft_support}` |
| First Escalation | `THM{good_job_escalating_your_first_alert}` |
| Second Escalation | `THM{looks_like_webshell_via_old_exchange}` |

---

## Key Takeaway

Writing clear reports, escalating incidents appropriately, and maintaining effective communication are essential responsibilities of a SOC L1 analyst. These skills ensure that critical threats are investigated efficiently, important evidence is preserved, and senior analysts have the information needed to respond quickly.

---

## Key Terms

| Term | Definition |
|---|---|
| **Alert Reporting** | Documenting investigation findings and conclusions. |
| **Alert Escalation** | Transferring an alert to a higher-level analyst for further investigation. |
| **Five Ws** | A reporting method using Who, What, When, Where, and Why. |
| **SOC L1** | First-line analyst responsible for monitoring and triaging alerts. |
| **SOC L2** | Analyst responsible for advanced investigation and incident response. |
| **True Positive (TP)** | A confirmed malicious security event. |
| **False Positive (FP)** | Legitimate activity incorrectly identified as malicious. |
| **Incident Response** | The process of identifying, containing, eradicating, and recovering from security incidents. |
