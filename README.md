<h2 align="center">👋 Hi, I'm Homen Shum</h2>

<h3 align="center">Building <a href="https://github.com/HomenShum/noderoom">NodeRoom</a> — a live room where humans and AI agents do high-trust research together, without clobbering each other.</h3>

<p align="center"><em>A career, compiled: banking/finance → data engineering → agentic AI, converging on human-agent collaboration systems where the agent leaves receipts.</em></p>

<p align="center"><sub>
<b>Meta</b> · agentic QA (PQX) &nbsp;·&nbsp; <b>JPMorgan</b> · 3.5 yrs, credit + agentic-RAG over 100k+ docs &nbsp;·&nbsp; <b>Ideaflow</b> &nbsp;·&nbsp; Founder, <b>NodeBench&nbsp;AI</b> &nbsp;·&nbsp; UC&nbsp;Santa&nbsp;Barbara &nbsp;·&nbsp; <a href="https://www.linkedin.com/in/homen-shum/">full&nbsp;history&nbsp;↗</a>
</sub></p>

<p align="center">
  <a href="https://github.com/HomenShum/noderoom"><img src="https://img.shields.io/badge/flagship-NodeRoom-111?style=flat" alt="NodeRoom"></a>
  <a href="https://www.linkedin.com/in/homen-shum/"><img src="https://img.shields.io/badge/LinkedIn-connect-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://komarev.com/ghpvc/?username=HomenShum&color=181717&style=flat" alt="profile views">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Convex-EE342F?style=flat-square&logo=convex&logoColor=white" alt="Convex">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TipTap-000000?style=flat-square&logo=tiptap&logoColor=white" alt="TipTap">
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright">
</p>

---

<!--
HERO — real walkthrough GIF (assets/noderoom-hero.gif): the "Live Startup Diligence War Room", encoded from docs/walkthroughs/startup-diligence-war-room.mp4 (t3–t17, 820px, 10fps).
A lighter static fallback still lives at assets/noderoom-hero.svg if you ever want it.

Original capture notes (kept for reference): ~10-15s, no audio, ≤820px, seamless loop.
Capture rig: Playwright drives a real session → Remotion frames → ffmpeg to GIF (so the hero doubles as a smoke test — record it the way you ship it).

  Beat 1 — THE ROOM IS ALIVE: open on the shared diligence sheet with TWO human cursors + at least one NodeAgent badge in the same room. A NodeAgent cell visibly fills ("Series A · $12M · led by ___") while a human types in an adjacent cell. Coexistence, not takeover.
  Beat 2 — SAFE SHARED EDITS (the money beat): trigger lock → draft → smart-merge on one row. The agent claims an affected-range lock, the human's nearby in-progress edit is NOT overwritten, the draft merges in. Hold on the "preserved your edit" / no-clobber affordance.
  Beat 3 — EVIDENCE STREAMS IN: findings stream into the sheet (a variance column fills), the note panel, and the post-it wall; a source chip snaps onto a claim. Evidence attached, not asserted.
  Beat 4 — REVIEW-READY: end on the review artifacts — company brief + runway chart + open-questions list.

  Direction: one unbroken flow, no cuts; hide chrome/devtools; cursor labels on (who is human, who is agent). If it runs long, sacrifice Beat 3, never Beat 2. Use feature-walkthrough-gif (below) to make it reproducible.
-->

<p align="center">
  <img src="./assets/noderoom-hero.gif" alt="NodeRoom — Live Startup Diligence War Room: humans + NodeAgents run shared research on a live diligence sheet — lock → draft → smart-merge with no-clobber proof" width="820">
</p>

---

### 🗺️ The system map — one lineage, not scattered repos

| Repo | Layer | What it is |
| --- | --- | --- |
| **[noderoom](https://github.com/HomenShum/noderoom)** ⭐ | **Current flagship** | Live multi-panel room where humans + NodeAgents edit a shared spreadsheet, note, and post-it wall through one versioned concurrency model — `lock → draft → smart-merge`, no-clobber, per-element CAS. |
| **[nodebench-ai](https://github.com/HomenShum/nodebench-ai)** | Research engine | Entity intelligence for any company, market, or question — searches + synthesizes with sources, turns each run into a reusable artifact, and ships a hosted public-research MCP. |
| **[NodeAgent](https://github.com/HomenShum/NodeAgent)** | Agent kernel | The distilled core of NodeBench — one loop, four tool UIs: live context, grounded/cited search, a versioned spreadsheet delta, and a TipTap notebook memo. |
| **[feature-walkthrough-gif](https://github.com/HomenShum/feature-walkthrough-gif)** | Proof / media | Playwright → Remotion → ffmpeg turns any feature into an annotated walkthrough GIF — and because it's scripted, the GIFs double as an integration smoke-test. |
| **[local-collab-mvp](https://github.com/HomenShum/local-collab-mvp)** | Room OS | Why co-located voice agents collapse into "yeah, exactly…" loops — and the fix: one server-authoritative room state (floor control, deterministic reducer), proven by side-by-side bad/good traces and a measured 6-model coordinator eval. |
| **[proofloop](https://github.com/HomenShum/proofloop)** | Completion gate | Bring any coding agent — proofloop blocks "done" until an executable proof gate passes: Stop-hook refusal, agent-tamper-proof proof state, fail-closed tool contracts. Zero runtime dependencies. |

<sub>Productivity infra: **[gmail-workspace-public](https://github.com/HomenShum/gmail-workspace-public)** (large inbox → one queue, one decision; private data stays local, public research delegated to NodeBench) · **[agent-workspace-template](https://github.com/HomenShum/agent-workspace-template)** (reusable Convex/Next agent-workspace runtime).</sub>

<sub>Also fresh (Jun–Jul 2026): **[noderl](https://github.com/HomenShum/noderl)** (agentic-RL substrate: trace → reward → memory → repair; 100/100 benchmark tasks scored with zero answer-key writers) · **[NodeMem](https://github.com/HomenShum/NodeMem)** (passive agent memory behind a 6-gate suppression pipeline) · **[visual-judge](https://github.com/HomenShum/visual-judge)** (deterministic browser evidence + a Gemini video critic) · **[solo-founder-agent-builder](https://github.com/HomenShum/solo-founder-agent-builder)** (one-prompt build run passing 32/33 executable proof gates).</sub>

---

### 🧬 The lineage

<sub>📜 Context: **[TIMELINE.md](./TIMELINE.md)** — the field's viral agent moments (ELIZA → scratchpads → AutoGPT → Manus), the layer every one of them was missing, and where each repo below sits on that map.</sub>

```mermaid
flowchart LR
    NB["NodeBench AI<br/>research / diligence engine<br/>sourced dossiers · MCP"]
    NA["NodeAgent<br/>distilled agent kernel<br/>one loop · four tool UIs"]
    NR["NodeRoom<br/>CURRENT FLAGSHIP<br/>live room · lock→draft→merge"]
    RO["Room OS<br/>shared-state voice agents<br/>floor control · loop suppression"]
    PF["Proof<br/>walkthrough GIFs + proofloop gates<br/>demos that double as tests"]

    NB -->|distill the core| NA
    NA -->|put humans + agents in one room| NR
    NR -->|many agents, one floor| RO
    NR -->|ship review-ready artifacts| PF

    style NR fill:#111,color:#fff,stroke:#111
```

---

### 🛠️ A career, compiled

Five capability buckets, each load-bearing in the work above:

- **Banking & diligence** — 3.5 yrs at JPMorgan: credit analysis (72 deals, ~$800M, 270 models) plus "LLMsuite," an agentic-RAG diligence tool over 100k+ documents. Turning messy research into structured, *cited* sheets and risk models — the reason NodeRoom is a War Room, not a toy.
- **Data engineering** — pipelines, schemas, reactive runtimes (Convex), durable streaming. The plumbing under every live room and report.
- **Agentic AI & evals** — agentic QA at Meta (PQX) and eval pipelines at Ideaflow: grounded search, tool loops, versioned model deltas, LLM-as-a-Judge scoring, scenario-based tests. Agents that get checked, not trusted — the harness matters more than the model.
- **Healthcare / regulated workflows** — prior-auth auto-fill with validation + eval: structured extraction where being wrong has consequences.
- **Product engineering** — Next.js / React / TS surfaces, UI parity harnesses, reproducible demos. The artifacts people actually click.

---

### 🎯 Current flagship demo — NodeRoom: Live Startup Diligence War Room

Multiple humans and multiple NodeAgents research companies **in one live room** and enrich a shared diligence sheet together:

- Agents claim an **affected-range lock** (still readable as context), a blocked agent **drafts around** it, and on unlock the draft **smart-merges** — committed human edits are never clobbered. Every edit carries a per-element version (**CAS**).
- Findings **stream** into the sheet, the note panel, and the post-it wall — no refresh; server-led agent work reaches every client (e.g. the live `Q3DEMO` room, `/ask reconcile Q3 revenue` filling a variance column).
- Runs **two modes from the same code**: a deterministic **no-key** in-memory engine + scripted agents (`npm run demo`), and **Live** with a real Convex reactive backend + a model-routed LLM agent (routes promoted by ladder evidence, not provider brand).
- Ends with **downstream-ready review artifacts**: company brief, runway chart, open-questions list.

> **People + agents + artifacts + evidence + review + shareability.**

---

<details>
<summary><b>📚 Selected earlier work</b> — the arc that compiled into the systems above</summary>

<br>

| Project | Signal |
| --- | --- |
| [parity-studio](https://github.com/HomenShum/parity-studio) | Image (or live app route) → verified componentized `ui_kit`, self-judged on a 16-check deterministic rubric with honest score drift. |
| [LLM Prior Authorization](https://github.com/HomenShum/LLM-Prior-Authorization-Form-Auto-Fill-System-With-Eval) | LLMs auto-fill prior-auth forms from patient notes — structured extraction, validation pass, LLM-as-a-Judge eval scored on clinical knowledge. |
| [Banking assistant](https://github.com/HomenShum/Banking_assistant_streamlit) | Finance-document assistant for company/PDF analysis — the diligence reflex, pre-NodeBench. |
| [openai-agent-eval-framework](https://github.com/HomenShum/openai-agent-eval-framework) | Agent evaluation for classification, context verification, and pruning — the eval discipline, early. |
| [CosmaNeura med billing](https://github.com/HomenShum/CosmaNeura-Med-Billing) | ICD/CPT recommendation from physician dictation — regulated extraction before the prior-auth system. |
| [FluencyMed](https://github.com/HomenShum/FluencyMed-Pub) | Early healthcare AI workflow prototype. |
| [voice_email_agent](https://github.com/HomenShum/voice_email_agent) | Email ingestion, summarization, embeddings, voice query — the seed of the Gmail workspace. |

</details>

---

### 💡 What I care about

**The agent should leave receipts.** Sources on every claim, a version on every edit, an eval on every answer, and a demo anyone can reproduce. High-trust work doesn't get faster by trusting the model more — it gets faster by making the model *checkable*.

Autonomous task horizons are [doubling roughly every seven months](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/). When AI labor becomes schedulable, the hard questions stop being "how smart" and become *who owns the state, who audits the decisions, who holds the floor, who can pause the fleet.* Chat windows don't answer those questions — **rooms do**. That's the bet behind everything above ([the full timeline →](./TIMELINE.md)).

📫 [LinkedIn](https://www.linkedin.com/in/homen-shum/) · `hshum2018@gmail.com`
