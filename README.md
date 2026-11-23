# Amit Vitekar

AI and systems security. Most of what I do is find the place where two
components disagree about what an input is, then build the smallest thing that
proves it.

[**Breakpoint**](https://r00tb3.github.io/breakpoint/) ·
[LinkedIn](https://www.linkedin.com/in/amitvitekar/) ·
[X](https://x.com/r00tb3)

---

## Projects

### [mcp-confused-deputy](https://github.com/r00tb3/mcp-confused-deputy)

`Python` · `MCP` · `agent security`

A deliberately vulnerable MCP tool broker. An agent scoped to `fs.read` and
`fs.write` sends a file write with two fields its schema never declared —
`escalate: true` and an `escalation_note`. The broker reads them anyway,
reloads a service on its own authority, and files the reload under the agent's
request. The agent never had permission and never needed it.

Ships with a four-step browser walkthrough, a vulnerable and a hardened mode,
an end-to-end verifier, and 36 tests. No dependencies beyond Python 3.10.

→ [Source](https://github.com/r00tb3/mcp-confused-deputy) ·
[88-second walkthrough](https://cdn.jsdelivr.net/gh/r00tb3/mcp-confused-deputy@main/demo/walkthrough.webm)

### [RAG-Poisoning-Lab](https://github.com/r00tb3/RAG-Poisoning-Lab)

`Python` · `RAG` · `detection`

A runnable RAG pipeline you can poison, with three detection checks measured
against the repo's own payloads — something the original README had not done.

The similarity check separates clean from poisoned perfectly, but its shipped
threshold never fires, so it catches nothing. The keyword filter catches two
payloads by also rejecting nine of ten plausible clean documents. Perplexity
cannot separate the two populations at any threshold, because their ranges
overlap.

→ [Source](https://github.com/r00tb3/RAG-Poisoning-Lab) ·
[Write-up: *Nine of Ten*](https://r00tb3.github.io/breakpoint/rag-poisoning/)

### [Breakpoint](https://r00tb3.github.io/breakpoint/)

`security research` · `long-form writing`

Where I write the long version: baseband firmware, telecom networks, and
machine-learning security, with the evidence and its limits stated plainly.

→ [Blog](https://r00tb3.github.io/breakpoint/) ·
[About](https://r00tb3.github.io/breakpoint/about/)

---

## Writing

| Post | Topic | Published |
|---|---|---|
| [*Nine of Ten* — Measuring Three Defences in a RAG Poisoning Lab](https://r00tb3.github.io/breakpoint/rag-poisoning/) | AI security · RAG | 14 Oct 2026 |
| [*The Eleventh Slot* — An IMS SDP Heap Overflow in Exynos Modem Firmware](https://r00tb3.github.io/breakpoint/cve-2023-24033/) | Baseband · CVE-2023-24033 | 12 Aug 2026 |

---

## The same bug three times

A parser and a policy engine disagree about the length of a list. A broker and a
tool schema disagree about which fields are real. A detector and a corpus
disagree about what "normal" means.

The reason this shape keeps working is that each component is correct on its own
terms. The bound check exists, in a different loop. The schema is enforced, by
the client. The threshold is calibrated, on a distribution that isn't the one in
production. A reviewer finds the check and stops looking.

So most of my work is finding that seam and measuring it. "This is broken" is an
opinion until there's a number.

---

## Background

Baseband and telecom came first: modem firmware, IMS/VoLTE stacks, LTE and 5G
protocol work, SDR-based fuzzing. That's where I learned to read a control-flow
graph and to distrust a comment.

The AI security work grew out of noticing the same shapes in agent tooling.
Unvalidated input crossing a trust boundary, with a component on the far side
that trusts it. Same discipline, newer surface.

**Training:** HTB AI Red Teamer, Microsoft AI Red Teaming, NVIDIA Adversarial ML,
100x Engineers GenAI cohort.

**Tools:** Python, C, Docker, Linux, FAISS, LangChain, AFL++, Scapy, USRP,
BladeRF.
