<h2 align="center">Homen Shum</h2>

<h3 align="center">An agent's claim that it finished is worthless unless the proof could have failed.</h3>

<p align="center">
I build the evidence layer that makes agent work checkable.<br>
<a href="https://github.com/HomenShum/proof-driven-development"><b>Proof-Driven Development</b></a> &mdash; the method, in one page. No framework. No install.
</p>

---

### The method

**[Proof-Driven Development](https://github.com/HomenShum/proof-driven-development)** rests on three rules:

1. **Default FAIL.** Every criterion starts `false`. The agent cannot mark it passing without opening the evidence first.
2. **The proof must be able to fail.** If the behavior broke tomorrow, would this check turn red? If not, it is decoration.
3. **The judge never built it.** The grader gets a fresh context and no write tools.

Rule 2 is the one most systems skip. It is also the one that finds fake evidence.

### Where the method came from

| Context | What I built | Result |
| --- | --- | --- |
| Meta Product Quality &amp; Experience (embedded via Tests Assured) | Planted-bug evaluation for an agentic QA platform | **1.00 precision, 0.80 recall, 0.89 F1**; rerun cost **&minus;98%** |
| JPMorgan Commercial Banking | Agentic-RAG diligence over 100,000+ documents, human review preserved | Prospecting **4 hr to 15&ndash;30 min**; a 2,000-company analysis **3 weeks to under 15 min** |
| AWS DeepRacer, JPMorgan Palo Alto team | Reward-function and race-line optimization | Lap time **23.260 s to 18.121 s** (theoretical line optimum: 19.673 s) |

Rule 2 is not theory. Planted bugs are how I learned that a passing check often proves nothing.

### The system, in layers

| Layer | Repo |
| --- | --- |
| **Doctrine** | [proof-driven-development](https://github.com/HomenShum/proof-driven-development) |
| **Reference implementation** | [NodeProof](https://github.com/HomenShum/NodeProof) &mdash; executable proof gates that block unsupported completion claims |
| **Components** | [NodeRL](https://github.com/HomenShum/NodeRL) (task evaluation) &middot; [NodeTrace](https://github.com/HomenShum/NodeTrace) (surface to span) &middot; [NodeMem](https://github.com/HomenShum/NodeMem) (memory gates) &middot; [agentic-ui-qa](https://github.com/HomenShum/agentic-ui-qa) (artifact-only completion) &middot; [AgentRedteam](https://github.com/HomenShum/AgentRedteam) |
| **Applications** | [NodeRoom](https://github.com/HomenShum/NodeRoom) (live human-agent workspace) &middot; [NodeBenchAI](https://github.com/HomenShum/NodeBenchAI) (entity intelligence) |

One idea. The rest are parts of it.

### Background

3.5 years inside JPMorgan commercial banking: credit underwriting, covenant analysis, and startup banking. 72 credit transactions, roughly $800M in aggregate exposure, 270 financial models. Then I became the engineer who builds the AI that automates that work.

Strongest where regulated, document-heavy workflows need agents somebody can actually check.

### Contact

[LinkedIn](https://linkedin.com/in/homen-shum) &middot; [nodebenchai.com](https://nodebenchai.com) &middot; hshum2018@gmail.com

---

<sub><b>Feedback wanted.</b> Rule 2 does not scale by hand. Breaking each behavior on purpose is cheap for three checks and expensive for three hundred. If you have solved this for agent workflows, I want to hear how.</sub>
