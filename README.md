# Konstantinos Sohos

**I build AI systems that are allowed to say "I don't know" — and that can prove why.**

Athens, Greece · native English, native Greek · [linkedin.com/in/konstantinos-sohos](https://linkedin.com/in/konstantinos-sohos) · [kaloconcierge.com](https://kaloconcierge.com) · konstantinos.sohos@gmail.com

---

## The thesis

Most AI tooling is optimised for *always answer*. The interesting engineering is in the opposite direction: knowing when not to answer, proving where a claim came from, and keeping a human in control of anything irreversible.

That is the line all of these projects sit on — an assistant that refuses rather than guesses, an agent that needs permission before it acts, and a log that proves afterwards what actually happened.

## What I build

### [`local-brain`](https://github.com/ksohos333/local-brain) — private, local-first knowledge brain · Python
Hybrid retrieval over a personal Markdown vault: FTS5 keyword search ranked together with sqlite-vec vector similarity, embeddings computed locally, and an MCP server so other tools can query it. Fully offline — no cloud, no telemetry, no account.

- **The hard problem:** ranking where keyword relevance and semantic similarity disagree, and making the ranking explainable instead of a black box.
- **The trade-off I'd defend:** a fully offline stack costs retrieval quality versus a hosted embedding API. For a personal knowledge vault that trade is right, and it means the vault never leaves the machine.

`Python · FastAPI · MCP · RAG · embeddings · SQLite · sqlite-vec · PySide6`

### [`agent-desktop`](https://github.com/ksohos333/agent-desktop) — guarded browser & desktop control · Python
An MCP server exposing 37 tools behind a policy engine: destructive actions require a confirmation token, secrets are redacted from tool output, and every action is written to a JSONL audit trail. **41 automated tests passing**, plus CI.

- **The hard problem:** an agent with real capabilities is also a liability. The policy layer is not a wrapper around the tools — it is the thing that decides whether a tool call is allowed to happen.
- **The trade-off I'd defend:** confirmation tokens add friction. I kept it on the destructive path only, because friction applied everywhere is friction people route around.

`Python · MCP · policy engine · secret redaction · JSONL audit trail · pytest`

### [`anticonf`](https://github.com/ksohos333/anticonf) — anti-confabulation MCP server · Python
Returns raw observed facts and never verdicts. Built on one principle: an assistant that cannot check a claim should say so, so that downstream systems can audit where a conclusion came from.

- **The hard problem:** resisting the urge to be useful. A tool that answers anyway is worse than a tool that refuses, because it launders a guess as a result.
- **The trade-off I'd defend:** the tool is much less convenient than one that returns an answer. That is the point — the caller decides what to do with a fact; it should not inherit my confidence.

`Python · MCP · LLM · verifiability · fact provenance`

### [`openklawc`](https://github.com/ksohos333/openklawc) — Rust TUI coding agent · Rust
A native terminal coding agent with multi-provider LLM streaming, bundled MCP servers, a policy engine and a written audit trail. Rust workspace of multiple crates with integration tests.

- **The hard problem:** keeping a terminal UI responsive while a model streams and tools run — and making a destructive tool call visible *before* it executes.
- **The trade-off I'd defend:** a TUI instead of a web UI. It keeps the whole agent in one process with no browser in the loop, which makes the audit trail trivial to keep complete.

`Rust · CLI · TUI · MCP · streaming LLM · policy engine`

### [`pocketai`](https://github.com/ksohos333/pocketai) — offline AI chat for Android · Kotlin
On-device chat where llama.cpp runs entirely on the phone — an embedded build of llama-server, plus a Termux flavour. No cloud, no account, nothing leaves the device.

- **The hard problem:** a quantized model and an inference runtime that fit on a phone and stay responsive.
- **The trade-off I'd defend:** on-device only. It caps model quality versus a hosted API, and in exchange the conversation never leaves the device — which for a phone is usually the point.

`Kotlin · Android · llama.cpp · on-device inference · privacy`

### [`asclepius`](https://github.com/ksohos333/asclepius) — provenance-tracked health MCP · Rust
A root-cause, natural-first physician that interprets lab work with dual reference ranges and records the provenance of every figure it reports.

- **The hard problem:** making a model's clinical framing traceable back to specific values, so a human can check it rather than trust it.
- **The trade-off I'd defend:** refusing to give a single verdict. It gives ranges and the reasoning between them, which is less satisfying and more honest.

`Rust · MCP · provenance · clinical reasoning · evidence grading`

## Also here

[`local-butler`](https://github.com/ksohos333/local-butler) (eight local-first Python apps under one host) · [`web_research`](https://github.com/ksohos333/web_research) (keyless web research MCP) · [`klisi`](https://github.com/ksohos333/klisi) (Greek conjugation, TypeScript) · [`leoforio`](https://github.com/ksohos333/leoforio) (Go, live transit for Athens) · [`pocketai`](https://github.com/ksohos333/pocketai) · [`kalo-concierge`](https://github.com/ksohos333/kalo-concierge) (the product: an AI assistant for small Greek hotels) · [`kaloconcierge-site`](https://github.com/ksohos333/kaloconcierge-site) (bilingual, zero-tracking site)

## How I build

I use AI coding assistants as part of my workflow — the way most teams now do. **My responsibility is architecture, integration, test coverage and evaluation**, and I own every decision in these repositories. The parts of that work that interest me are the ones where the obvious implementation is wrong: what an assistant should refuse to answer, what an agent needs before it is allowed to act, and how you prove afterwards what actually happened.

Everything here is verifiable — clone it, run it, read the tests. If a claim on this page is not backed by code, it should not be on this page.

## Currently

- Building Kalo Concierge — an AI assistant for small Greek hotels, in research and pilot stage.
- Learning to own the code I have already written, line by line, and re-implementing the core of it without assistance.
- Open to junior AI-tooling, AI application engineering, agent-platform and solutions-engineering roles in Athens or remote.

## Background

BA (Hons) Philosophy, Politics and Economics, Lancaster University (2026), economics concentration, dissertation graded A+ for econometric analysis on a 61,669-response dataset. Before this: client-facing consulting and business analysis (180 Degrees Consulting, Picky Eater), policy research at the Richardson Institute, and an investment internship at FounderPartners.

*Mathematics and statistics are how I got comfortable with data; politics is how I got interested in who a system answers for and who it leaves out. Both showed up in the work above.*
