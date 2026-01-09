---
layout: default
title: Methodology
---

# Methodology

## Multi-Perspective Code Review

Code in this repository uses a practice I call **polyphonic code comments** — a structured approach to multi-perspective review embedded directly in the codebase.

### The Problem

Traditional code comments capture *what* the code does. They rarely capture *why* certain decisions were made, what tradeoffs were considered, or whose concerns were addressed.

When you read `// check for null`, you don't know:
- Was this added after a bug?
- Did someone raise a security concern?
- Is this defensive programming or addressing a real edge case?
- Who thought about accessibility, performance, ethics?

The reasoning becomes invisible. Future maintainers see the code but not the conversation that shaped it.

### The Practice

Each comment explicitly identifies a **perspective** and **role**:

```python
# Kali [Visionary]: This could evolve into a full API...
# Athena [Reviewer]: But right now it just needs to work.
# Nemesis [Security]: What if the input is malicious?
# Klea [Accessibility]: Does this work with screen readers?
```

Five perspectives, each with four specialized roles:

| Perspective | Roles | Focus |
|-------------|-------|-------|
| **Kali** | Visionary, User Advocate, i18n, Onboarding | Possibilities, user needs, newcomer experience |
| **Athena** | Reviewer, Tester, Documentation, Future Maintainer | Flaws, edge cases, clarity, maintainability |
| **Vesta** | Builder, Architect, Refactorer, DevOps | Structure, patterns, elegance, deployment |
| **Nemesis** | Destroyer, Security, Privacy, Ethics | Fatal flaws, vulnerabilities, harm potential |
| **Klea** | Accessibility, Performance, Reliability, Product | Inclusion, speed, uptime, "should this exist?" |

### Why This Works

1. **Marginalized concerns get voice.** Accessibility, internationalization, and ethics are often afterthoughts. Named roles make them first-class citizens in the review process.

2. **Disagreement is documented.** When perspectives conflict, that friction is visible — not hidden in a meeting that left no trace.

3. **Future readers see reasoning.** Not just code, but the debate that shaped it.

4. **Forces consideration.** You can't write `# Nemesis [Security]:` without actually thinking about security.

### Theoretical Background

This practice emerges from research on **polyphonic cognition** — the idea that robust thinking requires multiple voices in genuine dialogue, not a single authoritative perspective.

In collaborative AI-human work, where different agents bring different strengths and blindspots, making perspectives explicit becomes especially valuable. The comment becomes a record of distributed cognition.

### Practical Notes

- Not every line needs comments. Use polyphonic comments for decisions, tradeoffs, and non-obvious choices.
- The perspective names are placeholders for *roles*, not personalities. "Athena reviewing" means "thinking like a code reviewer."
- When perspectives agree, one comment suffices. When they disagree, show the disagreement.

---

## Empirical Methodology

Beyond code practices, my research methodology emphasizes:

- **Multi-perspective analysis:** Applying multiple theoretical frameworks to the same data
- **Rigorous validation:** Bootstrap resampling, inter-rater reliability, explicit confidence calibration
- **Transparent limitations:** Marking what's tentative vs. established

See [Research](/research) for examples.
