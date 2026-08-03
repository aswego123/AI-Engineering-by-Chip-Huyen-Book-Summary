# ❓ Fine-Tuning — Open Questions

## Conceptual
- [ ] Why does LoRA work? (Low intrinsic rank of task adaptation.)
- [ ] When does DPO beat RLHF? When does it not?
- [ ] Is catastrophic forgetting always bad?

## Practical
- [ ] Have I exhausted prompting + RAG before tuning?
- [ ] Is my dataset deduplicated and de-leaked?
- [ ] What's my base model choice and why?
- [ ] What's my rollback plan if the tuned model regresses?

## Deeper
- [ ] Read *LoRA* (Hu 2021) and *QLoRA* (Dettmers 2023).
- [ ] Read *DPO* (Rafailov 2023).
- [ ] Read *LIMA: Less Is More for Alignment*.
- [ ] Actually run `unsloth` on a 7B model.
