# Threat Landscape — Lesson 2 Revision Sheet

## 1. Core Terminology

| Term | Definition | Example |
|---|---|---|
| Threat actor | An individual or group capable of carrying out harmful activity | A cybercriminal |
| Threat | A potential cause of harm to a system or organization | An attempt to steal customer data |
| Threat category | A broad classification of harmful activity | Malware or credential theft |
| Attack vector | The route or method used to reach a target | A phishing email |
| Vulnerability | A weakness that could be exploited | An unpatched software flaw |
| Security control | A measure that reduces risk | Phishing-resistant MFA |
| Impact | The harm caused by an incident | Data exposure or service disruption |
| Risk | The potential for harm, considering likelihood and consequences | A vulnerable application exposing customer records |
| Indicator of compromise (IOC) | An observable artifact or signal associated with possible malicious activity | A known malicious IP address or file hash |

**Remember:** A threat actor is not a threat category. An attack vector is not a vulnerability. A suspicious indicator is not proof of a successful attack.

## 2. Common Threat Categories

### Malware
Malicious software designed to perform unauthorized or harmful actions, such as stealing information, disrupting services, or providing unauthorized access.

**Relevant controls:** Endpoint detection and response (EDR), application control, least privilege, patching, and tested backups.

### Phishing and Social Engineering
Techniques that manipulate people into disclosing information, executing actions, or granting access.

**Relevant controls:** Phishing-resistant MFA, email filtering, verification procedures, and security awareness training.

### Credential Theft and Account Compromise
Obtaining or abusing passwords, tokens, or other authentication material to access accounts without authorization.

**Relevant controls:** Phishing-resistant MFA, conditional access, credential protection, authentication monitoring, and least privilege.

### Insider Threats
Harmful activity involving people with legitimate organizational access. It may be malicious, negligent, or accidental.

**Relevant controls:** Least privilege, access reviews, data loss prevention (DLP), audit logging, and separation of duties.

### Denial-of-Service (DoS/DDoS)
Overwhelming a service or its supporting resources so legitimate users cannot access it. A distributed denial-of-service attack uses multiple sources.

**Relevant controls:** Rate limiting, traffic filtering, capacity planning, and upstream or specialized DDoS mitigation.

### Software Supply-Chain Compromise
Compromising software, updates, dependencies, or distribution mechanisms to affect downstream users.

**Relevant controls:** Trusted update channels, dependency management, software provenance verification, vulnerability management, and monitoring.

## 3. Evidence-Based Investigation

1. **Observe:** Record what actually happened and when.
2. **Validate:** Check whether the event is expected or legitimate.
3. **Correlate:** Compare endpoint, network, authentication, and application evidence.
4. **Form hypotheses:** Identify plausible explanations without treating them as facts.
5. **Scope:** Determine which systems, accounts, and data may be affected.
6. **Contain:** Apply proportionate containment according to the incident response plan when warranted.
7. **Eradicate and recover:** Remove the cause, restore trusted operation, and validate recovery.
8. **Document:** State findings, evidence, uncertainty, actions, and remaining questions.

## 4. Facts Versus Hypotheses

- An unfamiliar IP connection is an observation; command-and-control (C2) is a hypothesis until supported by further evidence.
- A compromised update being installed establishes exposure, not necessarily execution of malicious behavior.
- No observed exfiltration does not prove that no data was stolen.
- A suspicious file hash, process, or IP address must be interpreted in context.
- A connection to a legitimate service does not automatically make the associated activity safe.

## 5. Knowledge Check

1. What is the difference between a threat actor and a threat category?
2. Why is a phishing email an attack vector rather than a vulnerability?
3. Does installing a compromised update prove that data was stolen? Explain.
4. Name three evidence sources that could help investigate suspicious outbound connections.
5. Why might isolating an endpoint be appropriate before every detail is confirmed?
6. What is the difference between command-and-control and data exfiltration?

## Key Principle

**Make conclusions proportional to the evidence.** Clearly distinguish observed facts, supported findings, plausible hypotheses, and unresolved questions.
