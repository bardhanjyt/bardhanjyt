# Jyotirmoy Bardhan | Principal AI Architect — Architecture Point of View

**Title**

Models propose. Deterministic services commit.

---

## The invariant

Models propose. Deterministic services commit.

Identity, consent, clinical safety, money movement, and external side effects are not model outputs. They are state transitions owned by services that can commit, compensate, and be audited. Security, resilience, regulatory evidence, latency, and unit cost are non-functional requirements on that boundary, not a review after the demo.

## What the video and the post cover

**How a requirement is taken apart.** The work does not start from a model or a platform choice. It starts from the decision to be made, the failure domain that must be isolated, and the non-functional requirements that survive go-live: consistency class, latency, RTO and RPO, sovereignty, tenant isolation, and the evidence an auditor or a post-incident review will reconstruct.

**How that becomes architecture.** Those requirements become plane boundaries.

- Control plane: policy, routing, and release.
- Data plane: state, features, and retrieval.
- Governance plane: audit, safety, and human authority.

A diagram that does not change a boundary or a build-versus-buy call is not an architecture decision.

**How trade-offs are made.** Every option has a cost. Latency against cost. Bounded autonomy against control. Managed inference against self-hosted serving. Delivery speed against the regulatory evidence required to ship. Each architecture decision record states the option taken, the options rejected, the requirement that decided it, the risk accepted, and the rollback.

**What is selected.** Not the most sophisticated architecture. The one that remains secure, operable, and economically sustainable when the model is wrong. Managed versus self-hosted is a TCO decision on latency, throughput, GPU utilization, operational complexity, and per-tenant cost attribution.

**How the model lifecycle is closed.** The lifecycle is a production control loop, not a notebook. Governed acquisition, point-in-time features, golden sets, retrieval and generation metrics, adversarial and groundedness tests, canary and shadow release, drift detection, remediation, and retirement. Models, prompts, agents, retrieval pipelines, tool contracts, and policies are versioned artifacts behind promotion gates. Experimental results do not re-enter training without protocol, quality control, and adjudication. If a change cannot be evaluated, observed, costed per tenant, and rolled back, it does not ship.

Generation is limited to synthesis and critique. Tool calls are typed, idempotent, and mediated. No generic HTTP tool. No model output becomes a recipient, a parameter, or execution authority. Human interrupt, saga compensation, and fail-closed escalation are in the contract.

**Where authority sits.** Architectural authority is ownership of those decisions, and of the consequence when they are breached. Reference architectures, resilience standards, decision records, and production-readiness gates. The escalation path stays open when delivery pressure tries to collapse the boundary. On one programme that was sixteen platform decision records and an explicit build-versus-buy record, taken with VP and CTO stakeholders.

**How leadership is exercised.** The invariant has to hold without the architect in the room. Programmes of up to 48 engineers across architecture, AI, data, platform, SRE, security, and QA. Product and executive stakeholders on one operating model. Reusable orchestration, policy enforcement, and release gates cut secure AI-solution onboarding time by more than 60 percent.

## Proof the post is willing to stand on

| Domain | What the architecture holds |
| --- | --- |
| Capital markets | Checkpointed, dependency-aware recovery. Sub-five-minute RTO. Near-zero RPO. Failure domains isolated. |
| Healthcare | 124+ biomarker signals available in under a second. |
| Supply chain | Hybrid semantic and lexical retrieval, with selective graph traversal, under 400 milliseconds, grounded and cited. |
| Enterprise operating model | Secure AI-solution onboarding time reduced by more than 60 percent. |

Domains in the close: healthcare, life sciences, capital markets, and supply chain. The pattern is the same in each. Separate probabilistic reasoning from workflow authority. Isolate failure domains. Pin the artifact. Recover state and side effects, not just the endpoint.


