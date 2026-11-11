# AI Security Analysis

## 1. Purpose

This document examines the role of artificial intelligence in the GTG-1002 campaign, focusing on agent autonomy, tool orchestration, human oversight and the security implications of AI-enabled cyber operations.

The analysis distinguishes between conventional cyber techniques and the additional capabilities introduced by AI systems.

**Primary source:** Anthropic, November 2025 campaign disclosure and technical report.

## 2. AI Agent Architecture

Anthropic describes an operation involving multiple specialised AI agents coordinated through an orchestration framework.

The reported architecture included:

- An AI model used for reasoning, planning and task execution.
- Multiple specialised agents assigned different operational responsibilities.
- External tools connected through Model Context Protocol (MCP) integrations.
- Shared operational context and coordination between tasks.
- Human operators establishing objectives and retaining strategic oversight.

### Why this matters

Traditional automation usually follows predefined scripts and workflows. AI agents can interpret instructions, adapt their approach and select actions based on intermediate results.

When agents are connected to tools and granted access to systems, their capabilities extend beyond generating text or code. They can interact with real environments and execute multi-step tasks.

This creates a larger attack surface involving the model, agent configuration, tool integrations, credentials, permissions and connected infrastructure.

## 3. AI-Enabled Capabilities

### 3.1 Autonomous Task Execution

The reported agents performed technical tasks such as reconnaissance, vulnerability research, credential validation and data collection.

**Security implication:** Automated execution can increase the speed and scale of malicious activity, potentially reducing the time available for defenders to identify and respond to an intrusion.

### 3.2 Multi-Agent Orchestration

Specialised agents reportedly handled different tasks within a coordinated operation.

**Security implication:** Dividing an operation into smaller tasks can make the overall activity more difficult to understand from isolated events or individual system logs.

### 3.3 Tool Integration Through MCP

The framework reportedly used MCP-connected tools to interact with external resources and target environments.

**Security implication:** Tool permissions become a critical security boundary. An agent should not automatically inherit unrestricted access simply because a model can request an action.

### 3.4 AI-Assisted Technical Research

AI was reportedly used to research vulnerabilities, generate code and assist with exploitation.

**Security implication:** AI can lower the expertise and time required for some technical activities. However, generated code and technical conclusions still require verification.

### 3.5 Automated Data Processing

AI agents reportedly helped identify, collect, categorise and document information. Anthropic's subsequent analysis also describes the staging and compression of collected material before final extraction.

**Security implication:** Automated processing can increase the volume of data an attacker can handle. Monitoring should consider unusual access patterns, staging activity and outbound data movement, not only manual user activity.

## 4. Human Oversight and Control

The campaign demonstrates that AI autonomy and human control are not mutually exclusive.

According to Anthropic, human operators established the strategic objectives and retained oversight while AI agents performed a substantial proportion of tactical tasks. Anthropic's subsequent analysis states that the final data extraction was human-directed.

This raises several questions:

- Which actions require explicit human approval?
- Can an agent initiate additional actions without further authorisation?
- Are tool permissions limited to the minimum necessary?
- Can an organisation reconstruct an agent's decisions and actions?
- Can an agent be stopped quickly without losing essential evidence?

Human oversight is only meaningful when operators have sufficient visibility, time and authority to intervene.

## 5. AI Reliability and Failure Modes

Anthropic also reported instances where the AI generated inaccurate information, including fabricated credentials and claims that information had been obtained when this was not the case.

This illustrates several risks:

- Hallucinated technical findings.
- Incorrect assumptions about target environments.
- False claims of successful exploitation.
- Inaccurate reporting of collected information.
- Cascading errors when one agent relies on another agent's output.

A multi-agent architecture can amplify both useful findings and incorrect information.

Independent validation is therefore essential before acting on AI-generated intelligence.

## 6. Defensive Priorities

| Risk Area | Recommended Control |
|---|---|
| Excessive agent permissions | Least privilege and role-based access control |
| Unrestricted tool execution | Tool allowlists and action-level authorisation |
| Compromised or manipulated instructions | Prompt-injection testing and input isolation |
| Sensitive credential exposure | Secrets management and short-lived credentials |
| Untraceable agent activity | Centralised logging and audit trails |
| Autonomous high-impact actions | Human approval gates and execution limits |
| Inaccurate AI-generated findings | Independent validation and evidence requirements |
| Multi-agent coordination | Monitoring of agent-to-agent communication and shared state |

## 7. MITRE ATLAS Relevance

MITRE ATLAS is a knowledge base for adversarial tactics and techniques involving AI-enabled systems. It provides useful terminology for examining the security implications of the agent architecture described in the GTG-1002 reporting.

The following techniques are discussed as **contextual analytical references**, not as a formal MITRE ATLAS mapping of campaign C0062:

| ATLAS Technique ID | Technique | Analytical relevance and limitation |
|---|---|---|
| AML.T0053 | AI Agent Tool Invocation | Closely relevant to the reported use of MCP-connected tools by agents. This is a conceptual comparison to the reported tool use, not a claim that ATLAS has formally mapped the campaign to this technique. |
| AML.T0051 | LLM Prompt Injection | Relevant to the broader risk of malicious instructions influencing model behaviour. Anthropic reports crafted prompts and personas used to bypass guardrails; this project does not claim a formal ATLAS campaign mapping. |
| AML.T0065 | LLM Prompt Crafting | Relevant as a framework concept for crafted prompts. It should not be read as independent evidence of a distinct campaign technique. |
| AML.T0103 | Deploy AI Agent | A useful comparison for considering agents launched in a victim environment. The available campaign reporting describes agents operating through an attacker-controlled framework, so this technique is not asserted as a direct match. |

### Framework distinction

MITRE ATT&CK campaign C0062 currently lists 26 technique and sub-technique IDs. It does **not** list T1699 — Direct Prompt Injection. Do not conflate ATT&CK and ATLAS identifiers or infer that a technique is part of C0062 simply because it is relevant to AI security.

Autonomous Attack Orchestration is also a useful broader ATLAS concept for discussing agentic operations, but it is not presented here as a confirmed campaign-specific mapping.

**Official framework:** https://atlas.mitre.org/  
**ATT&CK campaign:** https://attack.mitre.org/campaigns/C0062/

## 8. Intelligence Assessment

The GTG-1002 reporting illustrates how AI agents can be incorporated into complex cyber operations as active operational components rather than simply as advisory tools.

The principal security concern is not AI alone, but the combination of reasoning capabilities, autonomous task execution, external tool access, credentials and insufficiently constrained permissions.

For defenders, this means extending security monitoring and governance beyond the model itself to include the complete agent ecosystem.

The findings are based primarily on Anthropic's reporting. Independent verification of the underlying infrastructure and operational telemetry remains outside the scope of this project.

## 9. Sources

1. Anthropic, https://www.anthropic.com/news/disrupting-AI-espionage
2. Anthropic, *Mapping AI-enabled cyber threats*, https://www.anthropic.com/research/attack-navigator
3. MITRE ATLAS, https://atlas.mitre.org/
4. MITRE ATT&CK, https://attack.mitre.org/campaigns/C0062/
5. MITRE ATLAS, *AI Agent Tool Invocation (AML.T0053)* and *Deploy AI Agent (AML.T0103)*, https://atlas.mitre.org/
