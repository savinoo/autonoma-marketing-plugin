# Autonoma Marketing — Cowork Plugin

A marketing content plugin with a structured quality review process. Generate content, score it on 6 dimensions, refine until it passes, then distribute across platforms.

## How It Works

1. **Generate** — Create content for a specific platform and topic
2. **Review** — Score the content on 6 quality dimensions (1-5 scale)
3. **Refine** — If it doesn't pass the threshold, iterate (up to 3 rounds)
4. **Distribute** — Adapt the final content for other platforms

The review step uses a different "perspective" than the generation step — the idea is that writing and critiquing are separate tasks, so separating them can catch issues that self-review misses.

## Commands

| Command | What It Does |
|---------|-------------|
| `/autonoma:generate` | Create content with automatic review and quality scoring |
| `/autonoma:review` | Score existing content on 6 quality dimensions |
| `/autonoma:plan` | Create an editorial calendar with content pillars |
| `/autonoma:trends` | Research market trends with scored findings |
| `/autonoma:seo` | Keyword research + GEO (Generative Engine Optimization) |
| `/autonoma:distribute` | Adapt content for multiple platforms |
| `/autonoma:report` | Weekly performance analytics with recommendations |

## Skills

| Skill | Description |
|-------|-------------|
| **quality-gates** | 6-dimension rubric, review process, threshold enforcement |
| **brand-voice** | Customizable brand guidelines, tone, audience, formatting |
| **content-creation** | Platform-specific templates and best practices |
| **intelligence** | Market research methodology and finding scoring |
| **strategy** | Content pillars, editorial calendar, planning framework |

## Quality Rubric

Every piece of content is scored on:

| Dimension | Weight |
|-----------|--------|
| Hook Power | 20% |
| Authenticity | 20% |
| Value Density | 20% |
| Engagement Potential | 15% |
| Credibility | 15% |
| Platform Optimization | 10% |

**Pass conditions**: Weighted average >= 4.0/5.0 AND no single dimension below 3.0.

You can adjust the threshold in `skills/quality-gates/SKILL.md`.

## Installation

### Via Claude Code
```bash
claude plugin marketplace add savinoo/autonoma-marketing-plugin
claude plugin install autonoma-marketing
```

### Manual
Clone this repo into your plugins folder:
```bash
git clone https://github.com/savinoo/autonoma-marketing-plugin.git
```

## Customization

### Brand Voice
Edit `skills/brand-voice/SKILL.md` to match your company's voice, tone, and audience. This is the first thing you should customize — the defaults are Autonoma's own brand voice.

### Connectors
Edit `.mcp.json` to connect your tools (Slack, Notion, HubSpot, etc.). See `CONNECTORS.md` for setup details.

## Built by Autonoma

- Website: [autonoma-ai.dev](https://autonoma-ai.dev)
- Creator: Lucas Lorenzo Savino

## License

Apache-2.0
