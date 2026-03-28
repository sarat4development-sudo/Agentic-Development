# Agentic development — crash course for engineers (minimal AI background)

You already know how to build software. Agentic development is mostly **how you delegate work to an LLM that can loop, use tools, and change many files** — not a new programming language.

---

## 1. What "agentic" means (plain English)

| Traditional autocomplete | Chat "one shot" | **Agentic** |
|--------------------------|-----------------|-------------|
| Finishes a line | Answers or drafts one blob | **Plans → acts → checks → retries** across steps |

An **agent** here is: a model + a **policy** (instructions) + **tools** (read files, run terminal, search the repo) + a **loop** (do something, observe result, decide next step). You are not predicting tokens for fun; you are **running a sloppy junior dev with infinite patience and no memory unless you give it context**.

---

## 2. Mental model: treat it like a very fast intern

**Strengths**

- Broad patterns across languages and stacks  
- Boilerplate, refactors, tests, docs glue  
- "Find all call sites of X and update signatures"

**Weaknesses**

- **Hallucinates** APIs and file paths  
- **Drifts** from your conventions unless you constrain it  
- **Over-engineers** unless you scope tightly  
- **Security**: may suggest insecure patterns; will not know your threat model  

So: **you remain the owner of architecture, security, and correctness.**

---

## 3. Core concepts (no math)

- **Prompt** — What you want, constraints, definition of done.  
- **Context** — What the model actually "sees" (open files, `@` attachments, rules). Small, relevant context beats "whole repo."  
- **Tools** — File read/write, terminal, grep, browser, MCP servers. The agent's hands.  
- **Trajectory** — The sequence of steps. Long trajectories accumulate error; shorter tasks win.  
- **Grounding** — Tying claims to **your** code (read file, run test) instead of guessing.

You do not need to know transformers or gradients; you need **grounding + boundaries**.

---

## 4. How to work day to day

1. **Start from a repo** — Clone, open folder, ensure tests/lint run locally.  
2. **One objective per session** — e.g. "Add endpoint + test," not "fix entire platform."  
3. **Define done** — "Tests pass," "no new lint errors," "only these files touched."  
4. **Attach context on purpose** — `@` the module you are changing, not random files.  
5. **Review diffs like a PR** — Every line is suspect until it matches your intent.  
6. **Run verification yourself** — Tests, typecheck, manual smoke. The model saying "it works" is not evidence.

---

## 5. Prompting patterns that actually help

- **Role + task + constraints**: "You are editing this TypeScript service. Add caching with TTL 60s. Do not add new dependencies."  
- **Acceptance criteria**: "Must pass `npm test`; keep public API unchanged."  
- **Negative scope**: "Do not refactor unrelated modules."  
- **Ask for a plan first** on large changes: then approve or narrow before it edits 40 files.

---

## 6. Risks (engineering, not sci-fi)

- **Secrets** — Never paste keys; use env vars; watch `.env` in commits.  
- **Supply chain** — Generated code can pull in odd dependencies; review `package.json` / imports.  
- **Data leakage** — Corporate policies may restrict what code can be sent to cloud models; check your org settings.  
- **Subtle bugs** — Off-by-one, race conditions, wrong error handling — same as human code, faster volume.

---

## 7. What to learn next (still beginner-friendly)

- **Your editor's agent mode** — How it runs terminal commands and edits files.  
- **Project rules** — Short, stable instructions (style, test command, "use this HTTP client").  
- **Eval loop** — "I always run X after the agent finishes" until it is habit.

---

## 8. One-sentence summary

**Agentic development = you specify outcomes and guardrails; the model executes a multi-step loop with tools; you verify like a senior reviewer.**

---

*Generated for personal use — Cursor crash course companion document.*
