---
description: Research current market trends, competitor moves, and industry developments. Produces actionable intelligence for content creation.
argument-hint: "[research topic]"
---

# Trend Intelligence

> Market research agent that finds what's happening NOW in your industry. Produces scored findings ranked by relevance and actionability.

## Trigger

User runs `/autonoma:trends` or asks to research trends, analyze the market, or find what's happening in their industry.

## Inputs

1. **Research topic** — what to investigate (e.g., "AI agents in enterprise", "marketing automation trends", "competitor analysis for [product]")
2. **Industry focus** (optional) — narrow the search scope
3. **Time frame** — how recent (default: last 30 days)

## Research Process

### Step 1: Multi-Source Research

Search across multiple sources for the most recent and relevant information:
- Industry news and publications
- Social media discussions (LinkedIn, Twitter/X)
- Competitor announcements and product launches
- Market reports and analyst insights
- Community discussions (Reddit, Hacker News, forums)

### Step 2: Score Each Finding

For each finding, assess:

| Metric | Scale | What it means |
|--------|-------|---------------|
| Relevance | 0-1 | How relevant to the user's market |
| Materiality | 0-1 | Is this genuinely new/important, or noise? |
| Confidence | 0-1 | How well-supported is this finding? |

Only include findings with relevance >= 0.5 AND materiality >= 0.5.

### Step 3: Extract Actionable Insights

For each high-scoring finding, identify:
- How the user's business can leverage this
- Content topics it suggests
- Strategic implications
- Competitive threats or opportunities

## Output

Save the report to `intelligence/trends-[date].md`

Present as:

### Executive Summary
2-3 sentence overview of the most important findings.

### Top Findings (ranked by relevance x materiality)

For each finding:
- **Title**: Brief, descriptive
- **Summary**: 2-3 sentences
- **Scores**: Relevance / Materiality / Confidence
- **Actionable Insight**: What to do with this information
- **Content Ideas**: 1-2 topic suggestions

### Recommended Actions
Prioritized list of what to do based on the research.

## After Research

Ask: "Would you like me to:
- Plan content around these trends (`/autonoma:plan`)
- Generate a post about the top finding (`/autonoma:generate`)
- Deep-dive into a specific finding
- Research a different topic"
