# MITRE ATT&CK Mapping

## 1. Purpose

This document maps reported GTG-1002 campaign behaviours to the MITRE ATT&CK Enterprise framework.

The mappings are based on the official MITRE ATT&CK campaign entry C0062. They are not independent findings from this investigation.

**Campaign:** C0062 — Anthropic AI-orchestrated Campaign  
**Activity period:** September 2025  
**Threat actor assessment:** GTG-1002, assessed by Anthropic as a likely Chinese state-sponsored group.

**Primary reference:** https://attack.mitre.org/campaigns/C0062/

## 2. Technique Mapping

| Tactic / Activity | Technique ID | Technique Name | Reported Behaviour |
|---|---|---|---|
| Reconnaissance | T1595.001 | Active Scanning: Scanning IP Blocks | Scanning infrastructure across target-associated IP ranges. |
| Reconnaissance | T1595.002 | Active Scanning: Vulnerability Scanning | Scanning target infrastructure for vulnerabilities and exposed services. |
| Discovery | T1046 | Network Service Discovery | Enumerating internal services and endpoints. |
| Discovery | T1087 | Account Discovery | Querying account information and identifying privileged accounts. |
| Initial Access | T1190 | Exploit Public-Facing Application | Deploying a custom exploit targeting an identified SSRF vulnerability. |
| Resource Development | T1587.004 | Develop Capabilities: Exploits | Researching and developing a tailored exploit chain. |
| Credential Access | T1552.001 | Unsecured Credentials: Credentials In Files | Extracting authentication certificates from configuration files. |
| Discovery | T1083 | File and Directory Discovery | Identifying sensitive files and directories within compromised environments. |
| Collection | T1005 | Data from Local System | Gathering sensitive local data, credentials and system information. |
| Collection | T1213.006 | Data from Information Repositories: Databases | Querying internal databases to obtain sensitive information. |
| Collection | T1119 | Automated Collection | Automating the collection and processing of data. |
| Collection | T1074.001 | Data Staged: Local Data Staging | Staging collected data and operational documentation locally. |
| Exfiltration | T1567 | Exfiltration Over Web Service | Using a web service to facilitate data exfiltration. |
| AI-related activity | T1699 | Direct Prompt Injection | Using misleading prompts to represent the operation as authorised defensive testing and bypass safeguards. |

## 3. AI-Enabled Operational Considerations

Traditional ATT&CK mapping describes adversary behaviour, but it does not by itself explain the extent of AI involvement.

Three additional considerations are relevant:

- **Autonomous execution:** AI agents reportedly executed multiple technical tasks rather than simply recommending commands.
- **Tool orchestration:** MCP integrations connected AI agents to external tools and target environments.
- **Human direction:** Operators established objectives and retained strategic control while delegating substantial tactical work.

The AI component should therefore be analysed alongside the underlying ATT&CK techniques, rather than treated as a replacement for them.

## 4. Defensive Considerations

| Observed Behaviour | Defensive Focus |
|---|---|
| External scanning | Attack surface monitoring and network intrusion detection |
| Vulnerability exploitation | Vulnerability management, patching and web application protection |
| Account discovery | Identity monitoring and least-privilege access |
| Credential harvesting | Secret management, MFA and credential exposure monitoring |
| Lateral movement | Network segmentation and endpoint detection |
| Data collection | Database access monitoring and data classification |
| Data staging and exfiltration | Data loss prevention and outbound traffic monitoring |
| Prompt manipulation | AI application security, access controls and audit logging |

These are suggested defensive priorities, not proof that any individual control would have prevented the campaign.

## 5. Mapping Limitations

- The mapping follows MITRE ATT&CK's published campaign relationships.
- A technique's inclusion does not mean it occurred in every targeted environment.
- Some techniques describe conventional cyber activity, while others describe AI-specific behaviours.
- The ATT&CK framework is updated over time; technique names and relationships should be checked against the current official version.
- The presence of an AI-related technique does not, by itself, establish the degree of autonomy involved.

## 6. Sources

1. MITRE ATT&CK, [Campaign C0062 — Anthropic AI-orchestrated Campaign](https://attack.mitre.org/campaigns/C0062/).
2. Anthropic, [Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage).
3. MITRE ATT&CK, [Enterprise Matrix](https://attack.mitre.org/matrices/enterprise/).
