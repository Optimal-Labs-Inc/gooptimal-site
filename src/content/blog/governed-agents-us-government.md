---
title: "Delivering AI Agents in the US Government"
description: "How government leaders can overcome the impediments to governed autonomy. Agencies are putting agents into production faster than they are defining the controls around them."
date: 2026-11-10
category: "Trend Report"
image: "/blog/governed-agents-us-government.png"
imageAlt: "45% of federal IT leaders report agentic AI in a production workflow, while 8% report a defined incident response framework for it"
tags:
  - "agentic AI"
  - "AI security"
  - "federal AI"
  - "AI governance"
  - "zero trust"
  - "public sector"
---

<style>
  .tr-toc { border: 1px solid var(--rule); border-radius: var(--radius-sm); background: var(--surface); padding: 16px 20px; font-size: 14px; }
  .tr-toc-k, .tr-fig-k { font-family: var(--font-mono); font-size: 10.5px; letter-spacing: 0.2em; text-transform: uppercase; color: var(--sunset); }
  .tr-toc ol { margin: 10px 0 0; padding-left: 1.3em; gap: 0.3em; }
  .tr-toc a { border-bottom: 0; color: var(--text); }
  .tr-toc a:hover { color: var(--sunset); }
  .tr-fig { border: 1px solid var(--rule); border-radius: var(--radius-sm); background: var(--surface); padding: 18px 20px 14px; margin: 1.6em 0 0.4em; }
  .tr-fig-t { font-family: var(--font-display); font-weight: 600; font-size: 1.15rem; line-height: 1.3; color: var(--text); margin: 6px 0 16px; }
  .tr-row { display: grid; grid-template-columns: minmax(0, 1fr); gap: 5px; margin-top: 13px; }
  .tr-lab { font-size: 13px; line-height: 1.4; color: var(--text-dim); }
  .tr-lab small { color: var(--text-faint); font-size: 11px; }
  .tr-track { display: flex; align-items: center; gap: 10px; }
  .tr-bar { height: 18px; border-radius: 4px; background: var(--grad-sunset); min-width: 4px; }
  .tr-bar.q { background: #5f6a80; }
  .tr-val { font-family: var(--font-mono); font-size: 13px; font-weight: 600; color: var(--text); }
  .tr-src { border-top: 1px solid var(--rule); margin-top: 16px; padding-top: 8px; font-size: 10.5px; line-height: 1.5; color: var(--text-faint); }
  @media (min-width: 640px) {
    .tr-row { grid-template-columns: 250px minmax(0, 1fr); align-items: center; gap: 14px; }
  }
</style>

<nav class="tr-toc" aria-label="In this report">
  <div class="tr-toc-k">In this report</div>
  <ol>
    <li><a href="#summary">Summary</a></li>
    <li><a href="#federal-leaders-are-committed-to-agents-but-controls-lag-adoption">Federal leaders are committed to agents but controls lag adoption</a></li>
    <li><a href="#four-impediments-add-friction-to-agent-delivery-in-government">Four impediments add friction to agent delivery in government</a></li>
    <li><a href="#five-enablers-build-a-foundation-for-governed-agents">Five enablers build a foundation for governed agents</a></li>
    <li><a href="#use-six-strategies-to-accelerate-governed-agent-delivery">Use six strategies to accelerate governed agent delivery</a></li>
    <li><a href="#supplemental-material">Supplemental material</a></li>
  </ol>
</nav>

## Summary

The federal government does not have an interest problem with AI agents. It has a control problem. Published surveys of federal IT leaders show agents already running in production workflows and near-universal agreement that they will matter to the mission. The same surveys show that most agencies have not yet defined the testing, oversight, incident response, or vendor accountability that production use demands. This report outlines why governed delivery has to come first, the impediments that slow it down, the enablers that make it possible, and six strategies for getting agents into production without outrunning the controls.

## Federal leaders are committed to agents but controls lag adoption

The commitment is not in question. In a report ICF and MeriTalk published in October 2026, 85% of the 100 federal IT decision-makers surveyed [expect agentic AI to become critical or very important to their mission](https://www.icf.com/news/2026/10/report-challenge-federal-ai-adoption-operational) within three years, and 45% said their agencies already use it in at least one production or operational workflow (see Figure 1).

The controls tell a different story (see Figure 2). In that same ICF and MeriTalk report, only 35% said their agencies have defined human-in-the-loop review processes for agents. A Market Connections survey of more than 200 government technology executives, [reported by Nextgov/FCW in May 2026](https://www.nextgov.com/artificial-intelligence/2026/05/survey-more-half-federal-agencies-now-planning-agentic-ai-pilots/413324/), found that 20% have defined policies for pre-deployment testing, 8% have a defined framework for incident response, and 6% have a framework for third-party or vendor governance.

This gap is not due to a lack of seriousness. Respondents in the Market Connections survey overwhelmingly said they would require logging, guardrails, and human approval for high-risk data. Leaders know what the controls should be. What lags is the engineering and the process that turn a stated requirement into something enforced.

<figure class="tr-fig" role="img" aria-label="Bar chart: 85% of federal IT leaders expect agentic AI to be critical or very important within three years, 45% report it in at least one production workflow, and 34% are exploring or piloting it">
  <div class="tr-fig-k">Figure 1</div>
  <div class="tr-fig-t">Federal IT leaders are embracing agents</div>
  <div class="tr-row"><div class="tr-lab">Expect agentic AI to be critical or very important to the mission within three years</div><div class="tr-track"><div class="tr-bar" style="width:85%"></div><span class="tr-val">85%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Use agentic AI in at least one production or operational workflow</div><div class="tr-track"><div class="tr-bar" style="width:45%"></div><span class="tr-val">45%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Exploring or piloting agentic AI</div><div class="tr-track"><div class="tr-bar" style="width:34%"></div><span class="tr-val">34%</span></div></div>
  <div class="tr-src">Base: 100 federal IT decision-makers across civilian, defense, and national security agencies. Source: ICF and MeriTalk, "The Agentic Future," October 2026.</div>
</figure>

<figure class="tr-fig" role="img" aria-label="Bar chart of agencies with defined agent controls: 35% human-in-the-loop review, 34% clarified decision authority, 29% documented kill switch procedures, 20% pre-deployment testing policies, 8% incident response framework, 6% vendor governance framework">
  <div class="tr-fig-k">Figure 2</div>
  <div class="tr-fig-t">Few agencies have defined the controls that production requires</div>
  <div class="tr-row"><div class="tr-lab">Defined human-in-the-loop review processes <small>(ICF)</small></div><div class="tr-track"><div class="tr-bar q" style="width:35%"></div><span class="tr-val">35%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Clarified decision authority <small>(ICF)</small></div><div class="tr-track"><div class="tr-bar q" style="width:34%"></div><span class="tr-val">34%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Documented "kill switch" procedures <small>(MC)</small></div><div class="tr-track"><div class="tr-bar q" style="width:29%"></div><span class="tr-val">29%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Defined policies for pre-deployment testing <small>(MC)</small></div><div class="tr-track"><div class="tr-bar q" style="width:20%"></div><span class="tr-val">20%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Defined framework for incident response <small>(MC)</small></div><div class="tr-track"><div class="tr-bar q" style="width:8%"></div><span class="tr-val">8%</span></div></div>
  <div class="tr-row"><div class="tr-lab">Framework for third-party or vendor governance <small>(MC)</small></div><div class="tr-track"><div class="tr-bar q" style="width:6%"></div><span class="tr-val">6%</span></div></div>
  <div class="tr-src">Two separate surveys with different respondents and wording; rows are not directly comparable across sources. ICF: ICF and MeriTalk, "The Agentic Future," October 2026, 100 federal IT decision-makers. MC: Market Connections, sponsored by ServiceNow, March survey of more than 200 government technology executives, reported by Nextgov/FCW, May 2026.</div>
</figure>

### Why governed delivery has to come first

Agencies face real pressure to move, and the mission case for agents is strong. But the public's trust is the asset every federal program spends, and an agent that acts without bounds spends it quickly. Governing agents before scaling them is critical because:

- **An agent acts, and actions carry authority.** A chatbot that is wrong produces a bad answer. An agent that is wrong, or that has been manipulated by text it read, updates a record, sends a message, or provisions infrastructure with whatever permissions it holds. The risk question moves from what the system says to what the system does, and most existing AI policy was written for the first question.
- **The inventory is growing faster than the oversight.** GAO found that generative AI use cases at the agencies it reviewed [grew about ninefold in one year](https://www.gao.gov/products/gao-25-107653), from 32 in 2023 to 282 in 2024. OMB's [consolidated 2025 inventory](https://github.com/ombegov/2025-Federal-Agency-AI-Use-Case-Inventory) lists 3,611 individually reported use cases, 1,818 of them deployed or piloted and 445 designated high-impact. These inventories count all AI, not agents alone, but they show the slope every oversight function is standing on.
- **Bounded early wins build the trust that scale requires.** Agencies in the ICF and MeriTalk report cite measurable benefits in software development (62%), data validation (57%), compliance (56%), and cybersecurity (56%). These are workflows where output is reviewable and actions can be undone. An authorizing official who has watched an agent operate inside tight bounds for six months is far easier to bring along than one asked to approve broad autonomy on a promise.

## Four impediments add friction to agent delivery in government

Government leaders must overcome four impediments to move agents from pilot to production responsibly:

1. **Authorization was built for systems that hold still.** Federal authorization assesses a system at a point in time and then monitors it for drift. An agent's behavior shifts with every model version, tool manifest change, prompt revision, and memory write. None of those look like a configuration change to a traditional change board, yet any of them can alter what the system does. A process that certifies a snapshot will always be describing an agent that no longer exists.
2. **Agents inherit identities that were designed for people.** Many early deployments run an agent on a shared service account or on the invoking user's full permissions. The agent then holds far more authority than the task needs, and the audit log cannot separate what the person did from what the agent did. In the ICF and MeriTalk report, 51% named agent-specific identity and access controls as a safeguard they need before letting agents coordinate across systems.
3. **Workflows were designed around human handoffs.** In the same report, 91% said redesigning workflows is their biggest obstacle to scaling agents, and only 34% have clarified decision authority. Approval chains, separation of duties, and records requirements all assume a named person at each step. Dropping an agent into a process built that way either breaks the control or reduces the agent to a drafting tool.
4. **Prompt injection has no complete fix, and mission systems cannot absorb experiments.** An agent can be steered by any text it reads: a ticket, a PDF, a retrieved page. No filter or fine-tune removes that exposure entirely. In healthcare, law enforcement, defense, and benefits delivery, the systems an agent would touch are systems of record with decades of dependencies. Leaders are right to refuse a control that works only when the model behaves.

## Five enablers build a foundation for governed agents

Government leaders must build a foundation for agent delivery by emphasizing five enablers:

- **Identity.** Every agent needs its own identity, distinct from the person who invoked it and from every other agent. Credentials should be short-lived and scoped to the task. When one agent delegates to another, authority should narrow at each hop and never widen.
- **Enforcement.** Authorization has to be checked at the tool boundary, by a component the agent cannot influence. Guardrails should fail closed, and outbound network access should be denied by default. If a control stops working when the model is compromised, it was advice and not enforcement.
- **Evidence.** Every model call, tool call, and policy decision should land in a structured audit record joined by a single request identifier. That record is what lets an investigator reconstruct an incident and what lets an authorizing official see that a control operated, not just that it was documented.
- **People.** Only 33% of respondents in the ICF and MeriTalk report have trained staff to work with agents. Operators need to know what an agent is permitted to do, how to read its trail, and how to stop it. Reviewers need a workload they can actually review, or human-in-the-loop becomes a signature on output nobody read.
- **Measurement.** Promotion to production should depend on numbers set in advance: attack success rate ceilings scaled to the harm an action could cause, measured against adversaries that adapt, on a pinned model version. Reliability should be measured as success on every one of repeated trials, not success on at least one.

Any agency strategy for agents should include a plan to build up each of these areas, and should treat a gap in one as a limit on how much autonomy the others can support.

## Use six strategies to accelerate governed agent delivery

Government leaders should adopt six strategies to deliver agents without outrunning their controls:

1. **Start where actions are reversible.** Choose first deployments in workflows where the agent's output is reviewed before it takes effect, or where its actions can be undone: code changes behind a pull request, data validation, draft correspondence. Save irreversible actions for after the controls have a track record.
2. **Bound the authorization blast radius before tuning the model.** List every record the agent's credentials can read, every write and delete it can perform, and every destination it can send data to. That list is the damage a manipulated agent can do while working exactly as designed. Shrink it first. Sandboxing limits what an attacker reaches by escaping the runtime, which is the smaller exposure.
3. **Put enforcement outside the agent's reach.** Route every model and tool call through a gateway that authenticates the agent, applies policy, and writes the audit record. Instructions in a system prompt are not a control, because the text an attacker injects sits in the same context window.
4. **Treat every model, tool, and prompt change as a change.** Define in advance which events trigger re-evaluation: a new model version, an added tool, a changed prompt, a new data source. Run the evaluation suite on each one and gate promotion on the result. This is how authorization keeps pace with a system that changes weekly.
5. **Write the stop procedure before the first deployment.** Only 29% of agencies in the Market Connections survey have documented a kill switch procedure, and 8% have an incident response framework for agents. Decide who can halt an agent, how credentials get revoked, and how actions already taken get identified and rolled back. Then rehearse it.
6. **Buy accountability into the contract.** In the Market Connections survey, 44% include liability or responsibility clauses for AI vendors, and 6% have a vendor governance framework. Ask vendors for model version pinning, notice before model changes, access to logs, and disclosure of what the agent's tools can reach. OMB's acquisition guidance in M-25-22 gives contracting officers a starting point.

By working through these strategies, agencies can let autonomy operate inside limits they have chosen deliberately, and can show an authorizing official evidence that the limits hold.

## Supplemental material

### Sources and method

This report is a synthesis of published research and Optimal's own engineering work on agent security. We did not field an original survey or conduct interviews for it. The statistics come from the sources below, and the recommendations are our judgment.

- ICF and MeriTalk, ["The Agentic Future"](https://www.icf.com/news/2026/10/report-challenge-federal-ai-adoption-operational), October 2026. 100 federal IT decision-makers across civilian, defense, and national security agencies.
- Market Connections, sponsored by ServiceNow, March survey of more than 200 government technology executives, as [reported by Nextgov/FCW](https://www.nextgov.com/artificial-intelligence/2026/05/survey-more-half-federal-agencies-now-planning-agentic-ai-pilots/413324/), May 5, 2026. Market Connections is a business division of GovExec, the parent of Nextgov/FCW.
- OMB, [2025 Federal Agency AI Use Case Inventory](https://github.com/ombegov/2025-Federal-Agency-AI-Use-Case-Inventory), consolidated summary as of April 13, 2026.
- GAO, [Artificial Intelligence: Generative AI Use and Management at Federal Agencies](https://www.gao.gov/products/gao-25-107653) (GAO-25-107653), July 29, 2025.

Read the survey figures as directional. Both surveys are industry-run, the samples are small, and they define adoption differently: the Market Connections survey found 15% of agencies implementing agentic AI or finished doing so, while the later ICF and MeriTalk report found 45% using it in at least one production workflow. The federal inventories cover all AI use cases and do not break out agents.

### Related reading

The architecture behind the enablers and strategies above is laid out in our whitepaper, *Securing Agentic AI: Governing What the System Does, Not What It Says*, and summarized in [The Authorization Blast Radius](/blog/authorization-blast-radius).

<p>
  <a class="btn btn-primary" href="/whitepapers/securing-agentic-ai/">Download the whitepaper →</a>
  &nbsp;
  <a class="btn btn-ghost" href="/contact">Book a scoping call</a>
</p>
