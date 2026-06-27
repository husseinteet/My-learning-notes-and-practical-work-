# SOC Role in Blue Team

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Bigger Picture

A SOC analyst does not operate in isolation. Understanding where the SOC sits within a company helps you see why your work matters and where you can go from here.

Security priorities vary by industry. A law firm protects confidential documents. A hospital prioritizes patient safety. A factory cannot afford downtime on its production lines. Each company builds its security structure around what it cannot afford to lose.

At the top of that structure sits the **CISO** — the person responsible for translating business needs into a security strategy and overseeing all security departments beneath them.

---

## Security Departments

Larger companies typically split security into specialized teams:

| Team | Focus |
|---|---|
| **Red Team** | Offensive — finds vulnerabilities through ethical hacking and pentesting |
| **Blue Team** | Defensive — monitors, detects, and responds to attacks |
| **GRC Team** | Governance — manages policies and ensures regulatory compliance |

---

## Inside the Blue Team

The Blue Team is purely defensive. Depending on company size, it can range from a handful of people to fifty or more. The most common departments within it are:

**Security Operations Center (SOC)**
The starting point for most careers in defensive security. The SOC handles the bulk of daily alerts and attacks.

| Level | Role |
|---|---|
| L1 Analyst | Triages alerts and escalates complex cases |
| L2 Analyst | Investigates advanced threats passed from L1 |
| Engineer | Configures and maintains tools like SIEM and EDR |
| Manager | Oversees the team and ensures smooth operations |

**Cyber Incident Response Team (CIRT)**
Called in when an incident exceeds SOC capacity. CIRT members handle breaches without relying heavily on standard tools — broad knowledge and quick judgment are essential. Also referred to as CSIRT or CERT.

**Specialized Roles**
For larger organizations with more focused needs:
- **Digital Forensics Analyst** — examines disk and memory artifacts to uncover hidden threats
- **Threat Intelligence Analyst** — tracks emerging threat groups and attack trends
- **AppSec Engineer** — ensures security is built into the software development process
- **AI Researcher** — studies AI-related threats and defensive strategies

---

## Internal SOC vs MSSP

Not every company runs its own SOC. Some outsource to a **Managed Security Services Provider (MSSP)**, which delivers SOC services to multiple clients at once.

| | Internal SOC | MSSP |
|---|---|---|
| **Pace** | Generally calmer, more focused | High-pressure, constant alert queue |
| **Tools** | Few tools, deep knowledge of each | Many tools across dozens of clients |
| **Incident exposure** | Limited — a few major incidents per year | High — breaches and attacks every week |

Both are valid starting points. MSSP builds experience faster; internal SOC offers more depth in a single environment.

---

## Career Path

Starting as SOC L1 is one of the best ways to build a foundation in defensive security. From there, the path branches:

```
SOC L1 → SOC L2 → Senior Analyst
                 → SOC Engineer
                 → Incident Responder (CIRT)
                 → SOC Manager → CISO
```

The first one to two years are about gaining real exposure — real alerts, real attacks, real decisions. That experience is what prepares you for the next step, whatever direction you choose.

---

## Tips for SOC Analysts

- Learn something from every alert, even the false positives
- Think like an attacker to better understand what you are defending against
- Never assume — verify everything before closing a case
- Get involved in incidents whenever the opportunity comes up

---

## Key Terms

| Term | Meaning |
|---|---|
| CISO | Chief Information Security Officer |
| Blue Team | Defensive security team |
| CIRT / CSIRT / CERT | Cyber Incident Response Team |
| MSSP | Managed Security Services Provider |
| GRC | Governance, Risk, and Compliance |
| EDR | Endpoint Detection and Response |
| SIEM | Security Information and Event Management |

