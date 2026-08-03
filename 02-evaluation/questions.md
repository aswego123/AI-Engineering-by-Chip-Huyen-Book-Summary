# ❓ Evaluation — Open Questions

## Conceptual
- [ ] How reliable is LLM-as-judge vs human labels on my task?
- [ ] What's the smallest sample size to detect a 5% quality difference?
- [ ] Should I use pointwise or pairwise scoring?

## Practical
- [ ] What does my "golden set" look like? How was it built? Is it leaked?
- [ ] How do I detect prompt regressions before shipping?
- [ ] Can I automate a nightly eval run against last week's baseline?

## Deeper
- [ ] Read *Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena* (Zheng 2023).
- [ ] Look at RAGAS internals — what does "faithfulness" actually compute?
- [ ] Reproduce a public leaderboard result and see how noisy it is.
