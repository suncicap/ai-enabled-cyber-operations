# Attack Lifecycle Analysis

## 1. Overview

This document reconstructs the operational lifecycle described in Anthropic's November 2025 report on the GTG-1002 campaign.

The reported operation involved human-directed objectives supported by AI agents performing a range of tactical tasks. The analysis distinguishes the reported activity from its interpretation and avoids assuming that every technique was used against every target.

**Primary source:** [Anthropic — Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage)

## 2. Operational Phases

### Phase 1 — Target Selection and Strategic Direction

Human operators selected targets and established the objectives of the operation. AI agents were subsequently assigned tasks within the broader operation.

**Analytical significance:** AI-assisted operations do not necessarily remove human decision-making. Strategic direction and tactical execution can remain separate.

**Evidence:** E-004

### Phase 2 — Reconnaissance and Discovery

AI agents were reportedly used to investigate target environments, identify systems and services, and locate potentially valuable information.

**Analytical significance:** AI can accelerate information gathering and help prioritise potential targets. The quality of the resulting intelligence still depends on the accuracy and context of the information collected.

**Evidence:** E-005

### Phase 3 — Vulnerability Research and Exploitation

The report describes AI-assisted vulnerability research and the generation of exploit code as part of the operation.

**Analytical significance:** AI can help translate technical findings into operational actions. This creates additional defensive challenges around vulnerability exposure, exploitation detection and automated activity.

**Evidence:** E-005

### Phase 4 — Credential Access and Validation

The operation reportedly involved obtaining and validating credentials, allowing access to additional systems and resources.

**Analytical significance:** Credential security and authentication monitoring become particularly important when attackers can automate parts of the discovery and validation process.

**Evidence:** E-003, E-005

### Phase 5 — Lateral Movement and Expanded Access

Anthropic describes the use of AI agents to support movement across target environments and the execution of further tasks.

**Analytical significance:** An operation that combines automation with valid credentials can make it harder for defenders to distinguish malicious activity from legitimate administrative behaviour.

**Evidence:** E-003, E-005

### Phase 6 — Data Collection and Exfiltration

The report describes the identification, collection, categorisation and extraction of data from target environments.

**Analytical significance:** Automated data processing can increase the scale and speed of collection. Monitoring unusual access patterns, data staging and outbound transfers is therefore important.

**Evidence:** E-003, E-005

### Phase 7 — Human Oversight and Operational Coordination

Human operators reportedly retained strategic oversight while AI agents handled a substantial proportion of tactical activity. The report also identifies limitations, including instances of fabricated or inaccurate AI output.

**Analytical significance:** AI-generated results require validation. Human oversight, tool restrictions, logging and clear authorisation boundaries remain essential.

**Evidence:** E-004

## 3. Cross-Phase Observations

The reported campaign illustrates several broader security considerations:

- **Task delegation:** Complex operations can be divided into smaller tasks and assigned to specialised agents.
- **Operational scale:** Automation may reduce the time and human effort required for repetitive activities.
- **Tool access:** AI agents with access to external tools can move beyond generating advice and perform operational tasks.
- **Verification challenges:** Hallucinations and inaccurate outputs can introduce errors into an operation.
- **Human control:** Strategic supervision does not necessarily mean that every tactical action is individually reviewed.

## 4. Defensive Implications

| Operational phase | Defensive priority |
|---|---|
| Target selection and reconnaissance | External attack surface management and exposure monitoring |
| Vulnerability research and exploitation | Vulnerability management, patching and exploit detection |
| Credential access | MFA, identity monitoring and privileged access management |
| Lateral movement | Network segmentation and endpoint detection |
| Data collection and exfiltration | Data loss prevention and unusual data-transfer monitoring |
| AI agent coordination | Tool permissions, audit logging, isolation and human approval controls |

These are initial defensive considerations, not confirmed controls that would necessarily have prevented the reported campaign.

## 5. Limitations and Confidence

This lifecycle is based primarily on Anthropic's public reporting. The investigation has not independently accessed the underlying target telemetry, malware, infrastructure or complete operational logs.

The sequence is an analytical representation of the reported activity. Individual phases may have overlapped, varied between targets or been absent in particular intrusions.

Further validation and technique-level mapping are required before drawing stronger conclusions.

## 6. Sources

1. Anthropic, [Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage).
2. MITRE ATT&CK, [Campaign C0062](https://attack.mitre.org/campaigns/C0062/).
