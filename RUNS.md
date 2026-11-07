# Batch runs

Generated from `runs.jsonl`. Newest first. Rating is 1-5 for how well the model did the task.

| Date | Job | Task | Data | Model | Route | Cost (US$) | Rating | Notes | Also considered |
|---|---|---|---|---|---|---|---|---|---|
| 2026-11-07 | Sort GitHub stars into one category each from a fixed list | classification | 5,207 items; 5,199 repo names, descriptions and topics, plus 8 retries; ~670 tokens per request including the category list; 3,479,743 in / 40,474 out | `deepseek/deepseek-v4.1-flash` | openrouter-sync | 0.1614 | 4 | Rated from about 40 labels read by eye. 8 rows invented a category outside the list (no schema enforcement on this route); 7 fixed on retry. 4.5 minutes at 16 workers. Sync was cheaper than batch for this input-heavy job. | deepseek/deepseek-v4.1-flash:batch, inclusionai/ling-3.0-flash, qwen/qwen3.7-flash |
