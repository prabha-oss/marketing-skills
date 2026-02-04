# Marketing Skills

A collection of expert marketing plugins for Claude Code. Built for [skills.sh](https://skills.sh) ecosystem.

## Installation

```bash
npx skills add prabha-oss/marketing-skills
```

Or install individual plugins:
```bash
npx skills add prabha-oss/marketing-skills/cold-calling
npx skills add prabha-oss/marketing-skills/cold-email
npx skills add prabha-oss/marketing-skills/funnel-builder
npx skills add prabha-oss/marketing-skills/competitor-alternatives
npx skills add prabha-oss/marketing-skills/landing-page-intake
npx skills add prabha-oss/marketing-skills/landing-page-writer
```

## Available Plugins

| Plugin | Description |
|--------|-------------|
| `cold-calling` | Cold call scripts, openers, objection handling, discovery questions |
| `cold-email` | Cold email frameworks (PAS, 4P, AIDA), sequences, CTAs |
| `funnel-builder` | Marketing funnels with stages, copy, and Mermaid diagrams |
| `competitor-alternatives` | Competitor comparison and alternative pages for SEO |
| `landing-page-intake` | Structured intake process for landing page copy briefs |
| `landing-page-writer` | Section-by-section landing page copywriter with lock-in workflow |

## Plugin Details

### Cold Calling

Sub-skills included:
- **Opener Generator** — Permission-based, pattern-interrupt, direct openers
- **Objection Handler** — Acknowledge → Reframe → Redirect framework
- **Discovery Questions** — Qualifying questions that don't pitch
- **CTA Selector** — Right next step for each situation
- **Script Assembler** — Complete call flows

### Cold Email

Sub-skills included:
- **Framework Selector** — PAS, 4P, AIDA, One-Line
- **Subject Line Generator** — Open-worthy subjects
- **Email Writer/Rewriter** — Draft and shorten emails
- **Sequence Builder** — Multi-touch follow-up sequences
- **CTA Optimizer** — Soft, high-converting CTAs

### Funnel Builder

Funnel types included:
- **Free Trial** — SaaS low-touch
- **Demo Request** — SaaS high-touch
- **Strategy Call** — Agency/services
- **Product** — E-commerce
- **Webinar** — Courses mid-ticket
- **Application** — High-ticket coaching
- **Local Lead** — Local services

### Competitor Alternatives

Page formats covered:
- Singular alternative pages
- Plural alternatives pages
- You vs Competitor pages
- Competitor vs Competitor pages

### Landing Page Intake

Structured intake process:
- **17-question discovery** — Collects all info needed for copy
- **Structure recommendation** — Service vs product base, optional sections
- **Confirmation flow** — User approves before finalizing
- **Copy-ready brief** — Outputs intake summary + section inputs

### Landing Page Writer

Section-by-section copywriter:
- **Lock-in workflow** — Generate 10 options → User picks → Lock → Next micro-step
- **Style matching** — Matches tone/rhythm from user's reference copy
- **Micro-steps** — Hero (H1-H5), Features (F0-F3), Process (P1-Pn), FAQ, CTA
- **No buzzwords** — Enforced banned words list for concrete copy
- **Length limits** — Strict character/word counts per element

## Usage

After installation, use skills with any compatible AI agent:

```
"Write a cold email for SaaS CTOs about reducing churn"
"Generate 5 cold call openers for agency owners"
"Handle the 'send me an email' objection"
"Build a funnel for my $2k coaching program"
"Create a comparison page for Notion vs Coda"
"Start landing page intake for my service business"
"Write landing page copy using my intake summary"
```

## Project Structure

```
marketing-skills/
├── .claude-plugin/
│   └── marketplace.json
├── CLAUDE.md
├── README.md
└── plugins/
    ├── cold-calling/
    │   ├── .claude-plugin/plugin.json
    │   └── skills/cold-calling/
    │       ├── SKILL.md
    │       └── references/
    ├── cold-email/
    │   ├── .claude-plugin/plugin.json
    │   └── skills/cold-email/
    │       ├── SKILL.md
    │       └── references/
    ├── funnel-builder/
    │   ├── .claude-plugin/plugin.json
    │   └── skills/funnel-builder/
    │       ├── SKILL.md
    │       └── references/
    ├── competitor-alternatives/
    │   ├── .claude-plugin/plugin.json
    │   └── skills/competitor-alternatives/
    │       ├── SKILL.md
    │       └── references/
    ├── landing-page-intake/
    │   ├── .claude-plugin/plugin.json
    │   └── skills/landing-page-intake/
    │       ├── SKILL.md
    │       └── references/
    └── landing-page-writer/
        ├── .claude-plugin/plugin.json
        └── skills/landing-page-writer/
            ├── SKILL.md
            └── references/
```

## Philosophy

These skills encode **marketing reasoning**, not just templates:
- Decision-making frameworks over copy templates
- Systematic approaches over random tactics
- Qualification logic over persuasion tricks

## License

MIT
