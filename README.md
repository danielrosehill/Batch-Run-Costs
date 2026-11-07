# Batch Run Costs

A running record of the batch inference jobs I do: what the job was, how much data, which model on which route,
what it cost, and how well it worked. It exists to answer "what did I use for that, and how did it go?"

Read [RUNS.md](RUNS.md). The data is [runs.jsonl](runs.jsonl), one JSON object per job.

| Field | Meaning |
|---|---|
| `date` | Day of the run, YYYY-MM-DD |
| `job` | What the job was, in one line |
| `task_type` | classification, extraction, generation, summarising, judging, ... |
| `items`, `data_size` | How many items, and what they were |
| `tokens_in`, `tokens_out` | Total tokens |
| `model`, `route` | Model id, and how it ran (`openrouter-sync`, `openrouter-batch`, `anthropic-batch`, `local`) |
| `cost_usd`, `cost_basis` | API cost in US$; `measured` from usage data or `estimated` |
| `rating` | 1-5 for how well the model did the task; empty if nobody checked |
| `notes`, `alternatives` | Anything worth remembering; other models considered |

Prices are as of the run date and move often.

Rows are added with the `log-batch-run` skill and searched with `find-batch-run`, both in the
[Batch-Inference](https://github.com/danielrosehill/Batch-Inference) plugin. `RUNS.md` is generated, so don't edit it by hand.
