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
| landing-page-intake | `/landing-page-intake` | Structured intake for landing page copy briefs |
| landing-page-writer | `/landing-page-writer` | Write landing page copy section-by-section |

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

## Landing Page Intake Skill

### Purpose

Collects minimum information needed to write landing page copy. Does NOT write copy — outputs a structured brief.

### Question Flow (17 questions max)

**Batch 1 (Q0-Q4):** Business type, name, offer, audience, CTA
**Batch 2 (Q5-Q8):** Trigger, problems, outcome, timeframe
**Batch 3 (Q9-Q11):** Differentiation, proof
**Batch 4 (Q12-Q16):** Process, objections, boundaries

### Output

```
INTAKE SUMMARY
[All answers organized]

CONFIRMED LANDING PAGE STRUCTURE
[Recommended sections in order]

SECTION INPUTS
[Copy-ready notes per section]
```

### Key Rules

- Max 4 questions per message
- Must confirm structure before finalizing
- Recommend sections based on answers (not generic)
- Add [TBD proof] placeholders if proof missing

## Landing Page Writer Skill

### Purpose

Writes landing page copy using intake summary. Step-by-step lock-in workflow.

### Requires

1. INTAKE SUMMARY (from landing-page-intake)
2. CONFIRMED STRUCTURE (from landing-page-intake)
3. STYLE REFERENCE COPY (user pastes example copy)

### Lock-In Workflow

```
Generate 10 options → User picks ID → "Locked: {ID}" → Next micro-step
```

### Micro-Steps (per section)

**Hero:** H1 headline → H2 subheadline → H3 credibility → H4 CTA → H5 microcopy
**Features:** F0 themes → Fi1 header → Fi2 paragraph → Fi3 proof placeholder
**Process:** P1 all titles → P2-Pn subtitles → P_last closing line
**FAQ:** FAQ0 questions → FAQi answers
**CTA:** CTA1 headline → CTA2 button → CTA3 microcopy

### Key Rules

- Never invent proof (use `[TBD proof]`)
- Match style reference tone/rhythm
- No buzzwords (see banned-words.md)
- One micro-step per message

## Best Practices

1. **Check for context first** — Look for `.claude/business-context.md`
2. **Ask clarifying questions** — Don't assume
3. **Reference files for detail** — Keep SKILL.md responses short
4. **Output ready-to-use content** — Not just advice
