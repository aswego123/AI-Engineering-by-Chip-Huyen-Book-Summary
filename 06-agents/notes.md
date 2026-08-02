# 🤖 Agents

> AI that can **perceive**, **decide**, **act**, and **learn** — not just respond.

## What Is an Agent?

Anything that can:
1. **Observe** its environment
2. **Decide** based on observations
3. **Take actions** that affect the environment
4. **Learn** from outcomes

## Categories of Tools

### Knowledge Augmentation
- Text/image retrievers (RAG)
- SQL executors
- Web search
- APIs (inventory, email)
- Web browsers

### Capability Extension
- Calculators (LLMs are bad at math)
- Time zone/unit converters
- Translation services
- Code interpreters

### Write Actions
- Send emails, place orders, transfer money
- ⚠️ **HIGH RISK** — needs strong safeguards

## Planning

Complex tasks need decomposition. **Decouple planning from execution**:

1. Generate a plan
2. Validate the plan (heuristics or AI judge)
3. Execute only after validation

### Planning Tips

- Generate plans in **natural language first**, then translate to function calls
- Always ask agent to **report parameter values** before execution
- Human-in-the-loop for sensitive tasks

## Failure Modes

### Planning Failures
- Uses invalid tools
- Wrong parameters
- Fails to achieve goal or satisfy constraints

### Tool Failures
- Bad translation from plan → function call
- No access to required tools
- Tools give incorrect outputs (bad SQL, etc.)

### Efficiency Metrics
- Steps needed per task
- Cost per task
- Time per action
- Comparison to baseline (another agent or human)

## Memory Systems

Three types (like human memory):

| Memory Type | Location | Use Case |
|-------------|----------|----------|
| **Internal knowledge** | Model weights (training) | Essential, universal facts |
| **Short-term** | Context window | Current session |
| **Long-term** | External (RAG) | Rarely-used, but important info |

Benefits: persists across sessions, exceeds context window, more consistent behavior.

## Warnings

- Errors **compound** across steps
- Write actions have **real-world stakes**
- Needs more capable models than simple chatbots

📖 [Back to book summary](../00-book-overview/summary.md)
