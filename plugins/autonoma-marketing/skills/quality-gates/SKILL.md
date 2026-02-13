---
name: quality-gates
description: "Autonoma's quality assurance system: 6-dimension scoring rubric, peer-review process, threshold enforcement, and degradation protection. Use whenever evaluating, scoring, or improving content quality. This is what makes Autonoma different from every other marketing tool."
---

# Quality Gates — Peer Review System

The core differentiator of the Autonoma marketing pipeline. Every piece of content goes through a structured quality gate before delivery.

## Philosophy

Most AI content tools generate and deliver. Autonoma generates, **then reviews from a different perspective**, then delivers only what passes quality thresholds. This mirrors how real marketing teams work: a copywriter writes, an editor reviews.

The key insight: **the same AI can produce much better content when it systematically critiques its own work from a different perspective** (Creator vs Reviewer).

## The 6-Dimension Quality Rubric

### Dimensions and Weights

| # | Dimension | Weight | Why It Matters |
|---|-----------|--------|----------------|
| 1 | Hook Power | 20% | If nobody reads past line 1, nothing else matters |
| 2 | Authenticity | 20% | AI-generated slop is instantly recognizable and ignored |
| 3 | Value Density | 20% | Every sentence must earn its place |
| 4 | Engagement Potential | 15% | Content that doesn't spark interaction is wasted |
| 5 | Credibility | 15% | Claims without evidence damage trust |
| 6 | Platform Optimization | 10% | Wrong format = algorithmic burial |

### Scoring Scale (per dimension)

- **5** = Exceptional. Top 5% of content on this platform.
- **4** = Strong. Would perform well against human-written content.
- **3** = Adequate. Acceptable but not remarkable.
- **2** = Below average. Needs significant improvement.
- **1** = Failing. Must be rewritten entirely.

### Quality Threshold

Two conditions must BOTH be met:

```
weighted_average >= 4.0  (overall quality bar)
min(all_dimensions) >= 3.0  (no catastrophic weakness)
```

Content that scores 4.5 average but has a 2.0 on authenticity FAILS — because one weak dimension undermines the whole piece.

## Peer Review Process

### Step 1: Creator writes
Full creative freedom, following brand voice and platform guidelines.

### Step 2: Reviewer evaluates
Switch to a **completely different perspective**. The Reviewer:
- Is a senior content editor, not the creator
- Evaluates with brutal honesty
- Provides specific, actionable feedback (not vague suggestions)
- Scores each dimension independently

### Step 3: Iterate or deliver
- **PASS** (>= 4.0, no dimension < 3.0): Deliver to user
- **FAIL** (< 4.0 or any dimension < 3.0): Revise with specific feedback

### Step 4: Degradation protection
- Maximum 3 revision cycles
- If a revision scores LOWER than the previous version, keep the previous (best) version
- After 3 cycles, deliver the best version with honest score disclosure

## When to Apply Quality Gates

| Scenario | Apply? | Threshold |
|----------|--------|-----------|
| `/autonoma:generate` (new content) | Yes | >= 4.0 |
| `/autonoma:review` (existing content) | Score only | N/A (informational) |
| `/autonoma:distribute` (adaptations) | Yes | >= 3.5 (lower for adaptations) |
| Quick edits or tweaks | No | N/A |

## Feedback Quality Standards

Bad feedback: "Make it more engaging"
Good feedback: "Add a specific metric in paragraph 2. Replace the generic closing with a provocative question about whether AI agents will replace marketing teams within 2 years."

Feedback must be:
- **Specific**: Point to exact sentences or paragraphs
- **Actionable**: Describe what to do, not just what's wrong
- **Prioritized**: Focus on the lowest-scoring dimensions first
- **Example-driven**: Show a before/after when possible
