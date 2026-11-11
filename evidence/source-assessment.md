# Source Assessment

## 1. Purpose

This document evaluates the sources used in the GTG-1002 threat intelligence investigation.

Source reliability and confidence in individual findings are assessed separately. A credible source may report information that cannot be independently verified.

## 2. Source Evaluation Criteria

Each source is assessed against the following criteria:

- **Authority:** Is the source recognised and qualified in the relevant field?
- **Proximity:** Does the source have direct access to the reported activity?
- **Transparency:** Does it explain its methodology and supporting evidence?
- **Corroboration:** Are its claims supported by independent sources?
- **Potential bias:** Does the source have commercial, institutional or other interests that may influence its reporting?
- **Currency:** Is the information sufficiently recent for the investigation?

## 3. Source Assessments

### S-001 — Anthropic Campaign Disclosure

**Source:** https://www.anthropic.com/news/disrupting-AI-espionage

**Source type:** Primary vendor disclosure.

**Relevance:** Directly concerns the GTG-1002 campaign and provides the principal narrative for this investigation.

**Strengths:**
- Published by the organisation that identified and disrupted the reported activity.
- Provides operational details and an explanation of the AI systems involved.
- Offers direct insight into the provider's assessment of the campaign.

**Limitations:**
- The public disclosure does not provide the investigator with access to all underlying telemetry.
- Anthropic has a commercial and institutional interest in AI safety and security.
- Some claims may not be independently corroborated in public sources.

**Assessment:** High relevance and direct proximity to the reported incident. Individual claims require separate confidence assessments.

### S-002 — Anthropic Technical Report

**Source:** https://www-cdn.anthropic.com/d7dd50dd1185f59be051b307150d877f2b82bd2c.pdf

**Source type:** Technical report accompanying the public disclosure.

**Relevance:** Provides additional technical and operational detail for reconstructing the reported campaign.

**Strengths:**
- Provides a more detailed account of the reported activity and technical workflow.
- Supports investigation of agent orchestration, operational tasks and reported limitations.
- Provides material for evidence-level analysis.

**Limitations:**
- Produced by the same organisation as S-001 and therefore is not independent corroboration.
- Publicly available detail may not represent the complete incident record.

**Assessment:** High relevance. Treat as a technical companion to S-001 rather than a separate independent confirmation.

### S-003 — MITRE ATT&CK Campaign C0062

**Source:** https://attack.mitre.org/campaigns/C0062/

**Source type:** Structured adversary campaign knowledge base.

**Relevance:** Provides a recognised framework for examining reported campaign behaviours and associated techniques.

**Strengths:**
- Uses a consistent and widely recognised taxonomy.
- Provides traceable technique references.
- Helps translate narrative reporting into structured defensive analysis.

**Limitations:**
- Campaign mappings may rely on the same underlying public reporting.
- A technique mapping is not independent proof that the activity occurred.
- Framework entries may change as new information becomes available.

**Assessment:** High value as a structured analytical reference, but not independent corroboration of the original incident.

### S-004 — MITRE ATLAS

**Source:** https://atlas.mitre.org/

**Source type:** AI threat knowledge base.

**Relevance:** Provides a framework for analysing adversarial behaviour involving AI systems and agentic capabilities.

**Strengths:**
- Provides AI-specific threat terminology and technique descriptions.
- Supports analysis of agent tool use, prompt injection and autonomous behaviour.
- Helps identify relevant defensive controls and research questions.

**Limitations:**
- A framework technique is not evidence that a particular campaign used it.
- Some techniques are based on research demonstrations rather than confirmed real-world incidents.

**Assessment:** High value for contextual analysis. Apply only where specific campaign evidence supports a mapping.

## 4. Independence and Corroboration

A key limitation of this investigation is the dependency between sources.

MITRE ATT&CK C0062 provides a structured representation of campaign information, but it should not automatically be treated as independent confirmation of Anthropic's original reporting.

Similarly, the accompanying technical report and public announcement originate from the same organisation.

Further research should seek independent reporting, technical analysis or additional primary evidence before increasing confidence in important claims.

## 5. Overall Assessment

The available sources are highly relevant to the investigation, particularly because Anthropic was directly involved in detecting and disrupting the reported activity.

However, the evidence base is concentrated around one primary reporting organisation. This limits independent corroboration.

The investigation therefore treats Anthropic's reporting as the principal account of the campaign, uses MITRE frameworks to structure the analysis, and explicitly records uncertainty where independent verification is unavailable.
