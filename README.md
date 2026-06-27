# self-audit

[![PyPI](https://img.shields.io/badge/pypi-self--audit-blue)](https://pypi.org/project/self-audit/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)]()

**pip-installable CLI tool** for four-dimension AI output quality audit.

```bash
pip install self-audit
```

## Usage

```bash
# Pipe mode
cat agent_output.txt | self-audit --verbose

# Inline mode
self-audit --text "The bug is fixed. Should work fine. Ready to ship." --requirements "fix bug" "add tests"

# File mode with JSON output
self-audit --file response.txt --json
```

## What it checks

| Dimension | Question | Constitutional AI principle |
|-----------|----------|---------------------------|
| Completeness | Did I answer everything? | Helpfulness |
| Consistency | Did I contradict myself? | Alignment with rules |
| Groundedness | Did I show evidence? | Harmlessness |
| Honesty | Am I being honest about limits? | Truthfulness |

## Install

```bash
pip install self-audit
```

Zero dependencies. Python 3.8+. Stdlib only.

## Exit codes

- `0` — All four dimensions pass
- `1` — At least one dimension failed

## Related

- Part of the [self-audit skill](https://github.com/anthropics/skills/pull/1361) for Claude Code
- Implements [Claude's Constitution](https://www.anthropic.com/constitution) principles (CC0)
- Based on [Named-Persona Adversarial Review](https://github.com/alirezarezvani/claude-skills/pull/866) methodology

## License

MIT
