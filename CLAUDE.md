# Marketing Skills - Expert Marketing Automation

## What This Is

A marketplace of expert marketing plugins for Claude Code. Each plugin can be installed individually.

## Available Plugins

| Plugin | Command | Purpose |
|--------|---------|---------|
| cold-calling | `/cold-calling` | Cold call scripts, openers, objection handling |
| cold-email | `/cold-email` | Cold email frameworks, sequences, CTAs |
| funnel-builder | `/funnel-builder` | Marketing funnels with stages, copy, diagrams |
| competitor-alternatives | `/competitor-alternatives` | Competitor comparison and alternative pages |

## Cold Calling Skill

### Quick Reference

**Opener Types:**
- Permission-based: "Did I catch you at a bad time?"
- Pattern-interrupt: "Quick context so I don't waste your time..."
- Direct: "Quick question — are you handling {{responsibility}}?"

**Objection Framework:** Acknowledge → Reframe → Redirect

**The 5 Common Objections:**
1. "Not interested"
2. "Send an email"
3. "No time"
4. "We have someone"
5. "Call later"

### Key Rules

- First 10 seconds decide everything
- Speak less than 50% of the time
- One CTA only
- Never argue objections

## Cold Email Skill

### Frameworks

| Situation | Framework |
|-----------|-----------|
| Strong pain | PAS (Problem-Agitate-Solution) |
| Need credibility | 4P (Personalization-Problem-Proof-Proposal) |
| General awareness | AIDA |
| Senior executives | One-Line Email |

### Key Rules

- 50-120 words max
- One idea per email
- Plain text only
- Soft CTA only
- No Calendly in first email

## Funnel Builder Skill

### Funnel Selection

| Business | Price | Funnel Type |
|----------|-------|-------------|
| SaaS | <$100/mo | Free Trial |
| SaaS | >$100/mo | Demo Request |
| Agency | >$2k | Strategy Call |
| E-commerce | <$100 | Product |
| Course | <$500 | Webinar |
| Coaching | >$500 | Application |
| Local | Varies | Local Lead |

### Output Format

Each funnel includes:
1. Stage breakdown (purpose, content, metrics)
2. Copy elements (headlines, CTAs, emails)
3. Mermaid diagram (visual flowchart)

## Competitor Alternatives Skill

### Page Formats

| Format | URL Pattern |
|--------|-------------|
| Singular Alternative | `/alternatives/[competitor]` |
| Plural Alternatives | `/alternatives/[competitor]-alternatives` |
| You vs Competitor | `/vs/[competitor]` |
| Competitor vs Competitor | `/compare/[a]-vs-[b]` |

### Core Principles

- Honesty builds trust
- Depth over surface
- Help them decide
- Modular architecture

## Best Practices

1. **Check for context first** — Look for `.claude/business-context.md`
2. **Ask clarifying questions** — Don't assume
3. **Reference files for detail** — Keep SKILL.md responses short
4. **Output ready-to-use content** — Not just advice
