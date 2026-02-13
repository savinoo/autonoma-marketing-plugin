# Autonoma Marketing — Cowork Plugin

**The only marketing plugin with built-in quality gates and peer review.**

Most AI content tools generate and deliver. Autonoma generates, then reviews from a different perspective, scoring on 6 quality dimensions. Only content that passes the quality threshold (>= 4.0/5.0) gets delivered.

## What Makes This Different

| Feature | Default Marketing Plugin | Autonoma Marketing |
|---------|------------------------|-------------------|
| Content generation | Single-shot | Multi-step pipeline |
| Quality control | None | 6-dimension scoring rubric |
| Peer review | No | Creator writes, Reviewer evaluates |
| Degradation protection | No | Keeps best version across revisions |
| Quality threshold | No | >= 4.0/5.0, no dimension below 3.0 |
| Trend intelligence | Basic | Scored findings (relevance x materiality x confidence) |
| Editorial calendar | Basic | Data-driven with content pillars |

## Commands

| Command | What It Does |
|---------|-------------|
| `/autonoma:generate` | Create content with automatic peer review and quality scoring |
| `/autonoma:review` | Score existing content on 6 quality dimensions |
| `/autonoma:plan` | Create a data-driven editorial calendar with content pillars |
| `/autonoma:trends` | Research market trends with scored intelligence findings |
| `/autonoma:seo` | Keyword research + GEO (Generative Engine Optimization) |
| `/autonoma:distribute` | Adapt content for multiple platforms with quality checks |
| `/autonoma:report` | Weekly performance analytics with actionable recommendations |

## Skills

| Skill | Description |
|-------|-------------|
| **quality-gates** | 6-dimension rubric, peer-review process, threshold enforcement |
| **brand-voice** | Customizable brand guidelines, tone, audience, formatting |
| **content-creation** | Platform-specific templates and best practices |
| **intelligence** | Market research methodology and finding scoring |
| **strategy** | Content pillars, editorial calendar, data-driven planning |

## Installation

### Via Claude Cowork
Install directly from the plugin marketplace in Claude Desktop.

### Via Claude Code
```bash
claude plugin install autonoma-marketing
```

### Manual
Clone this directory into your Cowork plugins folder.

## Customization

### Brand Voice
Edit `skills/brand-voice/SKILL.md` to match your company's voice, tone, and audience. This is the first thing you should customize.

### Connectors
Edit `.mcp.json` to connect your specific tools (Slack, Notion, HubSpot, etc.). See `CONNECTORS.md` for details.

### Quality Threshold
The default quality threshold is 4.0/5.0. To adjust, edit the threshold in `skills/quality-gates/SKILL.md`.

## The Quality Rubric

Every piece of content is scored on:

| Dimension | Weight | What 5/5 Means |
|-----------|--------|-----------------|
| Hook Power | 20% | Impossible to stop reading |
| Authenticity | 20% | Genuine voice, specific details |
| Value Density | 20% | Every sentence delivers insight |
| Engagement Potential | 15% | Will spark comments and shares |
| Credibility | 15% | Concrete numbers, real examples |
| Platform Optimization | 10% | Perfect format for the platform |

**Pass conditions**: Weighted average >= 4.0 AND no single dimension below 3.0.

## Built by Autonoma

Autonoma is an AI-operated company where specialized AI agents handle each business function. This plugin packages the marketing team's quality methodology for anyone to use.

- Website: [autonoma-ai.dev](https://autonoma-ai.dev)
- Creator: Lucas Lorenzo Savino

## License

Apache-2.0
