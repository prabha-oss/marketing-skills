# Marketing Skills

A collection of AI agent skills for marketing tasks. Built for [skills.sh](https://skills.sh) ecosystem.

## Installation

```bash
npx skills add prabha-oss/marketing-skills
```

## Available Skills

| Skill | Description |
|-------|-------------|
| `competitor-alternatives` | Create competitor comparison and alternative pages for SEO and sales enablement |
| `cold-calling` | Complete cold calling system: openers, objection handling, discovery, scripts |
| `cold-email` | Cold email system: frameworks, sequences, CTAs, rewriting |

## Skill Details

### Cold Calling

Full taxonomy of sub-skills:
- **ICP Call Qualifier** — Decide if a lead is worth calling
- **Opener Generator** — Pattern-interrupt openers
- **Reason-for-Call Builder** — "Why you, why now" statements
- **Discovery Question Generator** — Qualify without pitching
- **Objection Handler** — Systematic objection responses
- **CTA Selector** — Right next step for each situation
- **Full Script Assembler** — Complete call flows

### Cold Email

Full taxonomy of sub-skills:
- **Framework Selector** — Choose PAS, 4P, AIDA, or One-Line
- **Subject Line Generator** — Open-worthy subjects
- **Email Writer** — Draft emails from scratch
- **Email Rewriter** — Shorten and clarify existing emails
- **Follow-Up Sequence Builder** — Multi-touch sequences
- **CTA Optimizer** — Improve call-to-action conversion

### Competitor Alternatives

Page formats covered:
- Singular alternative pages
- Plural alternatives pages
- You vs Competitor pages
- Competitor vs Competitor pages

## Usage

After installation, use skills with any compatible AI agent (Claude Code, Cursor, etc.):

```
"Write a cold email for SaaS CTOs about reducing churn"
"Generate 5 cold call openers for agency owners"
"Handle the 'send me an email' objection"
"Create a comparison page for Notion vs Coda"
"Rewrite this cold email to be shorter"
```

## Philosophy

These skills encode **sales reasoning**, not just scripts:
- Decision-making frameworks over copy templates
- Systematic approaches over random tactics
- Qualification logic over persuasion tricks

## Adding More Skills

Each skill lives in `skills/{skill-name}/SKILL.md`. See [skills.sh documentation](https://github.com/vercel-labs/skills) for the skill format.

## License

MIT
