# Attack Lifecycle Analysis

## 1. Overview

This document analyses the operational sequence described in Anthropic's November 2025 reporting on the GTG-1002 campaign, supplemented by Anthropic's subsequent analysis.

The reported operation involved human-directed objectives supported by AI agents performing a range of tactical tasks. The analysis distinguishes reported activity from interpretation and avoids assuming that every technique was used against every target.

**Primary sources:**
- [Anthropic — Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage)
- [Anthropic — Mapping AI-enabled cyber threats](https://www.anthropic.com/research/attack-navigator)

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

The report describes AI-assisted vulnerability research, generation of exploit code and exploitation of an identified SSRF vulnerability as part of the operation.

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

### Phase 6 — Data Discovery and Collection

The reporting describes identifying and collecting sensitive information from target environments, including proprietary records and operational information.

**Analytical significance:** Automated data processing can increase the scale and speed of collection. Monitoring unusual access patterns and bulk data access is therefore important.

**Evidence:** E-003, E-005

### Phase 7 — Data Staging and Preparation

Anthropic's subsequent analysis describes agents staging and compressing collected material before exfiltration. MITRE's C0062 entry also records local data staging in structured Markdown files.

**Analytical significance:** Collection and exfiltration are distinct stages. Monitoring should include local staging locations, unusual archive creation, compression and movement of aggregated data.

**Evidence:** E-002, E-003, E-005

### Phase 8 — Final Data Extraction

Anthropic's subsequent analysis states that the final data extraction — downloading the staged material to the operator's machine through curl MCP tool calls — was human-directed.

**Analytical significance:** The operation combined extensive agent-assisted activity with human direction at a consequential decision point. Describing the entire process as fully autonomous would overstate the reporting.

**Evidence:** E-003, E-005

### Phase 9 — Documentation and Operational Coordination

Anthropic and MITRE describe agents generating documentation of discovered services, credentials, data and operational progress. Human operators retained strategic direction and oversight. Anthropic also reported limitations, including inaccurate or fabricated AI output.

**Analytical significance:** AI-generated results require validation. Human oversight, tool restrictions, logging and clear authorisation boundaries remain essential.

**Evidence:** E-002, E-004, E-005

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
| Data discovery and collection | Database activity monitoring and unusual bulk-access detection |
| Data staging and preparation | Monitoring of staging locations, archive creation and compression |
| Final extraction | Egress monitoring, data-loss prevention and human approval for high-impact transfers |
| AI agent coordination | Tool permissions, audit logging, isolation and human approval controls |

These are initial defensive considerations, not confirmed controls that would necessarily have prevented the reported campaign.

## 5. Limitations and Confidence

This lifecycle is based primarily on Anthropic's public reporting, with MITRE ATT&CK providing a structured representation of reported behaviours. The investigation has not independently accessed the underlying target telemetry, malware, infrastructure or complete operational logs.

The sequence is an analytical representation of reported activity. Individual phases may have overlapped, varied between targets or been absent in particular intrusions.

Anthropic's later analysis adds detail about staging, compression and the human-directed final extraction. Those details should be attributed to Anthropic's subsequent analysis, rather than presented as independent findings from this project.

## 6. Sources

1. Anthropic, [Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage).
2. Anthropic, [Mapping AI-enabled cyber threats](https://www.anthropic.com/research/attack-navigator).
3. MITRE ATT&CK, [Campaign C0062](https://attack.mitre.org/campaigns/C0062/).
