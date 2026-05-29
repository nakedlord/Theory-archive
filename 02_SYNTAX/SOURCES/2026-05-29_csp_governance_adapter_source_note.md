# CSP Governance Adapter Source Note

Status: source_note / operator_provenance / non-canon
Date: 2026-05-29
Source ID: `syntax-2026-05-29-csp-governance-adapter`
CSP event: `projects/csp-system/events/2026-05-29-codex-syntax-governance-adapter.md`

## Source

The user proposed connecting SynTax to CSP as a reasoning and decision layer for
consolidation, roadmaps, decision-making, and system development logic. The
metaphor was that SynTax should act like the spider while CSP and the other
projects are the web.

Codex and the user then selected a conservative v1:

- manual protocol adapter, not active runner;
- CSP-first pilot;
- dual home: operational adapter in `csp-system`, theory/operator expression in
  `Theory-archive/02_SYNTAX/`;
- no new repository;
- no event/session schema change;
- no automation in v1;
- producer sessions leave event/session traces and mark `needs_consolidation`.

## Interpretation

The durable theory-side idea is that SynTax can serve as a governance operator
for CSP by framing system work before projection:

- choose a reasoning mode;
- identify the active tension;
- bind the judgment to evidence;
- recommend an existing roadmap status;
- state a proof gate;
- define the next action;
- name the system impact.

This is not a claim that SynTax becomes the source of truth for CSP. CSP remains
the state/routing/projection layer. SynTax supplies the decision discipline used
by humans or agents during review.

## Target Artifact

Primary operator:

- `02_SYNTAX/OPERATORS/csp_governance_adapter.md`

Operational CSP adapter:

- `context-state-protocol/docs/syntax-governance-adapter.md`

## Status Boundaries

- Non-canon.
- CSP-first pilot.
- Operator candidate.
- No autonomous execution authority.
- No roadmap/projection mutation by producers.
- No Agent Playbook route in v1 unless the pattern later becomes a reusable
  cross-agent workflow outside CSP governance.

## Next Test

Use the adapter during the next real `csp-system` consolidation or proposal
review. The test passes if it helps classify a proposal or roadmap item into a
mode, active tension, proof gate, status recommendation, next action, and system
impact without creating a new source of truth or promoting candidates too early.
