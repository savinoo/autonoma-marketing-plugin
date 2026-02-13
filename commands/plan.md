---
description: Create a data-driven editorial calendar with content pillars, topic prioritization, and weekly scheduling.
argument_hint: "[business goals]"
---

# Editorial Calendar

> Strategic content planning that connects business goals to specific content pieces. Creates content pillars and a weekly calendar with assigned topics, platforms, and priorities.

## Trigger

User runs `/autonoma:plan` or asks to plan content, create an editorial calendar, or define content strategy.

## Inputs

1. **Business goals** — what the business is trying to achieve (e.g., "grow LinkedIn following to 5K", "establish authority in AI agents", "generate leads for SaaS product")
2. **Time period** — how far ahead to plan (default: 1 week)
3. **Available platforms** — which platforms to include (default: LinkedIn, Twitter/X)
4. **Previous analytics** (optional) — what content has performed well before
5. **Trends data** (optional) — run `/autonoma:trends` first for timely planning

## Planning Process

### Step 1: Define Content Pillars

Content pillars are the 3-5 core themes that all content maps back to. Each pillar should:
- Directly support a business goal
- Have enough depth for 10+ pieces of content
- Resonate with the target audience
- Differentiate from competitors

For each pillar, define:
- **Name**: Short, memorable label
- **Description**: What this pillar covers and why
- **Keywords**: 3-5 target keywords for SEO

### Step 2: Generate Calendar

Create a weekly calendar with 5-7 content pieces. For each piece:

| Field | Description |
|-------|-------------|
| Topic | Specific topic to cover |
| Platform | Target platform |
| Content Type | Post, article, thread, newsletter |
| Pillar | Which content pillar it maps to |
| Angle | Unique hook or perspective |
| Target Keyword | Primary SEO keyword |
| CTA | What action readers should take |
| Priority | 1-10 (higher = more important) |
| Scheduled Date | Suggested publication date |

### Step 3: Prioritization

Rank content by:
1. **Strategic alignment** — how well it serves business goals
2. **Timeliness** — trending topics get priority
3. **Effort/impact ratio** — quick wins before big projects
4. **Audience demand** — what the audience has engaged with before

## Output

Save the calendar to `strategy/editorial-calendar-[date].md`

Present:
1. Content pillars summary
2. Weekly calendar as a table
3. Rationale for top 3 priority pieces

## After Planning

Ask: "Would you like me to:
- Generate content for the highest-priority piece (`/autonoma:generate`)
- Create detailed briefs for each calendar entry
- Research trends to inform the calendar (`/autonoma:trends`)
- Adjust the plan based on feedback"
