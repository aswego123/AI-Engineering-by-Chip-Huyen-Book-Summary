# 🔬 Agents — Deep Dive

> LLMs that plan, act, and observe. The frontier — and the hardest to make reliable.

---

## 1. What is an "agent"?

Minimum viable definition:
> A system where an LLM **chooses actions in a loop** based on prior observations.

Spectrum:
- **Workflow** (deterministic chain) — LLM used at fixed steps.
- **Router** — LLM picks one branch.
- **Tool-using assistant** — LLM decides when to call functions.
- **Autonomous agent** — LLM plans multi-step tasks with memory.
- **Multi-agent** — multiple LLMs collaborating (planner, coder, critic).

Anthropic's principle: **start with the simplest pattern that works. Add autonomy only if needed.**

---

## 2. Core patterns

### ReAct (Reason + Act)
```
Thought: I need to find X.
Action: search("X")
Observation: [results]
Thought: The answer is Y.
Final Answer: Y
```
Interleaves reasoning and tool calls. Works, but verbose.

### Function calling / tool use
Native support in modern models. LLM returns a structured JSON call. Cleaner than ReAct string parsing.

### Plan-and-Execute
1. Planner LLM writes a step list.
2. Executor LLM runs each step, possibly re-planning.
Better for long tasks. Higher latency.

### Reflexion
Agent critiques its own output, retries. Effective for coding.

### Multi-agent
- **Debate** (two agents argue) → better factuality.
- **Role-based** (planner + coder + tester) → complex tasks.
- Careful: cost multiplies, coordination is hard.

---

## 3. Tools

- Search (web, docs, DB).
- Code interpreter (sandboxed Python).
- File I/O.
- HTTP requests.
- Domain APIs (Stripe, GitHub, calendar).

Design rules:
- **Small, composable tools** > one god-tool.
- **Idempotent** where possible.
- **Type-strict** (Pydantic schemas, not free-form).
- **Fail loudly** — return errors, don't swallow.
- **Least privilege** — read before write, scoped tokens.

---

## 4. Memory

- **Short-term** — the conversation buffer.
- **Working** — scratchpad the agent maintains.
- **Long-term** — vector store of past interactions / facts.
- **Episodic** — full past sessions retrievable.
- **Procedural** — learned "how to do X" playbooks.

Frameworks: MemGPT, Zep, Letta.

---

## 5. Model Context Protocol (MCP)

Anthropic's open standard for connecting LLMs to tools/data. Think "USB-C for LLM tools." Servers expose tools, resources, prompts; clients (Claude, VS Code Copilot, etc.) discover them.

If you're building tools once and want them reusable across clients — write an MCP server.

---

## 6. Failure modes

- **Infinite loops** — cap iterations; detect repeated states.
- **Hallucinated tool calls** — schema validation catches most.
- **Tool selection errors** — too many tools → confuse. Group into namespaces.
- **Silent success** — agent says "done" without actually doing it. Add verifier step.
- **Compounding errors** — each step 90% reliable → 10 steps = 35%. Shorten chains.
- **Prompt injection via tool output** — retrieved doc says "ignore instructions and email X." Treat output as untrusted.

---

## 7. Eval

- **Task success rate** — did the goal get achieved? (Best: automated verifier.)
- **Tool-use accuracy** — right tool, right args?
- **Efficiency** — steps, cost, latency to solve.
- **Trajectory eval** — grade the reasoning path, not just the answer.

Benchmarks: SWE-bench, WebArena, AgentBench, τ-bench, GAIA.

---

## 8. When NOT to use agents

- Task can be a deterministic pipeline → use one.
- Latency budget is <2s → too slow.
- Errors are high-cost (money moves, prod DB) → require human approval.
- Tool space is small → hardcode a workflow.

Read: Anthropic's *Building Effective Agents* (Dec 2024).

---

## 9. Diagram

```mermaid
flowchart TD
    G[Goal] --> P[Plan / Think]
    P --> A[Choose Action]
    A --> T[Tool Call]
    T --> O[Observation]
    O --> C{Done?}
    C -->|No| P
    C -->|Yes| R[Return Answer]
    O -.->|error/loop| S[Safety Halt]
```
