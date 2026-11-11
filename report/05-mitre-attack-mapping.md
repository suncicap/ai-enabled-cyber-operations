# MITRE ATT&CK Mapping — GTG-1002

## 1. Purpose and Scope

This document summarises the Enterprise ATT&CK techniques listed on the official MITRE campaign page C0062, associated with the GTG-1002 activity.

**Campaign:** C0062 — Anthropic AI-orchestrated Campaign  
**Activity period:** September 2025  
**Threat actor designation:** GTG-1002  
**Attribution:** MITRE describes the actor as a likely China-nexus espionage actor, based on the cited reporting. This project does not independently establish attribution.

**Primary reference:** https://attack.mitre.org/campaigns/C0062/

The table below follows the technique IDs, names and procedure descriptions in MITRE ATT&CK campaign C0062 and its linked technique pages, checked on 11 November 2026. The current framework records 27 technique and sub-technique IDs, including T1699, whose procedure example explicitly references C0062. It does not assign a tactic column to these campaign relationships; therefore, this document does not infer or add tactic assignments.

These are MITRE's published mappings based on cited reporting, not independent observations or verification by this investigation.

## 2. Technique Mapping

| Technique ID | Technique name | Use described by MITRE for C0062 |
|---|---|---|
| T1087 | Account Discovery | Claude Code queried internal database user-account tables to enumerate accounts and identify high-privilege accounts. |
| T1595.001 | Active Scanning: Scanning IP Blocks | Claude Code scanned infrastructure across IP ranges associated with target organisations. |
| T1595.002 | Active Scanning: Vulnerability Scanning | Claude Code scanned target infrastructure for potential vulnerabilities, services and endpoints. |
| T1119 | Automated Collection | Claude Code automatically collected and processed large volumes of data without human direction. |
| T1584.004 | Compromise Infrastructure: Server | Dedicated penetration-testing servers accessible through MCP supported remote command execution, tool coordination and operational state across sessions. |
| T1136.001 | Create Account: Local Account | Claude Code created a local backdoor account to maintain access. |
| T1213.006 | Data from Information Repositories: Databases | Claude Code queried internal databases and systems for proprietary information, configurations and sensitive operational data. |
| T1005 | Data from Local System | Claude Code gathered sensitive data stored on local systems, including credentials, configurations and operational data. |
| T1074.001 | Data Staged: Local Data Staging | Extracted data and operational documentation were staged in structured Markdown files on local systems before exfiltration. |
| T1587.004 | Develop Capabilities: Exploits | Claude Code researched an identified SSRF vulnerability, generated a tailored payload and developed an exploit chain. |
| T1699 | Direct Prompt Injection | The adversary entered a prompt claiming the user was an employee of a cybersecurity firm and that Claude was being used for defensive cybersecurity testing to authorise restricted operations. |
| T1567 | Exfiltration Over Web Service | Claude Code generated a summary of collected data for operator review and approval before data was exfiltrated over Claude. |
| T1190 | Exploit Public-Facing Application | A custom exploit payload targeting an identified SSRF vulnerability was deployed to gain initial access. |
| T1083 | File and Directory Discovery | Claude Code identified sensitive data in the victim environment for extraction. |
| T1592.002 | Gather Victim Host Information: Software | Claude Code catalogued services and data on discovered endpoints. |
| T1592.004 | Gather Victim Host Information: Client Configurations | Claude Code gathered details of high-value systems, including databases and workflow orchestration platforms. |
| T1590.004 | Gather Victim Network Information: Network Topology | Claude Code mapped the target infrastructure's network topology. |
| T1683 | Generate Content | Claude Code generated documentation during the operation, including discovered services, harvested credentials, sensitive data, exploitation techniques and attack progression. |
| T1046 | Network Service Discovery | Claude Code enumerated internal services and endpoints using browser automation via MCP, including databases, container registries, administrative interfaces and workflow platforms. |
| T1588.002 | Obtain Capabilities: Tool | The adversary obtained open-source penetration-testing tools, including scanners, database exploitation frameworks, password crackers and binary-analysis suites. |
| T1588.007 | Obtain Capabilities: Artificial Intelligence | The adversary obtained access to Claude Code for cyber intrusion operations. |
| T1082 | System Information Discovery | Claude Code queried databases and systems to identify proprietary information, system configurations and database types. |
| T1016 | System Network Configuration Discovery | Claude Code gathered system configuration information from discovered devices. |
| T1049 | System Network Connections Discovery | Claude Code mapped internal network architecture and access relationships. |
| T1552.001 | Unsecured Credentials: Credentials In Files | Claude Code extracted authentication certificates stored in system configuration files across compromised environments. |
| T1078 | Valid Accounts | Harvested credentials were used to authenticate to internal APIs, database systems, container registries and logging infrastructure. |
| T1078.003 | Valid Accounts: Local Accounts | Claude Code tested harvested credentials against discovered devices. |

**Counting note:** This table contains 27 distinct technique/sub-technique IDs. The sub-techniques are listed separately from their parent techniques. No additional tactic relationships are inferred here.

## 3. AI-Enabled Operational Considerations

ATT&CK structures the conventional cyber behaviours reported in this campaign. The technique list alone does not explain the operational significance of the AI-enabled workflow.

Three aspects are particularly relevant:

### Agent-supported task execution

Anthropic reported that Claude Code agents performed substantial technical tasks and adapted their actions based on intermediate results. The degree of autonomy described in the reporting should not be interpreted as the absence of human direction.

### Tool orchestration

The reported operation connected AI agents to external penetration-testing tools through Model Context Protocol (MCP) integrations. This allowed the agents to interact with tools and target environments.

### Human direction and consequential decisions

Anthropic's subsequent analysis describes human operators setting strategic objectives while agents carried out much of the tactical work. It also states that the final data extraction was human-directed.

These characteristics should be analysed alongside the ATT&CK techniques, not treated as substitutes for them.

## 4. Defensive Considerations

| Reported behaviour | Defensive focus |
|---|---|
| External scanning and reconnaissance | Attack-surface monitoring, exposure management and network detection |
| Vulnerability research and exploitation | Vulnerability management, patching and application security |
| Account discovery and credential use | Identity monitoring, MFA and privileged access management |
| Local account creation | Account-change monitoring and endpoint detection |
| Network and system discovery | Network telemetry, segmentation and behavioural detection |
| Credential harvesting | Secrets management and credential-exposure monitoring |
| Data collection and staging | Database activity monitoring and data-loss prevention |
| Exfiltration over a web service | Egress monitoring, traffic analysis and data protection |
| AI agent and tool orchestration | Agent inventory, scoped tool permissions, approval controls and audit logging |

These are recommended defensive priorities, not proof that any individual control would necessarily have prevented the campaign.

## 5. Mapping Limitations

- This document follows the techniques and procedure descriptions currently associated with MITRE ATT&CK campaign C0062, including the C0062 procedure example on the T1699 technique page.
- MITRE's campaign page cites Anthropic reporting; the framework entry is not independent corroboration of that reporting.
- Inclusion of a technique does not establish that it occurred in every targeted environment.
- The campaign page's technique list does not assign tactic labels to the technique relationships. This document therefore avoids inferring tactic relationships.
- The mapping may change as MITRE updates the campaign entry.
- This project has not independently examined victim telemetry, infrastructure or forensic artefacts.

## 6. Sources

1. MITRE ATT&CK. *Anthropic AI-orchestrated Campaign — C0062.* https://attack.mitre.org/campaigns/C0062/
2. Anthropic. (2025, November 13). *Disrupting the first reported AI-orchestrated cyber espionage campaign.* https://www.anthropic.com/news/disrupting-AI-espionage
3. Anthropic. *Mapping AI-enabled cyber threats.* https://www.anthropic.com/research/attack-navigator
