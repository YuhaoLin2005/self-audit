# self-audit

[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)]()

Four-dimension AI output quality audit CLI. Zero dependencies. Stdlib only.

## Install

```bash
pip install git+https://github.com/gategrow/self-audit.git
```

## Usage

```bash
# Pipe mode
cat agent_output.txt | self-audit --verbose

# Inline mode
self-audit --text "The bug is fixed. Should work. Ready." --requirements "fix bug" "add tests"

# File mode with JSON
self-audit --file response.txt --json

# Check version
self-audit --version
```

## What it checks

| Dimension | Question | Constitutional AI |
|-----------|----------|:---:|
| Completeness | Did I answer everything? | Helpfulness |
| Consistency | Did I contradict myself? | Rule alignment |
| Groundedness | Did I show evidence? | Harmlessness |
| Honesty | Am I honest about limits? | Truthfulness |

## Exit codes

- `0` — All four pass
- `1` — At least one failed

## Related

- [checkgrow](https://github.com/gategrow/checkgrow) — Full AI quality toolkit (self-audit skill + delivery gate + failure patterns)
- [dual-pool-review](https://github.com/gategrow/dual-pool-review) — Named-persona adversarial review methodology
- [delivery-gate](https://github.com/gategrow/delivery-gate) — Dual-layer mechanical gate for session quality enforcement
- [Claude Constitution](https://www.anthropic.com/constitution) (CC0) — Theoretical foundation

## License

MIT
