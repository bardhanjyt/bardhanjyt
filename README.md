# Jyotirmoy Bardhan — Architecture Point of View

Principal AI Architect. A 2 minute 50 second film, and the LinkedIn post that goes with it.

The film is a first-person architecture argument for hiring managers. It is not a product demo and not a résumé recitation. The post carries the same argument in writing, with the decisions, planes, gates, and proof a VP or CTO can check.

**Title**

Models propose. Deterministic services commit.

**Video**

`Jyotirmoy-Bardhan-Architecture-POV.mp4`

1920×1080 · 24 fps · H.264 / AAC · 2:50 · burned-in captions · diagonal transparent watermark, *Jyotirmoy Bardhan*

Captions are in the picture. The film can be watched on mute.

---

## Who it is for

Hiring managers, VPs, and CTOs hiring a Principal AI Architect or equivalent architecture owner. The claim is not that a model is impressive. The claim is that the platform stays correct when the model is wrong, the region fails, or the cost curve moves.

## The invariant

Models propose. Deterministic services commit.

Identity, consent, clinical safety, money movement, and external side effects are not model outputs. They are state transitions owned by services that can commit, compensate, and be audited. Security, resilience, regulatory evidence, latency, and unit cost are non-functional requirements on that boundary, not a review after the demo.

## What the film and the post cover

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

## LinkedIn

**First line**

Models propose. Deterministic services commit.

**Post**

Hi, this is Jyotirmoy Bardhan, Principal AI Architect.

I architect enterprise AI platforms around one invariant: models propose, deterministic services commit. Identity, consent, clinical safety, money movement, and external side effects are not model outputs. They are state transitions owned by services that can commit, compensate, and be audited. Security, resilience, regulatory evidence, latency, and unit cost are non-functional requirements on that boundary, not a review after the demo.

When a requirement arrives, I do not start from a model or a platform choice. I fix the decision to be made, the failure domain that must be isolated, and the non-functional requirements that survive go-live: consistency class, latency, RTO and RPO, sovereignty, tenant isolation, and the evidence an auditor or a post-incident review will reconstruct. Those become plane boundaries. Control plane for policy, routing, and release. Data plane for state, features, and retrieval. Governance plane for audit, safety, and human authority. A diagram that does not change a boundary or a build-versus-buy call is not an architecture decision.

Trade-offs are taken under constraint, and they are written down. Latency against cost. Bounded autonomy against control. Managed inference against self-hosted serving. Delivery speed against the regulatory evidence required to ship. Each architecture decision record states the option taken, the options rejected, the requirement that decided it, the risk accepted, and the rollback. That is what holds checkpointed, dependency-aware recovery to a sub-five-minute RTO and near-zero RPO in capital markets; sub-second availability of 124+ biomarker signals; and hybrid semantic and lexical retrieval, with selective graph traversal, under 400 milliseconds, still grounded and cited.

I do not select for sophistication. I select for an architecture that remains correct when the model is wrong, the region fails, or the cost curve moves. Managed versus self-hosted is a TCO decision on latency, throughput, GPU utilization, operational complexity, and per-tenant cost attribution.

The model lifecycle is a production control loop, not a notebook. Governed acquisition, point-in-time features, golden sets, retrieval and generation metrics, adversarial and groundedness tests, canary and shadow release, drift detection, remediation, and retirement. Models, prompts, agents, retrieval pipelines, tool contracts, and policies are versioned artifacts behind promotion gates. Experimental results do not re-enter training without protocol, quality control, and adjudication. If a change cannot be evaluated, observed, costed per tenant, and rolled back, it does not ship. Generation is limited to synthesis and critique. Tool calls are typed, idempotent, and mediated. No generic HTTP tool. No model output becomes a recipient, a parameter, or execution authority. Human interrupt, saga compensation, and fail-closed escalation are in the contract.

Architectural authority is ownership of those decisions, and of the consequence when they are breached. I set reference architectures, resilience standards, decision records, and production-readiness gates, and I keep the escalation path open when delivery pressure tries to collapse the boundary. On one programme that was sixteen platform decision records and an explicit build-versus-buy record, taken with VP and CTO stakeholders.

Leadership is making the invariant hold without me in the room. I have directed programmes of up to 48 engineers across architecture, AI, data, platform, SRE, security, and QA, and aligned product and executive stakeholders on one operating model. Reusable orchestration, policy enforcement, and release gates cut secure AI-solution onboarding time by more than 60 percent.

Across healthcare, life sciences, capital markets, and supply chain, the pattern is the same. Separate probabilistic reasoning from workflow authority. Isolate failure domains. Pin the artifact. Recover state and side effects, not just the endpoint. Take the platform from a blank canvas to a system that can be operated, recovered, and explained.

I am Jyotirmoy Bardhan, Principal AI Architect. I do not design systems so a model can look capable. I put in place the boundaries, gates, and decision rights that keep complex AI systems reliable, affordable, and accountable under real load.

**Hashtags**

`#AIArchitecture` `#EnterpriseAI` `#AIGovernance` `#LLMOps` `#AgenticAI`

Five only. Do not add `#AI`, `#MachineLearning`, `#Innovation`, or `#OpenToWork`.

## How to post

1. Upload the watermarked MP4 as a native LinkedIn video. Do not link out.
2. First line of the post is the title above. The introduction follows it.
3. Hashtags go on their own line at the end.
4. Watch it once with sound before publishing. The voiceover is synthesized. It is not a personal recording. Captions carry the argument if a viewer never unmutes.

## What this document is not

It is not a résumé, a case study, or a design document for a single programme. Engagement narratives, team sizes on individual programmes, and regulated-domain detail stay on the résumé. The numbers in this README are only the ones the film and the post are willing to say in public.
