---
description: Generate a weekly performance report analyzing content metrics, engagement patterns, and strategic recommendations.
argument-hint: "[time period]"
---

# Performance Report

> Weekly analytics that goes beyond vanity metrics. Identifies patterns, compares against goals, and provides specific recommendations for the next week.

## Trigger

User runs `/autonoma:report` or asks for analytics, performance report, or content metrics.

## Inputs

1. **Time period** — which week/month to analyze (default: last 7 days)
2. **Goals** (optional) — what were the targets for this period
3. **Data source** — analytics platform (Amplitude if connected), manual data, or file with metrics

## Report Process

### Step 1: Gather Data

Collect metrics from available sources:
- Content published (count, types, platforms)
- Engagement metrics (likes, comments, shares, saves)
- Reach/impressions
- Follower growth
- Click-through rates
- Email open/click rates (if applicable)

### Step 2: Analyze Patterns

Go beyond surface metrics:

| Analysis | What to look for |
|----------|-----------------|
| **Top performers** | Which content got the most engagement? Why? |
| **Platform comparison** | Which platform delivers the best ROI? |
| **Topic performance** | Which topics resonate most with the audience? |
| **Timing patterns** | When does the audience engage most? |
| **Content type comparison** | Posts vs articles vs threads — what works? |
| **Engagement quality** | Comments from target audience vs random engagement? |

### Step 3: Compare to Goals

If goals were set, show progress:
- Follower growth vs target
- Content output vs target
- Engagement rate vs benchmark
- Lead generation vs target

### Step 4: Recommendations

Provide 3-5 specific, actionable recommendations for the next period:
- What to do MORE of (backed by data)
- What to STOP doing (low ROI)
- What to EXPERIMENT with (hypothesis-driven)
- Content topics to prioritize (based on engagement patterns)

## Output

Save to `analytics/weekly-report-[date].md`

Present as:

### Week in Numbers (dashboard-style metrics)
### Top 3 Performers (with analysis of why)
### Patterns & Insights
### Recommendations for Next Week
### Goals Tracker (if goals were set)

## After Report

Ask: "Would you like me to:
- Plan next week's content based on these insights (`/autonoma:plan`)
- Deep-dive into a specific metric
- Set goals for the next period
- Research trends around the top-performing topics (`/autonoma:trends`)"
