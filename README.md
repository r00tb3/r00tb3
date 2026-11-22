# Amit Vitekar

AI and systems security. Most of what I do is find the place where two
components disagree about what an input is, then build the smallest thing that
proves it.

---

## Things I've built

**[mcp-confused-deputy](https://github.com/r00tb3/mcp-confused-deputy)**

A tool broker that reads arguments nobody gave it. An agent scoped to `fs.read`
and `fs.write` sends a file write with two extra fields its schema never
declared. The broker reads them anyway, reloads a service on its own authority,
and files the reload under the agent's request. The agent never had permission
and never needed it.

There's a four-step walkthrough in a container, a vulnerable broker, a hardened
one, and 36 tests that show the difference between them.

**[RAG-Poisoning-Lab](https://github.com/r00tb3/RAG-Poisoning-Lab)**

A runnable RAG pipeline with three detection checks. I measured each one against
the repo's own payloads, which is a thing the original README had not done.

The similarity check separates clean from poisoned perfectly, and its shipped
threshold never fires, so it catches nothing. The keyword filter catches two
payloads by also rejecting nine of ten plausible clean documents. Perplexity
can't separate the two populations at any threshold, because their ranges
overlap.

I wrote up [the measurements](https://r00tb3.github.io/breakpoint/rag-poisoning/)
rather than the marketing.

**[Breakpoint](https://r00tb3.github.io/breakpoint/)**

Where I write the long version. The current post is
[a heap overflow in Exynos modem firmware](https://r00tb3.github.io/breakpoint/cve-2023-24033/):
finding the SDP parser in a Pixel 6 image, rebuilding the dispatch chain, and
reproducing the overflow from the real IMS entry point under full-system
emulation. About 6,000 words, and it says where the evidence stops.

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

---

## Elsewhere

[Breakpoint](https://r00tb3.github.io/breakpoint/) ·
[LinkedIn](https://www.linkedin.com/in/amitvitekar/) ·
[X](https://x.com/r00tb3)
