---
description: Generate content through a two-perspective pipeline — Creator writes, Reviewer scores on 9 dimensions (craft + reader psychology).
argument-hint: "[platform] [topic]"
model: opus
---

# Generate Content

> Two-perspective pipeline: Creator writes, then Reviewer evaluates with a 9-dimension rubric covering craft quality AND reader emotional impact. Only content scoring >= 4.0/5.0 is delivered.

## Inputs

Gather these before generating (infer from arguments if provided):

1. **Platform** — linkedin, twitter, blog, email, landing-page (default: linkedin)
2. **Topic** — what the content is about
3. **Content type** — post, article, thread, newsletter, ad-copy (infer from platform if not specified)

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

Now switch to a **critical editor AND reader psychology perspective**. You are no longer the creator — you are evaluating someone else's work.

IMPORTANT: Be calibrated. Most content is a 3. A 4 means genuinely good. A 5 is rare.

### Part A: Craft Quality (6 dimensions)

| Dimension | Weight | What 5 means |
|-----------|--------|---------------|
| Hook Power | 15% | Impossible to stop reading |
| Authenticity | 15% | Genuine voice, specific details, conversational |
| Value Density | 15% | Every sentence delivers insight, zero filler |
| Credibility | 15% | Concrete numbers, real examples cited |
| Engagement Potential | 10% | Will definitely spark comments and shares |
| Platform Optimization | 5% | Perfect format for the platform |

### Part B: Reader Perspective (3 dimensions)

Put yourself in the reader's shoes. You are a busy professional scrolling your feed.

| Dimension | Weight | What 5 means |
|-----------|--------|---------------|
| Emotional Resonance | 10% | Reader feels something strong (surprise, recognition, urgency) |
| Perceived Intent | 10% | "This person genuinely wants to help me." Feels generous |
| Trust Signal | 5% | "I want to follow this person." Builds real authority |

### Sentiment Summary

Write 2-3 sentences: How does this content feel from the reader's perspective? What emotion does it trigger? What impression does it leave about the author?

### Quality Gate

Both conditions must pass:
- **Weighted average >= 4.0** (across all 9 dimensions)
- **No single dimension below 3.0**

## Step 3: Iterate or Deliver

**If score >= 4.0** (passes quality gate):
- Save final version to `drafts/[platform]-[topic-slug]-final.md`
- Present the content with the quality scorecard
- Ask if the user wants to revise, distribute, or approve

**If score < 4.0** (fails quality gate):
- Show the score breakdown, sentiment summary, and specific feedback
- Rewrite addressing ALL feedback points (especially low reader-perspective scores)
- Re-score the revision
- Maximum 3 revision cycles
- Keep the best version (degradation protection)

## Output

Present the final content with:

```
CRAFT QUALITY
Hook Power:              [score]/5
Authenticity:            [score]/5
Value Density:           [score]/5
Credibility:             [score]/5
Engagement Potential:    [score]/5
Platform Optimization:   [score]/5

READER PERSPECTIVE
Emotional Resonance:     [score]/5
Perceived Intent:        [score]/5
Trust Signal:            [score]/5
─────────────────────────────────
Weighted Average:        [score]/5.0 PASS/FAIL
Revisions:               [count]/3

Sentiment: [2-3 sentence summary of how the reader feels]
```

Then ask: "Would you like to:
- Approve and save as final
- Request specific changes
- Adapt for other platforms (`/autonoma-distribute`)
- Generate more content on related topics"
