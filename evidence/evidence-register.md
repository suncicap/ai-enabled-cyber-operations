# Evidence Register

## Purpose

This register records the evidence collected during the investigation into the GTG-1002 AI-orchestrated cyber espionage campaign.

Each item should identify its source, describe what it supports, and record any limitations. Evidence and analytical interpretation must remain separate.

## Evidence Log

| ID | Source | Date | Evidence / Finding | Source Reliability | Confidence | Limitations |
|---|---|---|---|---|---|---|
| E-001 | Anthropic — Disrupting the first reported AI-orchestrated cyber espionage campaign | 13 November 2025 | Primary disclosure describing the GTG-1002 campaign and Anthropic's assessment of AI involvement in cyber operations. | Primary source — high relevance; vendor-reported findings | To be assessed by claim | Findings are reported by the organisation that detected and disrupted the activity; independent corroboration may be limited. |
| E-002 | MITRE ATT&CK — Campaign C0062 | Created 20 April 2026; last modified 31 July 2026; accessed 11 November 2026 | Current structured campaign reference. The campaign mapping and associated technique procedure pages currently associate 27 Enterprise technique and sub-technique IDs with C0062, including T1699 Direct Prompt Injection. The T1699 technique page explicitly lists a C0062 procedure example. | Established framework reference | High confidence in the contents of the current page; not independent confirmation of the incident | Check the underlying references and distinguish framework-recorded behaviours from independent verification. The campaign and technique pages may change. |
| E-003 | Anthropic technical report, p. 5 | November 2025 | The reported attack framework used Claude Code, MCP tools and multiple specialised AI agents to coordinate reconnaissance, credential validation, data extraction and lateral movement. | Primary source — high relevance; vendor-reported findings | Medium — reported architectural details | The underlying framework and infrastructure have not been independently examined in this project. |
| E-004 | Anthropic technical report, pp. 6–7 | November 2025 | Anthropic reports that AI performed approximately 80–90% of tactical operations, while human operators retained strategic supervision and authorisation responsibilities. | Primary source — high relevance; vendor-reported findings | Medium — based on Anthropic's operational analysis | The methodology behind the percentage estimate is not fully detailed in the public report. |
| E-005 | Anthropic technical report, pp. 3, 7–11 | November 2025 | The report describes AI-supported reconnaissance, vulnerability discovery, exploitation, credential harvesting, lateral movement, data collection and documentation. | Primary source — high relevance; vendor-reported findings | Medium — campaign-level reporting | Specific technical details and successful outcomes vary by target; do not assume every phase occurred in every intrusion. |
| E-006 | MITRE ATT&CK — Direct Prompt Injection, T1699 | Created 18 September 2026; accessed 11 November 2026 | MITRE's T1699 procedure examples explicitly include C0062 and describe a crafted prompt claiming a defensive cybersecurity testing context to authorise restricted operations. | Established framework reference | High confidence in the contents of the current technique page; not independent confirmation of the incident | The technique page classifies the reported procedure; it relies on the cited campaign reporting and is not independent corroboration. |

## Evidence Assessment Principles

- **Source reliability:** Consider the source's authority, proximity to the events, expertise, transparency and potential bias.
- **Confidence:** Assess how strongly the available evidence supports a particular finding.
- **Corroboration:** Look for independent sources that support or challenge important claims.
- **Limitations:** Record gaps, uncertainty, missing context and potential conflicts of interest.
- **Traceability:** Every significant analytical conclusion should link back to one or more evidence IDs.

## Confidence Scale

| Level | Meaning |
|---|---|
| High | Strong evidence for the specific proposition being assessed. For claims about a published source or framework entry, direct inspection may be sufficient. For underlying incident claims, independent corroboration is normally expected. |
| Medium | Credible supporting evidence, but with gaps or limited independent corroboration. |
| Low | Limited, indirect or uncertain supporting evidence. |
| Unassessed | Not yet evaluated. |

## Notes

This register is a working document. Entries will be updated as sources are reviewed and evidence is corroborated.

A source being credible does not automatically make every claim within it independently verified. MITRE ATT&CK C0062 is a structured framework entry based on cited reporting; it should not be counted as independent corroboration of Anthropic's account.
