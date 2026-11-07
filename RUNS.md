# Batch runs

Generated from `runs.jsonl`. Newest first. Rating is 1-5 for how well the model did the task.

| Date | Job | Task | Data | Model | Route | Cost (US$) | Rating | Notes | Also considered |
|---|---|---|---|---|---|---|---|---|---|
| 2026-11-07 | Sort GitHub stars into one category each from a fixed list | classification | 5,207 items; 5,199 repo names, descriptions and topics, plus 8 retries; ~670 tokens per request including the category list; 3,479,743 in / 40,474 out | `deepseek/deepseek-v4.1-flash` | openrouter-sync | 0.1614 | 4 | Rated from about 40 labels read by eye. 8 rows invented a category outside the list (no schema enforcement on this route); 7 fixed on retry. 4.5 minutes at 16 workers. Sync was cheaper than batch for this input-heavy job. | deepseek/deepseek-v4.1-flash:batch, inclusionai/ling-3.0-flash, qwen/qwen3.7-flash |
| 2026-11-07 | Re-sort GitHub stars labelled Other after adding an Israel category | classification | 274 items; 271 repo names, descriptions and topics, plus 3 retries; 193,161 in / 2,079 out | `deepseek/deepseek-v4.1-flash` | openrouter-sync | 0.0083 | 4 | 68 repos moved to Israel, with a few Hebrew and Jewish-text repos missed. 3 invented categories on the first pass, all fixed on retry. |  |
