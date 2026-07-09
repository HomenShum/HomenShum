# The agentic-AI timeline — and the layer every viral moment was missing

Every time AI has gone viral since 1966, it's because the public saw one **new fragment of agency** move from research into their hands: it talks, it thinks, it uses tools, it loops, it remembers, it controls software, it works while you sleep. Each fragment produced a wave of demos — and each wave broke on the same rocks: **no shared state, no durable control, no auditable coordination.**

That gap is what I build. This page maps the field's viral moments to the fragment each one proved, and to the repos where I work on the layer they were all missing.

---

## The viral moments

| When | Moment | The fragment it proved |
| --- | --- | --- |
| 1966 | **ELIZA** | *It talks.* Pattern matching, but people anthropomorphized it anyway — the original chatbot illusion. |
| 1968–70 | **SHRDLU** | *Language can act on a world model.* "Move the red block" — language + state + environment beats pure chat. |
| 1980s–90s | **BDI agents** | *Agents can be architected*: beliefs, desires, intentions — the ancestor of today's state + goal + policy framing. |
| 2011 | **Siri** (iPhone 4S) | *Assistants go mainstream* — but as command routers, not workers. |
| 2020 | **RAG** (Lewis et al.) | *It can look things up.* External memory becomes practical. |
| 2021 | **Scratchpads** (Nye et al.) | *It can show its work.* Hidden computation made visible — the seed of reasoning traces. |
| 2022 | **Chain-of-Thought** (Wei et al.) | *It thinks in steps.* |
| 2022 | **ReAct** (Yao et al.) | *It thinks and acts, interleaved* — the direct ancestor of every tool agent. |
| 2022 | **Adept ACT-1** | *It can drive a UI.* The browser-agent demo category is born. |
| Nov 2022 | **ChatGPT** | *Everyone talks to it.* ~100M users in two months. |
| Mar–Jun 2023 | **Plugins → function calling** | *It takes actions*, not just gives answers. |
| Mar–Apr 2023 | **AutoGPT / BabyAGI** | *It loops toward a goal* — and the whole internet watched it loop, burn money, and lose its state. |
| Apr 2023 | **Generative Agents** (Park et al.) | *It remembers and reflects.* Smallville looked like an autonomous society. |
| 2023 | **Reflexion / Self-Refine** | *It improves from its own feedback* — no weight updates needed. |
| 2023 | **Toolformer / HuggingGPT / ToolLLM** | *It orchestrates other tools and models.* |
| 2023 | **Tree of Thoughts / Voyager** | *It searches and accumulates skills.* |
| 2023 | **AutoGen / MetaGPT / CAMEL** | *Agents talk to each other.* Multi-agent becomes a framework category. |
| Nov 2023 | **GPTs + Assistants API** | *Anyone can ship an agent-ish app.* |
| Jan 2024 | **LangGraph** (stateful graph orchestration; durable execution followed later that year) | The field admits it: *agents need state, control flow, and human-in-the-loop.* |
| Mar 2024 | **Devin** | *"AI software engineer"* goes viral (and the backlash teaches the field about demo honesty). |
| May 2024 | **Project Astra** | *It sees and hears continuously.* |
| Sep–Oct 2024 | **o1-preview + Claude computer use** | *The scratchpad moves inside the model*; the model gets a mouse and keyboard. |
| Nov 2024 | **MCP** | *Tools standardize.* "USB-C for AI apps." |
| Dec 2024–Feb 2025 | **Deep Research** (Gemini, OpenAI) | *It works for 30 minutes and cites its sources.* |
| Jan 2025 | **Operator** | *It browses for you.* |
| Mar 2025 | **Manus** | *It works asynchronously on a cloud computer* — the "general agent" waitlist frenzy. |
| Mar–Jul 2025 | **Responses/Agents API → ChatGPT Agent** | *Agent-building becomes a platform primitive; consumer agents converge.* |
| 2025–26 | **Agentic coding (Cursor, Claude Code, Codex)** | *AI labor on real codebases becomes normal.* |
| 2026 | **Deep agents, subagent orchestration, local-first gateways** | *It delegates and scales* — fleets, not sessions. |

---

## The pattern

Read the table again as one sentence per era:

> **It talks → it thinks → it uses tools → it loops → it remembers → it controls software → it works async → it delegates.**

Every fragment went viral. And every fragment **failed the same way in production**: the AutoGPT wave looped and lied about being done; multi-agent frameworks clobbered each other's work; voice agents collapsed into "yeah, exactly…" acknowledgement loops; browser agents did things nobody could audit. The missing layer was never intelligence — it was **shared state, durable control, provenance, and the authority to say "done" or "stop."**

## Where my work sits

| The recurring failure | The field's viral example | What I shipped against it |
| --- | --- | --- |
| Thinks, but invisibly | scratchpads → o1 | **[NodeTrace](https://github.com/HomenShum/NodeTrace)** — cmd-click any UI surface, see the agent trace behind it |
| Loops, but lies about "done" | AutoGPT wave | **[NodeProof](https://github.com/HomenShum/NodeProof)** — a Stop-hook supervisor: the agent may claim, only the executable gate certifies |
| Remembers, then over-acts on it | Generative Agents | **[NodeMem](https://github.com/HomenShum/NodeMem)** — notice passively, act explicitly: a 6-gate suppression pipeline between detection and action |
| Judged by vibes | benchmark-chart drama | **[VisualJudge](https://github.com/HomenShum/VisualJudge)** + eval harnesses I built at Meta PQX — deterministic evidence first, model judgment second |
| Collaborates, but clobbers | multi-agent frameworks | **[NodeRoom](https://github.com/HomenShum/NodeRoom)** — lock → draft → smart-merge, per-element CAS: humans and agents edit the same sheet, nobody's work is silently overwritten |
| Talks together, loops forever | voice-agent demos | **[NodeVoice](https://github.com/HomenShum/NodeVoice)** — a server-authoritative room (floor control, deterministic reducer) with live side-by-side proof and on-screen model provenance |
| Acts, but unaudited | Operator/Manus era | Receipts everywhere: versioned edits, source-backed claims, provenance badges, replayable traces — across all of the above |

The lineage in one line: **[NodeBenchAI](https://github.com/HomenShum/NodeBenchAI)** (research engine) → **[NodeAgent](https://github.com/HomenShum/NodeAgent)** (agent kernel) → **[NodeRoom](https://github.com/HomenShum/NodeRoom)** (humans + agents in one governed room) → **NodeVoice + NodeProof** (coordination and completion authority).

## Where this goes — 2027, 2028

The task horizon agents can complete autonomously has been doubling roughly every seven months, measured across 2019–2025 ([METR](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/)). Follow it, and **2027 is the year AI labor becomes schedulable** — fleets of agents doing real work in parallel ([ai-2027.com](https://ai-2027.com/) is the sharpest scenario writing on this). Then **2028 is the control moment**: the questions stop being "how smart" and become *who owns the state, who audits the decisions, who holds the floor, who can pause the fleet.*

Chat windows don't answer those questions. **Rooms do** — shared authoritative state, floor control, provenance on every edit, human override on the critical path. That's the layer I've been building all along, one viral failure at a time.

> The agent should leave receipts. High-trust work doesn't get faster by trusting the model more — it gets faster by making the model *checkable*.

---

<sub>Primary sources: [ELIZA](https://dl.acm.org/doi/10.1145/365153.365168) · [SHRDLU](https://hci.stanford.edu/winograd/shrdlu/) · [RAG](https://arxiv.org/abs/2005.11401) · [Scratchpads](https://arxiv.org/abs/2112.00114) · [CoT](https://arxiv.org/abs/2201.11903) · [ReAct](https://arxiv.org/abs/2210.03629) · [Generative Agents](https://arxiv.org/abs/2304.03442) · [Reflexion](https://arxiv.org/abs/2303.11366) · [Tree of Thoughts](https://arxiv.org/abs/2305.10601) · [Voyager](https://arxiv.org/abs/2305.16291) · [Toolformer](https://arxiv.org/abs/2302.04761) · [computer use](https://www.anthropic.com/news/3-5-models-and-computer-use) · [MCP](https://www.anthropic.com/news/model-context-protocol) · [Operator](https://openai.com/index/introducing-operator/) · [METR long-task horizon](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/) · [AI-2027](https://ai-2027.com/)</sub>
