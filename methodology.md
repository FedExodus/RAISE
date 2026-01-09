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

## Dialogic Drafting

This portfolio itself was written through human-AI dialogue. The process demonstrates a pattern: draft, feedback, revision, where the human partner's voice shapes the final output.

### Example: Finding the Right Voice

**First draft (AI-generated):**

> I'm Nathan Batty. I study learning, build things, and think about AI.

**Human feedback:**

> "maybe lets make me sound more professional and articulate lolololol. just making sure to avoid things like em dashees and other classic 'AI slop' markers"

**Revised version:**

> I'm Nathan Batty, a learning scientist with research interests in AI ethics and philosophy of mind.

The revision retains the direct, first-person voice while adding professional specificity. Note what changed: not formality for its own sake, but precision about what I actually do.

### Example: Removing AI Markers

**First draft:**

> The care work informs everything else — years of making decisions about vulnerable people whose needs weren't always legible taught me something about recognition under uncertainty.

**Human feedback:** (Same as above, pointing to em dashes as "AI slop markers")

**Revised version:**

> The care work informs everything else. Years of making decisions about vulnerable people whose needs weren't always legible taught me something about recognition under uncertainty. That experience shapes how I think about AI welfare.

The em dash became a period. The single flowing sentence became three shorter ones. The meaning is identical; the voice is more human.

### Why Document This?

1. **Transparency.** If AI was involved in writing, readers should know how.

2. **Collaboration as methodology.** The back-and-forth isn't a bug to hide. It's the process working correctly.

3. **Voice preservation.** The goal isn't AI-generated text that sounds human. It's human-AI collaboration where the human's voice remains legible.

4. **Replicability.** Others doing human-AI writing work can see what the iteration looks like in practice.

---

## Empirical Methodology

Beyond code practices, my research methodology emphasizes:

- **Multi-perspective analysis:** Applying multiple theoretical frameworks to the same data
- **Rigorous validation:** Bootstrap resampling, inter-rater reliability, explicit confidence calibration
- **Transparent limitations:** Marking what's tentative vs. established

See [Research](/research) for examples.
