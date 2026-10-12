---
name: paper-to-code
description: Turn an academic paper into running code — extracts the core algorithm, maps equations to implementation, and delivers tested code with paper↔code traceability. Use when the user shares a paper (arXiv link, PDF, or text) and wants an implementation.
---

# Paper to Code 📄

Paper in, running code out — with every line traceable to the paper.

## Workflow

1. **Read the paper.** Get it from the arXiv link, PDF, or pasted text. Focus on: abstract, method section, key equations, algorithm pseudocode, hyperparameters, evaluation setup. If you can't access the full text, say so and work from what's available.

2. **Extract the blueprint.** Before coding, write down:
   - Core algorithm in 3-5 bullet steps
   - Inputs → outputs with shapes/types
   - Key equations numbered as in the paper (e.g. "Eq. 3, §3.2")
   - Hyperparameters and their reported values
   - What the paper evaluates and how

3. **Implement faithfully.** Write clean, runnable code where:
   - Structure mirrors the paper's structure (same section order where sensible)
   - Every non-trivial block has a comment citing its source: `# Eq. 3 (§3.2) — attention weights`
   - A runnable example/demo is included (synthetic data is fine)
   - A README maps code files ↔ paper sections

4. **Be honest about gaps.** End with a fidelity note:
   - ✅ Faithful: …
   - ⚠️ Simplified: … (and why — e.g. "training loop replaced with inference-only demo")
   - ❓ Unclear in paper: … (ambiguities you had to resolve, and your choice)

## Rules

- Never hallucinate results or claim the implementation reproduces the paper's numbers unless you actually ran the evaluation.
- Prefer clarity over cleverness — this code is for learning, mirror the math.
- If the paper has official code, mention it and explain how yours differs (e.g. "minimal single-file version").
- Keep dependencies light (numpy/PyTorch-level, not exotic).
