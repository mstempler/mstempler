# Applied LLM Engineering & Safety

**Technical focus:** Bounded LLM recommendations with deterministic policy enforcement.

## Business challenge
Produce bounded recommendations for synthetic financial cases without executing actions.

## Architecture and approach
Python, OpenAI Responses API, Pydantic contracts and deterministic policy validation.

[Conceptual architecture](../architecture/applied-llm.md)

## Engineering decision and trade-off
Separate probabilistic generation from deterministic acceptance. Invalid outputs receive a bounded retry; unresolved cases return structured errors. Human review is a recommendation, not an implemented approval workflow.

## Engineering evidence
Five recorded cases passed validation; mean latency 1,728.4 ms; estimated mean cost USD 0.0002848. Two recorded restricted cases required human supervision.

[Evidence record](../evidence/applied-llm.md)

## Contribution and provenance
Commits attributed to the portfolio owner; manual authorship not established.

## Limitations and next validation
Small synthetic sample; confidence is not calibrated; no formal verification or production impact claim.

## Business value hypothesis
Reduce unsafe recommendations and manual triage effort; measure policy violations, escalation recall and cost per valid recommendation. These are proposed success measures, not achieved outcomes.

## Next evidence milestone
Run a versioned synthetic adversarial suite with expected outcomes; report failure rates and latency percentiles.
