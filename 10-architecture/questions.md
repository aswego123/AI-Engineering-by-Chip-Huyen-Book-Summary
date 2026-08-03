# ❓ Architecture — Open Questions

## Conceptual
- [ ] Which of the 9 capabilities does my system have? Which are stubs?
- [ ] Where's the untrusted-input boundary in my LLM pipeline?
- [ ] What breaks first at 10× traffic?

## Practical
- [ ] Do I log full trace (prompt + context + tools + response + cost)?
- [ ] Can I roll back a prompt in <5 minutes?
- [ ] Do I have a kill switch to fall back to a canned response?
- [ ] What's my p95 end-to-end latency budget?

## Deeper
- [ ] Read Eugene Yan's *Patterns for LLM Systems*.
- [ ] Read Hamel Husain's *Evals* series.
- [ ] Set up Langfuse or Phoenix locally, instrument one flow.
- [ ] Do a red-team session against your own app.
