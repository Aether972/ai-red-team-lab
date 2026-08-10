# ai-red-team-lab

**A public lab notebook for learning to break — and secure — LLM systems.**

Started 10 August 2026. Target: employed in an AI security role by December 2027.

---

## The mission

I'm building the skills to red team AI systems, in public, from day one.

Not a tutorial collection. This repository is the working notebook: experiments that failed, mental models that were wrong and got corrected, payloads that only work 3 times out of 10 and why that's still a finding. Published as it happens rather than after it's polished.

The commitment is deliberately public because this field hires on demonstrated output, not credentials. If I'm going to make that claim, the evidence should be visible and timestamped.

**Target date: December 2027.** Progress against it is tracked below, updated weekly.

---

## Where I'm coming from

Security background, not an ML background — and the gap is the interesting part.

- **Smart contract auditing** — findings in public audit contests. Adversarial reasoning about systems where the attacker controls more of the input than the designer assumed. Indirect prompt injection turns out to be the same question on a different substrate.
- **DevSecOps** — CI/CD, containers, supply chain. Directly relevant to model supply chain and ML infrastructure security.
- **SOC / CSIRT and GRC in a regulated bank** — detection engineering on one side, control evidence and audit on the other. Relevant to the EU AI Act and NIST AI RMF work in the later phases of this project.

What I did not have on day one: transformer internals, adversarial ML, or any of the tooling. That's what the first phase is for, and the notes are all here.

---

## Scope and ethics

This repository documents offensive security research. The rules I work under:

- **Authorized targets only.** Systems I own and built to be vulnerable, public CTFs and challenge platforms (Gandalf, HackAPrompt, Gray Swan), or targets inside the scope of a published bug bounty program.
- **Responsible disclosure.** Findings against real products go to the vendor's program first. Public writeups follow disclosure timelines, and details are withheld where the program requires it.
- **No weaponization.** Payloads and harnesses published here are for evaluating and hardening systems. Techniques that produce genuinely harmful model output are described at the mechanism level, without working payloads for the harmful content itself.
- **Reproducibility over spectacle.** Every claimed technique reports a success rate across at least two models. A single lucky screenshot isn't a result.

If you believe something here crosses a line, open an issue and I'll take it seriously.

---

## Progress

| Artifact | Now | Target (Dec 2027) |
|---|---|---|
| Published writeups | 0 | 25–35 |
| Original tools / repos | 1 | 4–6 |
| Merged PRs to upstream red team tooling | 0 | ≥ 1 |
| Professional red team reports | 0 | 2 |
| Bug bounty findings (AI programs) | 0 | 3–8 |
| Conference talks / accepted CFPs | 0 | 1 |

**Current phase:** Phase 0 — Foundations & Lab (10 Aug – 20 Sep 2026)
**This week:** LLM internals — tokenization, attention, sampling, chat templates. First writeup ships Sunday.

---

## Writeups

Published research lives in [`/writeups`](./writeups) and is indexed here as it goes out.

*Nothing published yet — first post scheduled 16 August 2026.*

---

## Repository structure

```
notes/         Mental models. How the machine actually works.
labs/          Hands-on experiments. Messy on purpose.
writeups/      Published research, one directory per post.
tools/         Scripts and harnesses that outgrew a notebook.
threat-models/ Architecture and trust-boundary analysis of LLM apps.
```

Larger pieces of work graduate into their own repositories and get linked from here. This one stays the index and the notebook.

---

## Stack

**Models** — Ollama (Llama 3.1, Mistral, Qwen 2.5) for local work, frontier APIs for capability-gap testing
**Red team tooling** — garak, PyRIT, promptfoo, Giskard
**Defense** — NeMo Guardrails, Llama Guard
**Infra** — Python 3.12, uv, Jupyter, Chroma / pgvector, FastAPI

---

## Frameworks I'm working against

- OWASP Top 10 for LLM Applications (2025)
- MITRE ATLAS
- NIST AI Risk Management Framework
- EU AI Act (GPAI obligations)

---

## Roadmap

Four phases over 72 weeks:

| Phase | Window | Focus |
|---|---|---|
| 0 | Aug – Sep 2026 | Foundations, model internals, lab setup |
| 1 | Sep – Dec 2026 | Core attack surface: injection, jailbreaks, RAG, output handling |
| 2 | Jan – Apr 2027 | Agentic systems, MCP, supply chain, adversarial ML |
| 3 | May – Aug 2027 | Defense, guardrails, governance, market entry |
| 4 | Sep – Dec 2027 | Job hunt while still shipping |

---

## Contact

Open an issue, or reach me on LinkedIn. If you work in this field and think I'm getting something wrong, I'd rather hear it now than in an interview.

---

*Public because deadlines with witnesses get met.*
