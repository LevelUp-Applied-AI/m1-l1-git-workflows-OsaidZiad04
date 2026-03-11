# AGENTS.md — OmniGuard (Cyber Threat Intelligence Platform) AI Governance

> This file defines the rules, constraints, and boundaries for AI agents working in the OmniGuard repository.
> Last updated: 2026-03-11

---

## Testing Requirements
All changes must pass `python test_environment.py` before committing. Any threat detection models or data processing code added to `src/` must have a corresponding test in `tests/` that passes with `pytest tests/ -v`.

## Secrets Policy
**STRICT NO-SECRETS POLICY**: Do not include threat feed API keys, database passwords, sensitive network logs, or raw malware samples in any prompt. Never commit `.env`, `*.key`, `*.pem`, or any file containing credentials or real vulnerability data.

## Scope Boundaries
Agents may edit files in `src/` and `notebooks/` for analyzing cyber threats and developing AI models. 
- Do not modify `requirements.txt` without human review (to prevent supply chain attacks). 
- Do not modify `setup.sh` without running and testing the result locally. 
- Do not touch `.gitignore` without confirming the change doesn't accidentally expose sensitive logs or data.

## Reproducibility Standard
All AI-assisted changes require local-first execution: the change must run locally and produce the expected output on sample threat data before it is committed or pushed. "The AI generated it" is not a substitute for running and verifying the code.