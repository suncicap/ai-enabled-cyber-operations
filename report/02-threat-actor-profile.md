# Threat Actor Profile

## 1. Overview

GTG-1002 is the designation used by Anthropic to identify the threat actor responsible for the AI-orchestrated cyber espionage campaign disclosed in November 2025.

Anthropic assessed with high confidence that the activity was conducted by a Chinese state-sponsored group.

The public reporting provides information about the group's operational approach and capabilities, but does not establish the identities of individual operators or provide independently verified organisational attribution.

## 2. Attribution Assessment

**Reported designation:** GTG-1002  
**Attribution assessment:** Likely Chinese state-sponsored actor  
**Primary attribution source:** Anthropic  
**Confidence stated by source:** High confidence

The attribution is based on Anthropic's investigation of the campaign.

This report retains the GTG-1002 designation and attributes the state sponsorship assessment to Anthropic. It does not attempt to associate the activity with a named advanced persistent threat (APT) group without further supporting evidence.

## 3. Likely Objectives

The campaign's reported targeting and activities are consistent with cyber espionage objectives.

The targeted sectors included:

- Technology companies.
- Financial institutions.
- Chemical manufacturing organisations.
- Government agencies.

The reported collection of credentials, access to internal systems and extraction of data suggest an emphasis on obtaining sensitive organisational and potentially strategic information.

The precise intelligence requirements and intended use of the collected information have not been independently established.

## 4. Reported Capabilities

Anthropic's reporting describes several capabilities demonstrated during the campaign.

### Reconnaissance

AI agents were reportedly used to inspect target infrastructure, identify services and locate potentially valuable systems and databases.

### Vulnerability discovery and exploitation

The agents reportedly researched vulnerabilities, developed exploit code and attempted to gain access to target systems.

### Credential access

The operation included credential harvesting and identification of accounts with elevated privileges.

### Lateral movement and post-exploitation

The reported activity included movement through compromised environments, further access to internal systems and data collection.

### Data analysis and exfiltration

AI was reportedly used to organise collected information, assess its intelligence value and prepare documentation for subsequent operational activity.

These capabilities are based on Anthropic's account of the campaign and have not been independently reproduced in this investigation.

## 5. Operational Characteristics

The campaign demonstrated several notable characteristics:

- **AI-enabled task delegation:** Complex objectives were divided into smaller tasks assigned to specialised agents.
- **Tool integration:** Claude Code agents interacted with external tools through Model Context Protocol (MCP) integrations.
- **Human strategic direction:** Human operators selected targets, established the operational framework and intervened at important decision points.
- **High levels of automation:** Anthropic estimated that AI performed approximately 80–90% of the tactical work.
- **Verification limitations:** AI-generated outputs sometimes contained inaccurate or fabricated information, requiring human review.

The combination of automation and human oversight is important. The operation was not entirely autonomous; human operators remained responsible for strategic direction and critical decisions.

## 6. Assessment of Threat Significance

GTG-1002 illustrates how AI agents can potentially increase the speed, scale and operational capacity of a threat actor.

The most significant characteristic is not simply the use of an AI model to generate code or provide technical advice. It is the reported integration of AI reasoning, task delegation and external tool execution across multiple stages of an intrusion.

This creates additional defensive challenges around:

- Monitoring activity generated through legitimate tools.
- Identifying coordinated actions across multiple systems.
- Controlling access granted to AI agents.
- Detecting unusual patterns of automated behaviour.
- Maintaining visibility over human and machine decision-making.

## 7. Intelligence Gaps

The following questions remain open:

1. What is the independently verifiable identity and organisational structure of GTG-1002?
2. What was the precise intelligence objective for each target?
3. How much of the reported activity was performed by AI agents versus directly by human operators?
4. Which technical capabilities were developed specifically for this campaign?
5. Are there independently documented campaigns using comparable AI-agent orchestration methods?

These gaps limit the conclusions that can be drawn about the actor's wider capabilities and long-term intentions.

## 8. Sources

1. Anthropic, [Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage).
2. Anthropic, [Full campaign report](https://www-cdn.anthropic.com/d7dd50dd1185f59be051b307150d877f2b82bd2c.pdf).
3. MITRE ATT&CK, [Campaign C0062](https://attack.mitre.org/campaigns/C0062/).
