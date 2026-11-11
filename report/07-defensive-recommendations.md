# Defensive Recommendations

## 1. Purpose

This section translates the findings from the GTG-1002 case study into practical defensive recommendations.

The focus is on reducing the risks associated with AI-enabled cyber operations, particularly where AI agents can interact with external tools, access organisational systems and perform multi-stage tasks.

These recommendations are analytical conclusions drawn from the reported campaign. They should not be interpreted as controls confirmed to have prevented the incident.

## 2. Identity and Access Management

**Risk:** AI agents with access to credentials or privileged accounts may be able to perform actions beyond their intended scope.

**Recommendations:**
- Apply least-privilege access to human and machine identities.
- Use short-lived credentials and secure secrets management.
- Require strong authentication for sensitive operations.
- Review and revoke unnecessary permissions regularly.
- Monitor unusual authentication and privilege-escalation activity.

**Defensive priority:** Limit the potential impact of compromised credentials and prevent an AI agent from inheriting excessive access.

## 3. AI Agent Permissions and Tool Access

**Risk:** An AI agent connected to external tools may execute actions that have consequences beyond generating text or recommendations.

**Recommendations:**
- Maintain an inventory of deployed AI agents and their integrations.
- Restrict access to approved tools and services.
- Separate read-only access from permissions that allow modification or execution.
- Require human approval for high-impact actions.
- Validate tool inputs and outputs.
- Establish controls for agent-to-agent communication and delegation.

**Defensive priority:** Treat AI agents as active components of the technology environment, with explicit permissions and accountability.

## 4. Monitoring and Detection

**Risk:** Individual actions performed through legitimate tools may appear normal, while a sequence of coordinated actions may indicate malicious activity.

**Recommendations:**
- Log agent identities, tool calls, timestamps and requested actions.
- Correlate identity, endpoint, network and cloud telemetry.
- Monitor unusual reconnaissance, authentication and access patterns.
- Detect unexpected privilege changes and lateral movement.
- Establish alerts for unusual data access and outbound transfers.
- Preserve logs for investigation and incident response.

**Defensive priority:** Build visibility across the complete activity chain rather than monitoring isolated events.

## 5. Network Segmentation and Endpoint Security

**Risk:** Successful access to one system may enable further movement through an inadequately segmented environment.

**Recommendations:**
- Segment sensitive systems and critical infrastructure.
- Restrict unnecessary communication between network zones.
- Maintain endpoint detection and response coverage.
- Monitor administrative tools and remote access activity.
- Apply timely security updates and vulnerability remediation.
- Review exposed services and externally accessible systems.

**Defensive priority:** Reduce the ability of an attacker to expand access after an initial compromise.

## 6. Data Protection

**Risk:** AI-supported collection and analysis may accelerate the identification and aggregation of sensitive information.

**Recommendations:**
- Classify sensitive organisational information.
- Apply access controls based on business need.
- Monitor bulk data access and unusual collection patterns.
- Restrict unauthorised data transfers.
- Maintain data loss prevention controls where appropriate.
- Establish clear retention and deletion policies for AI-connected systems.

**Defensive priority:** Detect and restrict unauthorised access to, aggregation of and movement of sensitive data.

## 7. AI Security Governance

**Risk:** AI agents may be deployed without sufficient oversight of their permissions, behaviour, integrations or operational impact.

**Recommendations:**
- Establish an approval process for AI agent deployment.
- Conduct security assessments before connecting agents to organisational systems.
- Define acceptable use and prohibited actions.
- Test for prompt injection and unsafe tool invocation.
- Maintain an inventory of models, agents, tools and data connections.
- Assign clear ownership for monitoring and incident response.

**Defensive priority:** Integrate AI agent security into existing security governance and risk management processes.

## 8. Incident Response Preparedness

**Risk:** Conventional incident response procedures may not adequately account for automated activity initiated by AI agents or orchestrated across multiple integrations.

**Recommendations:**
- Include AI-enabled scenarios in incident response exercises.
- Define procedures for suspending or isolating compromised agents.
- Preserve agent logs, prompts, tool calls and relevant execution records.
- Review credentials and permissions associated with affected agents.
- Identify connected systems and assess potential downstream impact.
- Coordinate response between security, IT, legal and AI governance teams.

**Defensive priority:** Ensure organisations can rapidly contain AI-enabled activity while preserving the evidence needed for investigation.

## 9. Strategic Assessment

The GTG-1002 case reinforces the importance of combining established cybersecurity controls with security measures designed for AI-connected environments.

The most important defensive priorities are:

1. Strong identity and access controls.
2. Restricted agent permissions and tool access.
3. Comprehensive monitoring and auditability.
4. Effective network segmentation.
5. Protection of sensitive data.
6. AI-specific security governance.
7. Incident response procedures that account for agent behaviour.

No single control is sufficient. Effective defence requires coordinated measures across identity, infrastructure, data protection, monitoring and governance.

## 10. Sources and Frameworks

- MITRE ATT&CK: https://attack.mitre.org/
- MITRE ATLAS: https://atlas.mitre.org/
- NIST Cybersecurity Framework: https://www.nist.gov/cyberframework
- NIST AI Risk Management Framework: https://www.nist.gov/itl/ai-risk-management-framework
- Anthropic, Disrupting the first reported AI-orchestrated cyber espionage campaign: https://www.anthropic.com/news/disrupting-AI-espionage
