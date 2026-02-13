---
description: Research keywords, analyze search intent, and optimize content for search engines and AI discovery (GEO).
argument-hint: "[topic or keyword]"
---

# SEO Research

> Keyword research and content optimization for both traditional search engines and AI-powered discovery (Generative Engine Optimization).

## Trigger

User runs `/autonoma:seo` or asks about keywords, SEO, search optimization, or content discoverability.

## Inputs

1. **Topic or seed keyword** — starting point for research
2. **Target audience** — who should find this content
3. **Content type** (optional) — blog post, landing page, etc.
4. **Existing content** (optional) — content to optimize

## Research Process

### Step 1: Keyword Discovery

Research and categorize keywords:

| Category | Description |
|----------|-------------|
| Primary keyword | Main target (highest relevance + volume) |
| Secondary keywords | 2-3 supporting terms |
| Long-tail keywords | Specific phrases with lower competition |
| Questions | "How to...", "What is...", "Why does..." |
| Related topics | Adjacent concepts to cover for topical authority |

For each keyword, estimate:
- Search intent (informational, navigational, transactional)
- Competition level (low, medium, high)
- Content fit (which content type best serves this keyword)

### Step 2: GEO (Generative Engine Optimization)

AI search engines (ChatGPT, Perplexity, Claude) are becoming major traffic sources. Optimize for them:

- **Be the definitive source** — comprehensive, well-structured content gets cited
- **Use clear definitions** — AI models extract structured answers
- **Include data and statistics** — cited more often than opinions
- **Structured format** — lists, tables, and headers help AI parsing
- **Entity associations** — connect your content to known entities and brands

### Step 3: Content Recommendations

Based on the keyword research, provide:
- Recommended title (with primary keyword)
- Meta description template
- Content outline with keyword placement
- Internal linking suggestions
- Competitive gaps (what competitors rank for that you don't cover)

## Output

Save to `seo/keyword-research-[topic-slug].md`

Present as:

### Keyword Map
Table with all discovered keywords, intent, competition, and recommended content type.

### Content Brief
Optimized outline ready for content generation.

### Quick Wins
Keywords where you can rank with minimal effort.

## After Research

Ask: "Would you like me to:
- Generate SEO-optimized content for the top keyword (`/autonoma:generate`)
- Optimize existing content with these keywords
- Plan a content cluster around this topic (`/autonoma:plan`)
- Research a related topic"
