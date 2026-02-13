---
description: Adapt approved content for multiple platforms while maintaining quality and brand voice. One piece becomes 3-5 platform-optimized versions.
argument_hint: "[file path or paste content]"
---

# Distribute Content

> Take one piece of approved content and adapt it for multiple platforms. Each adaptation is optimized for the target platform's format, audience, and algorithm.

## Trigger

User runs `/autonoma:distribute` or asks to distribute, adapt, repurpose, or cross-post content.

## Inputs

1. **Source content** — the approved content to distribute (file path or pasted)
2. **Source platform** — where it was originally written for
3. **Target platforms** — which platforms to adapt for (default: all available)
4. **Priority message** (optional) — what's the ONE thing every version must convey

## Available Platform Adaptations

| Platform | Format | Key Constraints |
|----------|--------|-----------------|
| LinkedIn | Post | 1200-1500 chars, no links in body, personal voice, 3-5 hashtags at end |
| Twitter/X | Thread | 280 chars/tweet, numbered, hook on tweet 1, CTA on last tweet |
| Blog | Article | 800-2000 words, SEO-optimized, headers every 200-300 words |
| Email | Newsletter | Subject < 50 chars, 1 CTA, scannable, mobile-first |
| Instagram | Caption | Visual-first, storytelling hook, hashtags in first comment |

## Adaptation Process

For each target platform:

### Step 1: Extract Core Message
Identify the central insight, story, or argument from the source content.

### Step 2: Platform-Native Rewrite
Rewrite completely for the target platform — not just truncate or reformat. Each version should feel native to its platform.

### Step 3: Quality Check
Run the 6-dimension quality review on each adapted version. All versions must score >= 3.5/5.0 (slightly lower threshold since these are adaptations, not originals).

## Output

Save each version to `drafts/[platform]-[topic-slug]-distributed.md`

Present all versions with their quality scores.

## After Distribution

Ask: "Would you like me to:
- Improve any specific version
- Share via Slack (if connected)
- Create visuals via Canva (if connected)
- Schedule in your content calendar"
