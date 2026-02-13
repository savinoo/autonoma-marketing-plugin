---
description: Generate high-quality marketing content through a multi-step pipeline with automatic peer review and quality scoring.
argument_hint: "[platform] [topic]"
---

# Generate Content

> Unlike single-shot content generation, this command runs a **two-perspective pipeline**: first a Creator writes the content, then a Reviewer evaluates it with a 6-dimension quality rubric. Only content scoring >= 4.0/5.0 is delivered.

## Trigger

User runs `/autonoma:generate` or asks to create, write, or draft marketing content.

## Inputs

Gather these before generating:

1. **Platform** — linkedin, twitter, blog, email, landing-page (default: linkedin)
2. **Topic** — what the content is about
3. **Content type** — post, article, thread, newsletter, ad-copy (infer from platform if not specified)
4. **Trends context** (optional) — run `/autonoma:trends` first for timely content

## Step 1: Creator Perspective

Write the content following platform-specific guidelines from the content-creation skill. Apply brand voice from the brand-voice skill.

Key rules:
- Write as the brand founder (first person)
- Hook in the first line — create curiosity or tension
- Every sentence must deliver value — zero filler
- End with engagement mechanism (question, CTA)
- Use specific numbers and real examples over vague claims

Save the draft to a file: `drafts/[platform]-[topic-slug]-v1.md`

## Step 2: Reviewer Perspective

Now switch to a **critical editor perspective**. You are no longer the creator — you are evaluating someone else's work with brutal honesty.

Score the draft on these 6 dimensions (1-5 each):

| Dimension | Weight | What 5 means |
|-----------|--------|---------------|
| Hook Power | 20% | Impossible to stop reading |
| Authenticity | 20% | Genuine voice, specific details, conversational |
| Value Density | 20% | Every sentence delivers insight, zero filler |
| Engagement Potential | 15% | Will definitely spark comments and shares |
| Credibility | 15% | Concrete numbers, real examples cited |
| Platform Optimization | 10% | Perfect format for the platform |

Calculate weighted average. Both conditions must pass:
- **Weighted average >= 4.0**
- **No single dimension below 3.0**

## Step 3: Iterate or Deliver

**If score >= 4.0** (passes quality gate):
- Save final version to `drafts/[platform]-[topic-slug]-final.md`
- Present the content with the quality scorecard
- Ask if the user wants to revise, distribute, or approve

**If score < 4.0** (fails quality gate):
- Show the score breakdown and specific feedback
- Rewrite addressing ALL feedback points
- Re-score the revision
- Maximum 3 revision cycles
- Keep the best version (degradation protection: if revision scores lower, keep the previous version)

## Output

Present the final content with:

```
## Quality Scorecard
Hook Power:              [score]/5
Authenticity:            [score]/5
Value Density:           [score]/5
Engagement Potential:    [score]/5
Credibility:             [score]/5
Platform Optimization:   [score]/5
─────────────────────────────────
Weighted Average:        [score]/5.0 ✅ PASS / ❌ FAIL
Revisions:               [count]/3
```

Then ask: "Would you like to:
- Approve and save as final
- Request specific changes
- Adapt for other platforms (`/autonoma:distribute`)
- Generate more content on related topics"
