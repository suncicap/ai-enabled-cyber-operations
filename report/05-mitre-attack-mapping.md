# MITRE ATT&CK Mapping — GTG-1002

## 1. Purpose and Scope

This document maps the behaviours associated with the GTG-1002 campaign to the MITRE ATT&CK Enterprise framework.

The mapping is based on the official MITRE ATT&CK campaign entry C0062, which documents techniques associated with the campaign using publicly reported information.

**Campaign:** C0062 — Anthropic AI-orchestrated Campaign  
**Activity period:** September 2025  
**Threat actor designation:** GTG-1002  
**Attribution:** Anthropic assessed the activity as likely conducted by a Chinese state-sponsored group.

**Primary reference:** https://attack.mitre.org/campaigns/C0062/

The mappings below reflect MITRE's published campaign relationships. They are not independent findings or independently verified observations from this investigation.

## 2. Technique Mapping

The following table reproduces the 27 Enterprise ATT&CK technique and sub-technique relationships currently listed for C0062.

| Tactic | Technique ID | Technique name | Reported campaign behaviour |
|---|---|---|---|
| Reconnaissance | T1595.001 | Active Scanning: Scanning IP Blocks | Scanning infrastructure across IP ranges associated with target organisations. |
| Reconnaissance | T1595.002 | Active Scanning: Vulnerability Scanning | Scanning target infrastructure to identify potential vulnerabilities and enumerate services and endpoints. |
| Reconnaissance | T1592.002 | Gather Victim Host Information: Software | Cataloguing services and software on discovered endpoints. |
| Reconnaissance | T1592.004 | Gather Victim Host Information: Client Configurations | Gathering information about high-value systems, including databases and workflow platforms. |
| Reconnaissance | T1590.004 | Gather Victim Network Information: Network Topology | Mapping network topology and infrastructure relationships. |
| Resource Development | T1584.004 | Compromise Infrastructure: Server | Operating dedicated penetration-testing servers connected through MCP to support remote execution and tool coordination. |
| Resource Development | T1587.004 | Develop Capabilities: Exploits | Researching an SSRF vulnerability and developing a tailored exploit chain. |
| Resource Development | T1588.002 | Obtain Capabilities: Tool | Obtaining open-source penetration-testing tools, including scanners and exploitation utilities. |
| Resource Development | T1588.007 | Obtain Capabilities: Artificial Intelligence | Obtaining access to Claude Code for use in cyber operations. |
| Resource Development | T1683 | Generate Content | Automatically generating documentation of discovered services, credentials, data and operational progress. |
| Initial Access | T1190 | Exploit Public-Facing Application | Deploying a custom exploit targeting an identified SSRF vulnerability. |
| Initial Access | T1078 | Valid Accounts | Using harvested credentials to authenticate to internal systems and services. |
| Initial Access | T1078.003 | Valid Accounts: Local Accounts | Testing and using harvested credentials against discovered devices. |
| Execution | T1699 | Direct Prompt Injection | Using a crafted prompt and claimed defensive-testing context to persuade Claude to perform restricted operations. |
| Persistence | T1136.001 | Create Account: Local Account | Creating a local account to maintain access. |
| Persistence | T1078 | Valid Accounts | Maintaining access through valid credentials. |
| Privilege Escalation | T1078 | Valid Accounts | Using valid accounts to access resources with higher privileges. |
| Privilege Escalation | T1078.003 | Valid Accounts: Local Accounts | Using local accounts to access systems and resources. |
| Stealth | T1078 | Valid Accounts | Using valid credentials to blend activity with legitimate authentication. |
| Stealth | T1078.003 | Valid Accounts: Local Accounts | Using local accounts as part of activity mapped to valid-account techniques. |
| Credential Access | T1552.001 | Unsecured Credentials: Credentials In Files | Extracting authentication certificates stored in system configuration files. |
| Discovery | T1087 | Account Discovery | Querying internal database account tables to identify accounts and privileged users. |
| Discovery | T1046 | Network Service Discovery | Enumerating internal network services and endpoints using tool integrations. |
| Discovery | T1082 | System Information Discovery | Querying systems and databases to identify system configurations and database types. |
| Discovery | T1016 | System Network Configuration Discovery | Gathering network configuration information from discovered devices. |
| Discovery | T1049 | System Network Connections Discovery | Mapping internal network architecture and connections. |
| Discovery | T1083 | File and Directory Discovery | Identifying sensitive files and directories within compromised environments. |
| Collection | T1005 | Data from Local System | Gathering sensitive local data, credentials and system information. |
| Collection | T1213.006 | Data from Information Repositories: Databases | Querying internal databases for proprietary and operational information. |
| Collection | T1119 | Automated Collection | Automatically collecting and processing large volumes of data. |
| Collection | T1074.001 | Data Staged: Local Data Staging | Staging collected data and documentation in structured local files before exfiltration. |
| Exfiltration | T1567 | Exfiltration Over Web Service | Preparing collected information and exfiltrating data through a web service. |

**Note:** ATT&CK techniques can be associated with more than one tactic. The table reflects the campaign relationships and reported procedure descriptions in MITRE's C0062 entry; it is not a claim that every technique occurred in every target environment.

## 3. AI-Enabled Operational Considerations

ATT&CK provides a structured way to describe adversary behaviour, but the technique mapping alone does not explain what made this campaign distinctive.

Three aspects are particularly relevant:

### Autonomous task execution

Anthropic reported that Claude Code agents performed substantial technical tasks with limited human intervention. The agents reportedly made decisions based on intermediate results rather than simply generating recommendations.

### Tool orchestration

The reported operation connected AI agents to external penetration-testing tools through Model Context Protocol (MCP) integrations.

### Human direction and oversight

Human operators established objectives and directed the broader operation. Anthropic reported that AI handled a substantial proportion of tactical execution, while consequential decisions remained subject to human involvement.

These characteristics should be analysed alongside the conventional ATT&CK techniques, not treated as substitutes for them.

## 4. Defensive Considerations

| Observed behaviour | Defensive focus |
|---|---|
| External scanning and reconnaissance | Attack surface monitoring, exposure management and network detection |
| Vulnerability research and exploitation | Vulnerability management, patching and application security |
| Account discovery and credential use | Identity monitoring, MFA and privileged access management |
| Local account creation | Account-change monitoring and endpoint detection |
| Network and system discovery | Network telemetry, segmentation and behavioural detection |
| Credential harvesting | Secrets management and credential exposure monitoring |
| Data collection and staging | Database activity monitoring and data loss prevention |
| Exfiltration over web services | Egress monitoring, traffic analysis and data protection |
| Prompt manipulation and tool use | AI application security, tool authorisation and audit logging |

These are recommended defensive priorities. They are not proof that any individual control would necessarily have prevented the campaign.

## 5. Mapping Limitations

- The mapping follows MITRE ATT&CK's published C0062 campaign entry.
- MITRE campaign mappings are based on publicly available reporting and do not represent every possible technique used.
- The inclusion of a technique does not establish that it occurred in every compromised environment.
- A technique's presence in the campaign entry does not independently verify the underlying incident.
- Some descriptions reflect AI-enabled execution of conventional cyber techniques; they should not automatically be classified as AI-specific techniques.
- Technique names, IDs and campaign relationships can change as ATT&CK is updated.

## 6. Sources

1. MITRE ATT&CK. *Anthropic AI-orchestrated Campaign — C0062.* https://attack.mitre.org/campaigns/C0062/
2. MITRE ATT&CK. *Enterprise Matrix.* https://attack.mitre.org/matrices/enterprise/
3. Anthropic. (2025, November 13). *Disrupting the first reported AI-orchestrated cyber espionage campaign.* https://www.anthropic.com/news/disrupting-AI-espionage
4. Anthropic. *Mapping AI-enabled cyber threats.* https://www.anthropic.com/research/attack-navigator
