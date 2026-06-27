# Humans as Attack Vectors

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Core Idea

Breaking into a system the technical way — exploiting vulnerabilities, bypassing firewalls — takes time, skill, and effort. Targeting a human is faster and easier. A well-crafted phishing email sent to the right person can hand an attacker full access to a corporate network within minutes.

This is why humans are consistently described as the **weakest link** in cybersecurity. Not because people are careless, but because attackers are skilled at exploiting natural human behaviors — trust, urgency, fear, and curiosity.

> A corporate network is like a fortress with thick walls and armored gates. You can breach the walls — or you can just convince the gatekeeper to open the door.

---

## Why Humans Are Targeted

Attackers go after humans because of the **access** they hold. The goal is not always the person — it is what the person can unlock.

| Target | What the Attacker Is After |
|---|---|
| HR manager's Google account | Employee database — sold or used for further attacks |
| Wealthy individual running malware | Hijacked banking session |
| IT administrator's VPN credentials | Direct access to the core corporate network |
| Government worker tricked into sharing information | Intelligence used to plan the next attack |

---

## What Is Social Engineering?

Social engineering is the technique of **manipulating people** into doing something that benefits the attacker — without needing to exploit a single technical vulnerability.

For a social engineering attack to succeed, it must be:

- **Trustworthy** — the attacker must appear legitimate so the victim does not question the request
- **Emotional** — the attack must trigger a strong feeling: urgency, fear, excitement, or curiosity

---

## Common Attack Types

### Phishing
The most widespread form of social engineering. An attacker sends an email that looks legitimate — often mimicking a bank, IT department, or familiar service — and tricks the victim into clicking a link or entering credentials on a fake login page.

- Estimated **3.4 billion** malicious emails are sent every day
- The fake page looks real but sends credentials directly to the attacker

### Malware Downloads
Victims are tricked into downloading and running malicious software, often disguised as a legitimate application. Attackers make this more convincing using:
- Fake CAPTCHA pages
- Malicious QR codes
- SEO poisoning — pushing malicious websites to the top of search results

### Deepfakes
AI-generated video or audio used to impersonate a trusted person. In a real case, a finance worker was tricked into wiring **$25 million** after receiving a deepfake video call from someone appearing to be their company's CFO requesting an urgent transfer.

### Impersonation
Without any AI, attackers simply pretend to be someone the victim trusts — a colleague, an IT support agent, or an executive. Many ransomware attacks begin with a phone call from someone claiming to be from the IT department, asking to "take over the account for a quick system repair."

### Other Attacks
Social engineering goes beyond digital channels:
- **USB drop campaigns** — leaving infected USB drives in public spaces hoping someone picks one up
- **Physical attacks** — tailgating into secured areas by pretending to be a delivery person
- **Insider threats** — employees who intentionally or unintentionally assist attackers
- **Fake job offers** — luring targets into sharing sensitive information under the guise of recruitment

---

## Defense: Mitigation vs Detection

No defense is perfect. The approach is two-layered:

**Mitigation** — reduce the chance of an attack succeeding in the first place  
**Detection** — catch the attacks that slip through mitigation

| Mitigation Measure | How It Helps |
|---|---|
| Anti-phishing solution | Automatically blocks phishing emails before users see them |
| Antivirus / EDR | Prevents malware from executing on corporate devices |
| "Trust but verify" principle | Teaches employees to question suspicious requests, even from apparent authority figures |
| Security awareness training | Educates staff on recognizing phishing and social engineering, reinforced with simulations |

---

## The SOC Analyst's Role

As an L1 analyst, your job sits on the **detection** side. When mitigation fails — and it eventually will — you are the one catching what got through.

Beyond alert monitoring, SOC analysts in more involved teams may:
- Work closely with IT and HR teams to share threat intelligence
- Propose security policy improvements
- Run company-wide security awareness training
- Operate a hotline for employees who suspect they are being targeted

---

## Key Terms

| Term | Definition |
|---|---|
| **Social Engineering** | Manipulating people psychologically to gain unauthorized access or information |
| **Phishing** | Fraudulent emails designed to steal credentials or deliver malware |
| **Deepfake** | AI-generated video or audio used to impersonate a real person |
| **Impersonation** | Pretending to be a trusted individual to manipulate a victim |
| **SEO Poisoning** | Manipulating search engine results to push malicious sites to the top |
| **EDR** | Endpoint Detection and Response — security software monitoring devices for threats |
| **Mitigation** | Actions taken to prevent or reduce the impact of an attack |
| **Insider Threat** | A risk originating from within the organization, either malicious or accidental |

