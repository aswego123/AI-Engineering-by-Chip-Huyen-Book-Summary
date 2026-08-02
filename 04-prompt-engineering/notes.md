# 💬 Prompt Engineering

> Crafting instructions that guide the model to produce your desired output. The **easiest** and **cheapest** adaptation technique.

## Prompt Components

1. **Task description** — role + expected output format
2. **Examples** — few-shot samples showing what to do
3. **Concrete task** — the specific query

## System vs. User Prompts

- **System prompt** — task, role, constraints (set by app developer)
- **User prompt** — the actual query (from end user)
- Follow the model's exact chat template — even an extra newline can break things

## Key Strategies

### ✅ Write Clear Instructions
Be explicit about scoring systems, edge cases, ambiguity.

### ✅ Assign a Persona
"Respond as an experienced pediatrician" — changes tone and focus.

### ✅ Provide Examples (Few-Shot)
Dramatically shifts response style.

### ✅ Specify Output Format
Request JSON, markdown, no preamble, specific headings.

### ✅ Break Complex Tasks into Subtasks
Improves quality, makes debugging easier.

### ✅ Give the Model Time to Think
- **Chain of Thought** — "think step by step"
- **Process instructions** — "first X, then Y"
- **Self-critique** — "check your work"

### ✅ Iterate Systematically
- Version your prompts
- Store prompts in config files (not hardcoded)
- Track experiments with metrics

## In-Context Learning

- **Zero-shot** — no examples
- **One-shot** — one example
- **Few-shot** — multiple examples

## Prompt Placement Tips

- Instructions at **beginning or end** work best (not middle)
- GPT-4 prefers task description at the start
- Llama 3 prefers task at the end

## Security: Prompt Attacks

1. **Prompt extraction** — attacker tries to steal your system prompt
2. **Jailbreaking / prompt injection** — bypass safety features
3. **Information extraction** — leak training data or context

### Defenses

- Repeat system prompt before AND after user input
- Explicit boundaries about what NOT to reveal
- Run generated code in isolated environments
- Human approval for impactful actions
- Input & output guardrails
- Track **violation rate** vs. **false refusal rate**

## Automation Tools

- **OpenPrompt**, **DSPy** — automate prompt optimization
- Warning: expensive (many API calls), may produce buggy prompts
- Start manual, then automate

📖 [Back to book summary](../00-book-overview/summary.md)
