# Konstantinos Sohos

Software engineer and founder building local-first systems in Athens.

I like software that runs on your own machine and keeps working when nothing
else does — a Markdown vault with hybrid semantic search, a news intelligence
engine with a live map, and an AI assistant for small hotels. No accounts, no
cloud, no telemetry.

## What I build

### [local-brain](https://github.com/ksohos333/local-brain) · `local-brain`

A private, local-first knowledge brain. Notes stay as plain Markdown files you
own; search runs against a local SQLite database with FTS5 full-text and
sqlite-vec vector similarity, ranked together.

- **Hybrid retrieval** — keywords and semantics in one query
- **MCP server** — `search_memory`, `recent_context`, `index_memory`, so AI
  tools can query the vault directly
- **37 REST endpoints**, a FastAPI backend and a PySide6 desktop shell
- **Fully offline** — embeddings computed locally with `fastembed` or Ollama

`Python · FastAPI · MCP · RAG · embeddings · SQLite · sqlite-vec · PySide6`

### [local-butler](https://github.com/ksohos333/local-butler) · `local-butler`

A platform of eight Python applications under one host process.

- **GeoNews** — 25 primary-source feeds, geolocated and plotted on a live
  Leaflet map, with Bayesian trend scoring, an LLM research agent, and
  prediction markets
- **Calendar** — a natural-language scheduler driving a local CalDAV server
- **Money Tracker**, **Diagnostic** (a GTK Linux troubleshooter) and a
  **Privacy Dashboard** that shows what is holding the camera and microphone
- **393 tests passing** — API, data model, scheduling and ingestion pipelines

`Python 3.12 · FastAPI · SQLAlchemy · Alembic · SQLite · Jinja2 · Leaflet · pytest`

### [kalo-concierge](https://github.com/ksohos333/kalo-concierge) · `kalo-concierge`

A WhatsApp or Viber assistant for small Greek hotels — a pilot I am running one
hotel at a time, built from conversations with owners rather than from a spec.

The assistant answers recurring guest questions in the guest's own language,
passes anything about bookings to the owner, and only ever uses information the
hotel has given it — it never invents prices, availability or policies.

`Product · AI · Hospitality · Greece · Privacy-first`

### [kaloconcierge-site](https://github.com/ksohos333/kaloconcierge-site) · `kaloconcierge-site`

The bilingual, zero-tracking website for the above — plain HTML and CSS, no
build step, no cookies, no analytics, and nothing in the code that could
collect data.

`HTML · CSS · Static · Bilingual EN/ΕΛ · Vercel`

## Stack

**Languages** — Python, JavaScript, SQL, Bash, HTML, CSS
**Backend** — FastAPI, SQLAlchemy, Alembic, Pydantic, REST, PostgreSQL, SQLite
**Frontend** — Vanilla JS, Leaflet, Jinja2, HTML5, CSS3
**AI** — RAG, embeddings, MCP, llama.cpp, Bayesian modelling, feed parsing
**Testing** — pytest, pytest-asyncio, integration testing

## Currently

- Running a small pilot for [Kalo Concierge](https://kaloconcierge.com) and
  building the assistant behind it.
- Publishing the platforms above properly, with documentation and tests I can
  defend.
- Learning the fundamentals properly rather than shipping on vibes — reading
  other people's code, writing tests that matter, and understanding why a
  system fails.

## Elsewhere

- Website — [kaloconcierge.com](https://kaloconcierge.com)
- Email — [ksohos@kaloconcierge.com](mailto:ksohos@kaloconcierge.com)
- LinkedIn — [linkedin.com/in/konstantinos-sohos](https://linkedin.com/in/konstantinos-sohos)
