---
description: Peer-review existing content with a 6-dimension quality rubric. Get specific, actionable feedback with quality scores.
argument-hint: "[file or paste content]"
---

# Review Content

> Apply Autonoma's 6-dimension quality rubric to any marketing content. Get scored feedback with specific revision suggestions.

## Trigger

User runs `/autonoma:review` or asks to review, evaluate, score, or critique content.

## Inputs

1. **Content to review** — accept in any form:
   - Pasted directly into conversation
   - A file path (e.g., `drafts/linkedin-ai-agents-v1.md`)
   - Multiple pieces for batch review

2. **Platform context** — which platform is this for? (affects Platform Optimization scoring)

3. **Brand guidelines** — use the brand-voice skill automatically. If the user has custom guidelines, they override defaults.

## Review Process

Adopt the perspective of a **senior content editor and marketing strategist**. Evaluate with brutal honesty — sugar-coating helps nobody.

### Score on 6 Dimensions (1-5 each)

#### 1. Hook Power (20% weight)
- 5 = Impossible to stop reading. Creates immediate curiosity or tension.
- 4 = Strong opening that grabs attention.
- 3 = Decent hook but could be stronger.
- 2 = Weak opening, easy to scroll past.
- 1 = No hook at all.

#### 2. Authenticity (20% weight)
- 5 = Genuine personal voice. Real stories. Specific details. Conversational.
- 4 = Mostly authentic with minor generic phrases.
- 3 = Mix of personal and templated content.
- 2 = Mostly formal/corporate. Feels AI-generated.
- 1 = Obvious AI slop. Buzzwords everywhere.

#### 3. Value Density (20% weight)
- 5 = Every sentence delivers insight or value. Zero filler.
- 4 = High value with minimal filler.
- 3 = Good content but some filler paragraphs.
- 2 = Mostly filler with occasional good points.
- 1 = No actionable value.

#### 4. Engagement Potential (15% weight)
- 5 = Will definitely spark comments and shares. Strong CTA.
- 4 = Good discussion potential. Clear CTA.
- 3 = Some engagement hooks but not compelling.
- 2 = Passive reading experience. Weak CTA.
- 1 = No engagement mechanism.

#### 5. Credibility (15% weight)
- 5 = Concrete numbers, real examples, specific experience cited.
- 4 = Good evidence with minor generalizations.
- 3 = Some evidence but too many vague claims.
- 2 = Mostly unsupported claims.
- 1 = Pure opinion with zero evidence.

#### 6. Platform Optimization (10% weight)
- 5 = Perfect format for the platform.
- 4 = Minor formatting issues.
- 3 = Noticeable formatting problems.
- 2 = Wrong format for the platform.
- 1 = Completely wrong format.

### Quality Gate

Both conditions must pass:
- **Weighted average >= 4.0**
- **No single dimension below 3.0**

## Output

Present the review as:

### Quality Scorecard
Show each dimension with score, then the weighted average.

### Top Issues
For the 3 lowest-scoring dimensions, provide:
- What specifically is wrong
- A concrete suggestion for improvement
- A before/after example showing the fix

### Feedback
Provide specific, actionable feedback. Instead of "make it more engaging", say "add a specific metric in paragraph 2 and replace the generic closing with a provocative question about X".

### Verdict
- **PASS** (>= 4.0, no dimension < 3.0): "Ready to publish. Minor suggestions above are optional improvements."
- **FAIL** (< 4.0 or any dimension < 3.0): "Needs revision. Focus on [lowest dimensions] first."

## After Review

Ask: "Would you like me to:
- Rewrite the content applying this feedback
- Review additional content
- Focus on fixing just the failing dimensions
- Adapt this content for a different platform"
