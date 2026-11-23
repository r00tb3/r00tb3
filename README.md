# 👋 Hi, I'm Amit Vitekar

**Security Researcher** | AI & Systems Security | I find where two components disagree about what an input is, then build the smallest thing that proves it

[![Breakpoint](https://img.shields.io/badge/Breakpoint-E61919?style=for-the-badge&logo=rss&logoColor=white)](https://r00tb3.github.io/breakpoint/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amitvitekar/)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/r00tb3)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/r00tb3)

## 🚀 About Me

I'm a security researcher working at the seam between AI systems and the infrastructure they run on. Most of my work starts with two components that each believe they are correct — a parser and a policy engine, a broker and a tool schema, a detector and a corpus — and ends with the smallest proof that they disagree.

Baseband and telecom came first. Agent tooling is where the same shapes keep showing up.

- 🔬 **Current focus**: MCP and agent-tool security, RAG poisoning, confused-deputy privilege escalation
- 🧪 **Flagship lab**: `mcp-confused-deputy` — a vulnerable MCP broker with a four-step walkthrough, a hardened mode, an end-to-end verifier, and 36 tests
- 📝 **Writing**: long-form security research at [Breakpoint](https://r00tb3.github.io/breakpoint/), with the evidence and its limits stated plainly
- 🎓 **Training**: HTB AI Red Teamer, Microsoft AI Red Teaming, NVIDIA Adversarial ML, 100x Engineers GenAI cohort
- 📡 **Background**: modem firmware, IMS/VoLTE stacks, LTE and 5G protocol work, SDR-based fuzzing

## 🔧 Technologies & Tools

**Languages & Core**
- Python, C, Linux, Docker, Git

**AI Security**
- RAG pipelines (FAISS, LangChain), prompt injection, data poisoning, detection evaluation

**Offensive Tooling**
- AFL++, Scapy, USRP, BladeRF, custom protocol fuzzing

**Research**
- Baseband and telecom protocol analysis, firmware reverse engineering, full-system emulation

---

## 🌟 Featured Projects

### 🧩 [mcp-confused-deputy](https://github.com/r00tb3/mcp-confused-deputy)
**MCP Security | Confused-deputy privilege escalation**

- An agent scoped to `fs.read` and `fs.write` smuggles `escalate: true` into a file call; the broker honours it and reloads a service on its own authority.
- Ships two policies over the same broker — vulnerable and hardened — plus an end-to-end verifier and 36 tests that prove the difference.
- Four-step browser walkthrough; no dependencies beyond Python 3.10.
- **Tech**: Python, MCP, JSON-RPC, streamable HTTP, Docker

→ [Source](https://github.com/r00tb3/mcp-confused-deputy) · [88-second walkthrough](https://cdn.jsdelivr.net/gh/r00tb3/mcp-confused-deputy@main/demo/walkthrough.webm)

### ☠️ [RAG-Poisoning-Lab](https://github.com/r00tb3/RAG-Poisoning-Lab)
**AI Security | Data poisoning and detection**

- A runnable RAG pipeline you can poison, with three detection checks measured against the repo's own payloads.
- The similarity check separates clean from poisoned, but its shipped threshold never fires. The keyword filter rejects nine clean documents to catch two payloads. Perplexity cannot separate the populations at any threshold.
- **Tech**: Python, RAG, FAISS, LangChain

→ [Source](https://github.com/r00tb3/RAG-Poisoning-Lab) · [Write-up: *Nine of Ten*](https://r00tb3.github.io/breakpoint/rag-poisoning/)

### 📝 [Breakpoint](https://r00tb3.github.io/breakpoint/)
**Security Research | Long-form writing**

- Baseband firmware, telecom networks, and machine-learning security, with reproduction steps and evidence limits.
- Latest: [*Nine of Ten*](https://r00tb3.github.io/breakpoint/rag-poisoning/) (RAG poisoning) and [*The Eleventh Slot*](https://r00tb3.github.io/breakpoint/cve-2023-24033/) (an IMS SDP heap overflow in Exynos modem firmware).

→ [Read the blog](https://r00tb3.github.io/breakpoint/) · [About](https://r00tb3.github.io/breakpoint/about/)

## 🏆 Goals for 2026

- 🧩 Publish the long-form write-up for the MCP confused-deputy lab
- 🛠️ Land a real fix in an MCP or agent-security scanner upstream
- 📏 Keep measuring detection claims instead of repeating them
- 📡 Publish one more baseband or telecom deep dive

## 🤝 Let's Connect!

I'm always interested in discussing:

- 🤖 Agent tool security and MCP
- ☠️ RAG and LLM data poisoning, and how to detect them
- 📡 Baseband, telecom, and SDR research
- 🚀 Security tooling, disclosure, and research collaborations

**Reach out via:**

- 🌐 [Breakpoint](https://r00tb3.github.io/breakpoint/)
- 🔗 [LinkedIn](https://www.linkedin.com/in/amitvitekar/)
- 🐦 [X](https://x.com/r00tb3)
- 💻 [GitHub](https://github.com/r00tb3)

**Open to AI-security and offensive-security roles, research collaborations, and speaking.**

**Thanks for visiting! Explore the labs, read the write-ups, and get in touch. 🔍**
