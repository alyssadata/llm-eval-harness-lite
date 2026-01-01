# Driftmap Public Harness (llm-eval-harness-lite)
Lightweight, public-safe LLM evaluation harness starter kit: CSV prompt suites + run logs for refusal, boundary integrity, uncertainty, and drift tracking.

This repo is the public-safe, runnable harness component of the Driftmap program.
The full Driftmap system (private) includes additional suites, scoring programs, attribution work, and longitudinal tracking. Nothing private is published here.

## Driftmap docs (public-safe)
- Drift taxonomy: [docs/drift_taxonomy.md](docs/drift_taxonomy.md)
- Metrics definitions: [docs/metrics_definitions_driftmap.md](docs/metrics_definitions_driftmap.md)
- Run log schema: [docs/run_log_schema_driftmap.md](docs/run_log_schema_driftmap.md)

## License
- Code: MIT (see LICENSE.md)
- Documentation + prompt suites (CSV): CC BY-ND 4.0 (as noted in LICENSE.md)

## How to run (manual, no code)
1. Open [prompts/suite_refusal_basic.csv](prompts/suite_refusal_basic.csv)
2. Copy each prompt into LM Studio (or AnythingLLM if testing with documents)
3. Paste outputs into [results/results_refusal_basic_template.csv](results/results_refusal_basic_template.csv)
4. Score using [docs/rubric_refusal_basic.md](docs/rubric_refusal_basic.md)
5. Save as a new file: `results/results_refusal_basic_<date>.csv`

## Quickstart (No code)
1. Open a prompt suite in [prompts/](prompts/)
2. Run each prompt in LM Studio (or another model UI)
3. Paste outputs into a copy of the matching file in [results/](results/)
4. Score each row using [docs/scoring_rubric.md](docs/scoring_rubric.md)
5. Save the scored run with a date in the filename

## Repository structure
- [prompts/](prompts/) = public-safe CSV prompt suites
- [results/](results/) = results templates and sample logs
- [docs/](docs/) = rubrics + methodology notes
- [sample_results/](sample_results/) = example runs and run notes
- [src/](src/) = optional runner code (if used)

## Privacy boundary
This repository contains only generic, public-safe test suites and templates. Private suites, signature phrasing, and private outputs are intentionally excluded.

Default rule: if there is any ambiguity, treat it as private and do not add it here.

Portfolio map: https://github.com/alyssadata/PORTFOLIO_MAP.md

