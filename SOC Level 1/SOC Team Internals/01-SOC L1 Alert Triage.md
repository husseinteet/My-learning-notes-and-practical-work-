# Alert Triage

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Core Idea

Security devices generate thousands—even millions—of events every day. Reviewing each event manually would be impossible, so security solutions generate **alerts** whenever suspicious activity matches predefined detection rules. The job of a SOC analyst is not to investigate every log, but to quickly identify which alerts represent real threats and respond appropriately.

Alert triage is the process of reviewing, prioritizing, investigating, and classifying alerts to determine whether they require further action.

---

## From Events to Alerts

Every alert starts as a normal system event.

### Alert Lifecycle

1. A user or system performs an action.
2. The operating system, firewall, or application records the action as a log.
3. Logs are forwarded to a security platform such as a SIEM or EDR.
4. Detection rules analyze the incoming logs.
5. If suspicious behavior is detected, an alert is created.

Without alerts, SOC analysts would need to review millions of logs every day.

---

## Alert Management Platforms

Different security platforms can generate and manage alerts.

| Platform | Examples | Purpose |
|---|---|---|
| **SIEM** | Splunk ES, Elastic SIEM | Collects logs, correlates events, and generates alerts |
| **EDR** | Microsoft Defender, CrowdStrike | Detects suspicious activity on endpoints |
| **SOAR** | Splunk SOAR, Cortex SOAR | Automates repetitive investigation and response tasks |
| **ITSM** | Jira, TheHive | Tracks incidents and manages investigation tickets |

---

## SOC Roles During Alert Triage

Each SOC team member has a different responsibility during an investigation.

| Role | Responsibilities |
|---|---|
| **SOC L1 Analyst** | Reviews alerts, performs initial investigation, classifies alerts, escalates confirmed threats |
| **SOC L2 Analyst** | Performs deeper investigation and remediation |
| **SOC Engineer** | Maintains SIEM, creates detection rules, improves alert quality |
| **SOC Manager** | Oversees SOC operations and analyst performance |

---

## Understanding Alert Properties

Every alert contains information needed to perform the investigation.

| Property | Purpose |
|---|---|
| **Alert Time** | When the alert was generated |
| **Alert Name** | Summary of suspicious activity |
| **Severity** | Indicates business impact |
| **Status** | Shows investigation progress |
| **Verdict** | Final classification after investigation |
| **Assignee** | Analyst responsible for the alert |
| **Description** | Explains why the alert was generated |
| **Fields** | Evidence such as usernames, IP addresses, or hostnames |

---

## Alert Severity

Severity helps analysts determine which alerts should be investigated first.

| Severity | Description |
|---|---|
| 🟢 **Low** | Informational activity with minimal risk |
| 🟡 **Medium** | Suspicious activity requiring investigation |
| 🟠 **High** | Likely malicious activity affecting important assets |
| 🔴 **Critical** | Active or confirmed attack requiring immediate attention |

---

## Alert Prioritization

When multiple alerts are waiting, analysts should investigate them in the correct order.

### Recommended Workflow

1. Ignore alerts already assigned or closed.
2. Investigate **Critical** alerts first.
3. Continue with High, Medium, then Low severity.
4. If severity is equal, investigate the oldest alert first.

This approach minimizes the impact of ongoing attacks.

---

## Alert Triage Process

Alert triage follows a structured workflow.

### Initial Actions

Before beginning the investigation:

- Assign the alert to yourself.
- Change its status to **In Progress**.
- Read the alert description.
- Identify affected users and systems.

---

### Investigation

Review all available evidence.

Common investigation steps include:

- Reviewing related logs
- Identifying affected users
- Examining IP addresses
- Checking executed commands
- Looking for additional suspicious events
- Using Threat Intelligence when needed

---

### Final Actions

After completing the investigation:

- Determine whether the alert is malicious.
- Document your findings.
- Close the alert.
- Escalate confirmed incidents to L2 if necessary.

---

## Alert Classification

After investigation, every alert receives a verdict.

| Verdict | Meaning |
|---|---|
| **True Positive (TP)** | The alert represents a real security incident. |
| **False Positive (FP)** | Legitimate activity incorrectly identified as malicious. |

Correct classification is one of the most important responsibilities of a SOC L1 analyst.

---

## Best Practices

- Always assign the alert before investigating.
- Review surrounding events, not just the triggering event.
- Verify affected users and systems.
- Document every action performed.
- Escalate incidents when necessary.
- Never assume an alert is benign without evidence.

---

## Lab Highlights

| Question | Answer |
|---|---|
| Number of Alerts | **5** |
| Most Recent Alert | **Double-Extension File Creation** |
| VPN Login Verdict | **False Positive** |
| Affected User | **M.Clark** |
| First Priority Alert | **Potential Data Exfiltration** |

---

## Challenge Flags

| Challenge | Flag |
|---|---|
| First Alert | `THM{looks_like_lots_of_zoom_meetings}` |
| Second Alert | `THM{how_could_this_user_fall_for_it?}` |
| Third Alert | `THM{should_we_allow_github_for_devs?}` |

---

## Key Takeaway

Alert triage is the foundation of SOC operations. Analysts must prioritize alerts correctly, investigate available evidence, distinguish real attacks from false positives, and document their findings. Efficient alert handling enables organizations to detect and respond to threats before significant damage occurs.

---

## Key Terms

| Term | Definition |
|---|---|
| **Alert** | A notification generated when suspicious activity matches a detection rule. |
| **SIEM** | A platform that collects logs, correlates events, and generates alerts. |
| **EDR** | Endpoint Detection and Response solution used to monitor endpoint activity. |
| **SOAR** | Security platform that automates investigation and response tasks. |
| **Severity** | Indicates the potential impact of an alert. |
| **True Positive** | A confirmed malicious security event. |
| **False Positive** | Legitimate activity incorrectly classified as malicious. |
| **Alert Triage** | The process of reviewing, investigating, and classifying security alerts. |
| **Escalation** | Passing a confirmed incident to a higher-level analyst. |
| **Threat Intelligence** | Information used to identify and investigate malicious activity. |
