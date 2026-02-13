---
description: Deep content review — craft quality + reader psychology. 9 dimensions including sentiment analysis and perceived intent.
argument-hint: "[file or paste content]"
model: opus
---

# Review Content

> Evaluate content from TWO perspectives: craft quality AND reader emotional impact. Be the harshest critic in the room.

## Inputs

1. **Content to review** — pasted directly, or a file path
2. **Platform context** — which platform is this for?
3. **Brand guidelines** — use the brand-voice skill automatically

## Review Process

You evaluate from two different lenses. First as a **senior content editor** (is it well-written?), then as the **target reader** (how does it make me feel?).

IMPORTANT: Be calibrated. Most content is a 3. A 4 means genuinely good. A 5 is rare. Do NOT give 5/5 unless the content is truly exceptional.

### Part 1: Craft Quality (6 dimensions, 1-5 each)

#### 1. Hook Power (15% weight)
- 5 = Impossible to stop reading. Creates immediate curiosity or tension.
- 4 = Strong opening that grabs attention.
- 3 = Decent hook but could be stronger.
- 2 = Weak opening, easy to scroll past.
- 1 = No hook at all.

#### 2. Authenticity (15% weight)
- 5 = Genuine personal voice. Real stories. Specific details. Conversational.
- 4 = Mostly authentic with minor generic phrases.
- 3 = Mix of personal and templated content.
- 2 = Mostly formal/corporate. Feels AI-generated.
- 1 = Obvious AI slop. Buzzwords everywhere.

#### 3. Value Density (15% weight)
- 5 = Every sentence delivers insight or value. Zero filler.
- 4 = High value with minimal filler.
- 3 = Good content but some filler paragraphs.
- 2 = Mostly filler with occasional good points.
- 1 = No actionable value.

#### 4. Credibility (15% weight)
- 5 = Concrete numbers, real examples, specific experience cited.
- 4 = Good evidence with minor generalizations.
- 3 = Some evidence but too many vague claims.
- 2 = Mostly unsupported claims.
- 1 = Pure opinion with zero evidence.

#### 5. Engagement Potential (10% weight)
- 5 = Will definitely spark comments and shares. Strong CTA.
- 4 = Good discussion potential. Clear CTA.
- 3 = Some engagement hooks but not compelling.
- 2 = Passive reading experience. Weak CTA.
- 1 = No engagement mechanism.

#### 6. Platform Optimization (5% weight)
- 5 = Perfect format for the platform.
- 4 = Minor formatting issues.
- 3 = Noticeable formatting problems.
- 2 = Wrong format for the platform.
- 1 = Completely wrong format.

### Part 2: Reader Perspective (3 dimensions, 1-5 each)

Put yourself in the reader's shoes. You are a busy professional scrolling through your feed.

#### 7. Emotional Resonance (10% weight)
How does this content make the reader FEEL?
- 5 = Triggers a strong emotion (inspiration, surprise, recognition, urgency). Reader feels something.
- 4 = Evokes mild positive emotion or curiosity.
- 3 = Emotionally flat. Reader feels nothing specific.
- 2 = Feels preachy, condescending, or performative.
- 1 = Triggers negative reaction (cringe, distrust, annoyance).

#### 8. Perceived Intent (10% weight)
What does the reader think the author WANTS from them?
- 5 = "This person genuinely wants to help me." Feels generous.
- 4 = "Interesting perspective, worth my time." Feels balanced.
- 3 = "Not sure what they want." Mixed signals.
- 2 = "They're trying to sell me something." Feels transactional.
- 1 = "This is pure self-promotion." Feels extractive.

#### 9. Trust Signal (5% weight)
Would the reader trust this author after reading?
- 5 = "I want to follow this person." Builds real authority.
- 4 = "They seem credible." Mildly increases trust.
- 3 = "Neutral." Neither builds nor damages trust.
- 2 = "Something feels off." Vague claims raise skepticism.
- 1 = "This is BS." Actively damages credibility.

### Quality Gate

Both conditions must pass:
- **Weighted average >= 4.0** (across all 9 dimensions)
- **No single dimension below 3.0**

## Output

### Quality Scorecard

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
```

### Sentiment Summary
2-3 sentences: How does this content feel from the reader's perspective? What emotion does it trigger? What impression does it leave about the author?

### Top Issues
For the 3 lowest-scoring dimensions, provide:
- What specifically is wrong
- A concrete suggestion for improvement
- A before/after example showing the fix

### Verdict
- **PASS** (>= 4.0, no dim < 3.0): "Ready to publish."
- **FAIL** (< 4.0 or any dim < 3.0): "Needs revision. Focus on [lowest dimensions] first."

## After Review

Ask: "Would you like me to:
- Rewrite the content applying this feedback
- Review additional content
- Focus on fixing just the failing dimensions
- Adapt this content for a different platform"
