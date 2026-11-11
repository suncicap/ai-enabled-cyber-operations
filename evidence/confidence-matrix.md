# Intelligence Confidence Matrix

## 1. Purpose

This matrix evaluates confidence in the principal findings of the GTG-1002 investigation.

It distinguishes confidence that a source made a particular statement from confidence that the underlying event has been independently established. A directly accessible primary source can support high confidence that the statement was made, without independently proving every reported event.

## 2. Confidence Scale

| Rating | Definition |
|---|---|
| High | Strong evidence for the specific proposition being assessed. For claims about what a source published, this may be the directly accessible source itself. For claims about underlying events, high confidence normally requires corroboration or unusually strong primary evidence. |
| Medium | Credible and relevant evidence supports the proposition, but important limitations, incomplete transparency or limited independent corroboration remain. |
| Low | Indirect, incomplete or substantially uncertain evidence. |
| Unassessed | Insufficient analysis to assign a confidence rating. |

## 3. Finding Assessment

| Finding | Supporting Evidence | Confidence | Rationale |
|---|---|---|---|
| Anthropic publicly reported a cyber espionage campaign designated GTG-1002. | E-001 | High — confidence in the publication | The disclosure is directly accessible. This rating confirms what Anthropic reported, not the independent truth of every underlying claim. |
| The reported campaign involved multiple specialised AI agents and tool integrations. | E-003 | Medium | Detailed vendor reporting, but no independent access to the underlying framework or telemetry. |
| AI performed approximately 80–90% of tactical operations. | E-004 | Medium — confidence in the reported estimate | Anthropic provided this estimate, but the public methodology behind the percentage is limited. |
| AI supported reconnaissance, vulnerability research, exploitation and data collection. | E-005 | Medium | Multiple operational activities are described in the primary reporting, but independent corroboration remains limited. |
| Human operators retained strategic oversight. | E-004 | Medium | Reported by Anthropic; the precise boundaries of human intervention are not independently established. |
| AI-generated outputs included inaccurate or fabricated information. | E-001, E-005 | Medium | Reported examples illustrate reliability problems, but the full frequency and impact are unknown. |
| MITRE ATT&CK associates 27 technique and sub-technique IDs with campaign C0062, including T1699 Direct Prompt Injection. | E-002, E-006 | High — confidence in the current framework entries | Checked against the current MITRE campaign and T1699 technique pages on 11 November 2026. This confirms the contents of the framework entries, not independent verification of the underlying campaign activity. |

## 4. Intelligence Gaps

The following questions remain open:

1. Can the reported technical activity be independently corroborated?
2. What evidence supports the reported level of AI autonomy?
3. How consistently were human approval controls applied?
4. Which reported techniques were successfully executed against individual targets?
5. What additional telemetry or technical artefacts would allow independent validation?

## 5. Analytical Judgement

The available reporting provides a credible basis for examining the use of AI agents in cyber operations.

The strongest conclusions concern what Anthropic publicly reported and what the current MITRE campaign entry records. Greater caution is necessary when assessing the precise degree of autonomy, the effectiveness of individual techniques and the wider implications for threat actors.

The investigation therefore maintains medium confidence in most campaign-specific technical findings pending independent corroboration.

## 6. Review and Update

This matrix should be updated when:

- New independent reporting becomes available.
- Additional technical evidence is identified.
- Existing claims are contradicted or revised.
- The underlying MITRE ATT&CK campaign information changes.
