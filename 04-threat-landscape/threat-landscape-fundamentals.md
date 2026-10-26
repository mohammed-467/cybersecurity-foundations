# Threat Landscape Fundamentals

## 1. Introduction

The cybersecurity threat landscape is the set of potential threats, threat actors, attack methods, vulnerabilities, and risks relevant to a system or organization.

Security professionals study these elements to understand how harm could occur, identify weaknesses, prioritize defensive measures, and investigate suspicious events.

A disciplined analysis separates what is known, what is suspected, and what has been demonstrated by evidence.

## 2. Why the Threat Landscape Matters

Organizations depend on information systems to store data, communicate, deliver services, and conduct business.

Threats can affect the confidentiality, integrity, and availability of these systems and their information.

Understanding the threat landscape helps organizations:

- Identify important assets and potential threats.
- Recognize weaknesses that require remediation.
- Prioritize security controls according to risk.
- Prepare for potential incidents.
- Investigate suspicious activity systematically.
- Reduce the likelihood and impact of security incidents.

## 3. Core Terminology

### 3.1 Threat

A threat is a potential cause of harm to an asset, system, individual, or organization.

Threats can arise from malicious activity, human error, technical failures, or environmental events.

**Example:** A cybercriminal attempts to obtain unauthorized access to a company's customer database.

The threat describes the potential for harm. It does not establish that the attacker succeeded.

### 3.2 Threat Actor

A threat actor is an individual, group, or other entity that can initiate activity affecting the security of a system.

Threat actors may include:

- Cybercriminals motivated by financial gain.
- State-sponsored groups pursuing strategic objectives.
- Malicious insiders abusing legitimate access.
- Hacktivists pursuing political or social objectives.
- Authorized security testers operating within an agreed scope.

Not every threat actor has the same motivation, resources, capability, or level of access.

**Example:** A cybercriminal sends a fraudulent email to persuade an employee to disclose login credentials.

### 3.3 Vulnerability

A vulnerability is a weakness in a system, implementation, configuration, procedure, or security control that could be exploited or triggered.

Examples include:

- Unpatched software containing a known security flaw.
- An exposed service with inadequate access restrictions.
- Weak authentication requirements.
- Excessive permissions assigned to an account.
- Incorrectly configured cloud storage.
- Insufficient monitoring of important security events.

A vulnerability represents a weakness, not proof of exploitation.

### 3.4 Attack Vector

An attack vector is a route or method through which an attacker attempts to reach a target or carry out an attack.

Examples include:

- Phishing emails.
- Malicious websites or links.
- Exploitation of an exposed network service.
- Compromised credentials.
- Malicious attachments.
- Removable media.

An attack vector describes the method of access or attack. It is not necessarily a vulnerability itself, although a weakness may make the attack more likely to succeed.

### 3.5 Risk

Cybersecurity risk concerns the potential for adverse consequences when a threat affects a system or organization.

Risk assessment commonly considers:

- **Likelihood:** How likely the adverse event is to occur in the circumstances being assessed.
- **Impact:** The severity of the consequences if the event occurs.
- **Exposure and controls:** Factors that influence the likelihood or consequences.

A simple conceptual model is:

**Risk depends on likelihood and impact.**

This is not a universal numerical formula. Organizations may use qualitative ratings, quantitative models, or defined risk-assessment methodologies.

**Example:** An internet-facing system containing sensitive customer information may present substantial risk if it has an exploitable weakness and inadequate access controls.

### 3.6 Security Control

A security control is a safeguard or countermeasure intended to prevent, detect, or reduce the impact of security problems.

Examples include:

- Multifactor authentication (MFA).
- Least-privilege access.
- Security updates and patch management.
- Email filtering.
- Network segmentation.
- Logging and monitoring.
- Tested backups and recovery procedures.

Controls reduce risk but do not necessarily eliminate it.

## 4. How the Concepts Relate

Consider an organization that stores customer records in a web application.

1. **Asset:** The customer database and its information.
2. **Threat actor:** A cybercriminal seeking valuable information.
3. **Threat:** Unauthorized access and possible disclosure of customer records.
4. **Vulnerability:** A flaw in the application or an inadequate access-control configuration.
5. **Attack vector:** A request sent through the web application to attempt to exploit the weakness.
6. **Risk:** Potential harm to customers and the organization, assessed using likelihood and impact.
7. **Security controls:** Patching, access restrictions, secure development, monitoring, and incident-response procedures.

This example describes a possible attack scenario. It does not establish that an attack occurred or that the database was compromised.

## 5. Example: Phishing and Credential Theft

An employee receives an email that appears to come from the organization's IT department. The email directs the employee to a fraudulent sign-in page.

The employee enters their password.

### Analysis

| Element | Example |
|---|---|
| Threat actor | The person operating the phishing campaign |
| Threat | Unauthorized account access |
| Attack vector | The phishing email and fraudulent sign-in page |
| Possible weakness | Inadequate email filtering, insufficient user awareness, or weak authentication protections |
| Potentially exposed asset | The employee's account and accessible organizational data |
| Preventive controls | Email filtering, security awareness, and phishing-resistant MFA |
| Limiting controls | Least-privilege permissions and restricted access to sensitive resources |
| Detective controls | Authentication monitoring and alerts for unusual sign-in activity |

The employee entering a password indicates credential exposure in this scenario. Whether the attacker actually obtained or used the credential requires further evidence.

MFA can reduce the risk of unauthorized access when a password is stolen. However, some MFA methods remain susceptible to phishing or session theft. Phishing-resistant MFA provides stronger protection.

Least privilege limits the resources an account can access, reducing potential damage if the account is compromised.

## 6. Vulnerability Does Not Equal Compromise

Finding a vulnerability does not automatically establish that a system has been compromised.

A vulnerability assessment may identify a weakness without any evidence that an attacker has exploited it.

To investigate a suspected compromise, an analyst may correlate relevant evidence, such as:

- Authentication records showing unusual or unauthorized access.
- Application logs recording suspicious requests.
- Endpoint telemetry showing unexpected process execution.
- Network records showing unusual outbound connections.
- File-integrity records showing unauthorized changes.
- Evidence of unauthorized data access or transfer.

Evidence must be interpreted in context. A suspicious event may support an investigation without independently proving a successful attack.

A disciplined analyst distinguishes between:

- **Observed fact:** What the evidence directly shows.
- **Hypothesis:** A possible explanation that needs testing.
- **Assessment:** A conclusion based on the available evidence and its limitations.
- **Confirmed finding:** A conclusion supported by sufficient, relevant evidence for the investigation's standard of proof.

The amount and type of evidence required depend on the incident and the question being investigated.

## 7. A Basic Threat Analysis Workflow

Use the following sequence when examining a security scenario:

1. **Identify the asset.** Determine what information, system, service, or business process needs protection.
2. **Define the threat scenario.** Describe the potential harmful event.
3. **Identify the threat actor or source.** Consider who or what could cause the event, without assuming attribution prematurely.
4. **Identify vulnerabilities and exposure.** Determine which weaknesses or conditions could enable the event.
5. **Identify attack vectors.** Explain how the threat could reach or affect the asset.
6. **Assess risk.** Consider likelihood, impact, existing controls, and remaining exposure.
7. **Recommend controls.** Prioritize proportionate preventive, detective, and corrective measures.
8. **Validate with evidence.** Test assumptions and distinguish potential exposure from observed activity or confirmed compromise.
9. **Document limitations.** Record what remains unknown and what additional evidence would help resolve the uncertainty.

## 8. Defensive Measures

Organizations can reduce cybersecurity risk through layered defenses.

### Prevention

- Apply security updates in a timely, risk-based manner.
- Use strong authentication and phishing-resistant MFA where appropriate.
- Enforce least-privilege access.
- Secure system configurations.
- Filter malicious email and web content.
- Reduce unnecessary network exposure.

### Detection

- Collect and protect relevant logs.
- Monitor unusual authentication events.
- Investigate unexpected processes and network connections.
- Use endpoint detection and network monitoring where appropriate.
- Establish alerts for suspicious activity.

### Response and Recovery

- Maintain an incident-response plan.
- Preserve relevant evidence.
- Contain confirmed or suspected incidents according to the response plan.
- Restore affected systems from trusted backups when necessary.
- Document lessons learned and improve controls.

The appropriate controls depend on the organization's assets, environment, threat model, and risk tolerance.

## 9. Key Takeaways

- A threat is a potential cause of harm.
- A threat actor is an entity capable of initiating activity that affects security.
- A vulnerability is a weakness that could be exploited or triggered.
- An attack vector is a route or method used to reach a target or carry out an attack.
- Risk assessment considers likelihood and impact, along with relevant conditions and controls.
- Security controls reduce risk but do not guarantee complete protection.
- A vulnerability does not prove exploitation.
- An investigation should correlate relevant evidence, test alternative explanations, and document uncertainty.
- Security conclusions should be proportionate to the evidence.

## 10. Review Questions

1. What is the difference between a threat and a vulnerability?
2. In a phishing incident, what is the attack vector, and what role does the threat actor play?
3. How can MFA reduce the risk of stolen credentials being used?
4. Why does least privilege help limit the impact of a compromised account?
5. Why does discovering an unpatched vulnerability not prove that a system has been compromised?
6. Name three types of evidence an analyst might examine when investigating a suspected compromise.
7. Explain how likelihood and impact contribute to risk assessment.

## References

See [References](references.md) for authoritative terminology and defensive guidance.
