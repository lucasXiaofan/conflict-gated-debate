# Conflict-Gated Debate for RAG

Folders:
- `madam_rag/` — MADAM-RAG code and **RAMDocs**, the benchmark built around conflicting information (ambiguity, misinformation, noise). Original: https://github.com/HanNight/RAMDocs
- `trivia_qa/` — the TriviaQA repo (evaluation code only; download the data from the [TriviaQA site](http://nlp.cs.washington.edu/triviaqa/)). Original: https://github.com/mandarjoshi90/triviaqa

## Benchmarks
Evaluate each RAG method on **both** benchmarks and report **accuracy** and **token usage**.

- **RAMDocs** (primary): 500 queries, 1–3 valid answers each, 5.53 documents on average. It combines ambiguity, misinformation, noise and imbalanced evidence, so it shows when debate helps.
- **TriviaQA** (500-query subset, public DPR-retrieved passages): each query has gold answers and ranked passages, some answer-bearing and some distractors. It is *not* built to contain conflicts, so it measures how often a router invokes debate unnecessarily on ordinary single-hop RAG queries.

## Model
Suggested: `meta-llama/llama-3.3-70b-instruct` (the model used in the MADAM-RAG paper), called through OpenRouter.
