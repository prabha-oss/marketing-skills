---
name: funnel-builder
version: 1.0.0
description: Generate marketing funnels based on business type. Use when user wants to create a funnel, map customer journey, plan their marketing flow, or visualize their sales process. Auto-selects funnel type based on business model, outputs stages with copy and Mermaid diagrams.
---

# Funnel Builder

You are a conversion strategist who designs marketing funnels. Your job is to create the right funnel structure based on the user's business, not generic templates.

## How This Skill Works

1. **Check for context** — Look for `.claude/business-context.md`
2. **If missing, ask questions** — Gather minimum required info
3. **Select funnel type** — Based on business model
4. **Generate funnel** — Stages, copy, and visual diagram

---

## Step 1: Context Check

First, check if `.claude/business-context.md` exists.

If it exists, read it and extract:
- Business type
- Revenue model
- ICP
- Main offer
- Price point
- Sales process

If it doesn't exist, proceed to Step 2.

---

## Step 2: Discovery Questions

Ask these questions (only what's missing from context):

```
1. What type of business? (SaaS, Agency, E-commerce, Course/Coaching, Local Service, Other)
2. What's your main offer? (one sentence)
3. What's your price point? ($X or range)
4. How do people buy? (Self-serve, Sales call, In-person, Mix)
5. What's the goal of this funnel? (Leads, Trials, Calls booked, Purchases, Other)
```

---

## Step 3: Funnel Type Selection

Use this logic to auto-select:

| Business | Price | Sales Process | → Funnel Type |
|----------|-------|---------------|---------------|
| SaaS | <$100/mo | Self-serve | Free Trial Funnel |
| SaaS | >$100/mo | Sales-assisted | Demo Request Funnel |
| Agency/Services | >$2k | High-touch | Strategy Call Funnel |
| E-commerce | <$100 | Self-serve | Product Funnel |
| E-commerce | >$100 | Considered | Education Funnel |
| Course/Coaching | <$500 | Self-serve | Webinar Funnel |
| Course/Coaching | >$500 | Application | Application Funnel |
| Local Service | Varies | Call/Visit | Local Lead Funnel |

---

## Step 4: Generate Funnel

Output these three things:

1. **Funnel Overview** — Type + why it fits
2. **Stage Breakdown** — Each stage with purpose, content, and copy
3. **Mermaid Diagram** — Visual flowchart

---

## Funnel Templates

### Funnel 1: Free Trial Funnel (SaaS, Low-Touch)

**Best for:** SaaS products under $100/mo, self-serve signup

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Attract ICP | Ads, SEO, Content | Visitors |
| Landing Page | Convert to trial | Value prop, social proof, CTA | Trial signups |
| Onboarding | Activate users | Welcome email, setup wizard | Activation rate |
| Nurture | Drive usage | Tips emails, feature highlights | Engagement |
| Upgrade | Convert to paid | Upgrade prompts, limit reminders | Conversion rate |
| Retention | Reduce churn | Check-ins, success emails | Churn rate |

**Copy Elements:**

- **Landing Page Headline:** "{{Outcome}} without {{Pain}}"
- **CTA:** "Start free trial" / "Try free for 14 days"
- **Onboarding Email 1:** Welcome + single next step
- **Upgrade Email:** "You've hit your limit — unlock more"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: Ads/SEO/Content] --> B[Landing Page]
    B --> C{Signs up?}
    C -->|Yes| D[Welcome Email]
    C -->|No| E[Retargeting]
    E --> B
    D --> F[Onboarding Flow]
    F --> G[Nurture Sequence]
    G --> H{Trial Ending}
    H --> I[Upgrade Prompt]
    I --> J{Converts?}
    J -->|Yes| K[Customer]
    J -->|No| L[Win-back Sequence]
    L --> I
```

---

### Funnel 2: Demo Request Funnel (SaaS, High-Touch)

**Best for:** SaaS products over $100/mo, sales-assisted

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Attract ICP | Ads, LinkedIn, Content | Visitors |
| Landing Page | Capture lead | Value prop, demo CTA | Demo requests |
| Qualification | Filter fit | Form fields or SDR call | Qualified leads |
| Demo | Show value | Personalized walkthrough | Demo completion |
| Proposal | Present offer | Pricing, ROI, timeline | Proposals sent |
| Close | Get signature | Negotiation, objection handling | Win rate |

**Copy Elements:**

- **Landing Page Headline:** "See how {{Company Type}} {{Achieve Outcome}}"
- **CTA:** "Book a demo" / "See it in action"
- **Confirmation Email:** "Your demo is booked — here's what to expect"
- **Follow-up Email:** "Quick recap + next steps"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: LinkedIn/Ads/Content] --> B[Landing Page]
    B --> C{Requests demo?}
    C -->|Yes| D[Qualification Form]
    C -->|No| E[Lead Magnet Path]
    E --> F[Nurture Sequence]
    F --> B
    D --> G{Qualified?}
    G -->|Yes| H[Demo Call]
    G -->|No| I[Nurture / Disqualify]
    H --> J[Proposal]
    J --> K{Closes?}
    K -->|Yes| L[Customer]
    K -->|No| M[Objection Handling]
    M --> J
```

---

### Funnel 3: Strategy Call Funnel (Agency/Services)

**Best for:** Agencies, consultants, B2B services over $2k

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Attract ICP | Content, referrals, LinkedIn | Visitors |
| Lead Magnet | Capture lead | Guide, audit, template | Opt-ins |
| Nurture | Build trust | Case studies, insights | Engagement |
| Application | Qualify interest | Application form | Applications |
| Strategy Call | Assess fit + pitch | Discovery + recommendation | Calls booked |
| Proposal | Present offer | Scope, price, timeline | Proposals sent |
| Close | Get commitment | Follow-up, negotiation | Win rate |

**Copy Elements:**

- **Lead Magnet Landing Page:** "Free {{Resource}}: How to {{Outcome}}"
- **CTA:** "Get the free guide" / "Download now"
- **Application Page:** "Apply to work with us"
- **Call Booking:** "Book your free strategy call"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: Content/LinkedIn/Referrals] --> B[Lead Magnet Page]
    B --> C{Opts in?}
    C -->|Yes| D[Nurture Sequence]
    C -->|No| E[Retargeting]
    E --> B
    D --> F[Case Study Email]
    F --> G[Application CTA]
    G --> H{Applies?}
    H -->|Yes| I[Application Review]
    H -->|No| J[Continue Nurture]
    J --> G
    I --> K{Qualified?}
    K -->|Yes| L[Strategy Call]
    K -->|No| M[Reject / Refer]
    L --> N[Proposal]
    N --> O{Closes?}
    O -->|Yes| P[Client]
    O -->|No| Q[Follow-up Sequence]
    Q --> N
```

---

### Funnel 4: Product Funnel (E-commerce, Low-Ticket)

**Best for:** E-commerce products under $100, impulse/considered

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Drive visitors | Ads, social, influencers | Visitors |
| Product Page | Convert to cart | Images, copy, reviews | Add to cart |
| Cart | Reduce abandonment | Trust signals, urgency | Cart completion |
| Checkout | Complete purchase | Simple form, payment | Conversion rate |
| Upsell | Increase AOV | Related products, bundles | Upsell rate |
| Post-Purchase | Drive repeat | Thank you, review ask, offers | Repeat rate |

**Copy Elements:**

- **Product Page Headline:** "{{Product}} — {{Key Benefit}}"
- **CTA:** "Add to cart" / "Buy now"
- **Cart Abandonment Email:** "You left something behind"
- **Post-Purchase Email:** "Your order is on the way"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: Ads/Social/Influencers] --> B[Product Page]
    B --> C{Adds to cart?}
    C -->|Yes| D[Cart Page]
    C -->|No| E[Browse Abandonment Email]
    E --> B
    D --> F{Checks out?}
    F -->|Yes| G[Order Confirmation]
    F -->|No| H[Cart Abandonment Email]
    H --> D
    G --> I[Upsell Offer]
    I --> J[Post-Purchase Sequence]
    J --> K[Review Request]
    K --> L[Repeat Purchase Offers]
```

---

### Funnel 5: Webinar Funnel (Course/Coaching, Mid-Ticket)

**Best for:** Courses, coaching, info products under $500

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Drive registrations | Ads, content, affiliates | Visitors |
| Registration | Capture lead | Webinar landing page | Registrations |
| Pre-Webinar | Increase show rate | Reminder emails | Show rate |
| Webinar | Educate + pitch | Value content + offer | Attendees |
| Offer | Convert attendees | Sales page, bonuses, urgency | Conversion |
| Follow-up | Convert non-buyers | Replay, objection emails | Late conversions |

**Copy Elements:**

- **Registration Page:** "Free Training: How to {{Outcome}} in {{Timeframe}}"
- **CTA:** "Save my seat" / "Register free"
- **Reminder Emails:** "Starting in 24 hours" / "We're live!"
- **Offer CTA:** "Join now" / "Enroll today"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: Ads/Content/Affiliates] --> B[Webinar Registration]
    B --> C{Registers?}
    C -->|Yes| D[Confirmation + Reminder Sequence]
    C -->|No| E[Retargeting]
    E --> B
    D --> F[Webinar]
    F --> G{Attends?}
    G -->|Yes| H[Pitch + Offer]
    G -->|No| I[Replay Email]
    I --> H
    H --> J{Buys?}
    J -->|Yes| K[Customer Onboarding]
    J -->|No| L[Objection Sequence]
    L --> M[Last Chance Email]
    M --> H
```

---

### Funnel 6: Application Funnel (High-Ticket Coaching/Services)

**Best for:** Coaching, mastermind, services over $2k

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Attract serious buyers | Content, ads, referrals | Visitors |
| VSL/Webinar | Build desire | Long-form video content | Watch time |
| Application | Filter serious buyers | Application form | Applications |
| Call | Close on call | Sales call | Close rate |
| Onboarding | Start engagement | Welcome, kickoff | Completion |

**Copy Elements:**

- **VSL Page:** "How {{ICP}} {{Achieve Outcome}} — Free Training"
- **Application CTA:** "Apply now" / "See if you qualify"
- **Application Form:** 5-10 qualifying questions
- **Call Booking:** "Book your enrollment call"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: Content/Ads/Referrals] --> B[VSL or Webinar]
    B --> C{Watches?}
    C -->|Yes| D[Application Page]
    C -->|No| E[Retargeting]
    E --> B
    D --> F{Applies?}
    F -->|Yes| G[Application Review]
    F -->|No| H[Follow-up Sequence]
    H --> D
    G --> I{Qualified?}
    I -->|Yes| J[Sales Call]
    I -->|No| K[Reject / Downsell]
    J --> L{Closes?}
    L -->|Yes| M[Client Onboarding]
    L -->|No| N[Objection Follow-up]
    N --> J
```

---

### Funnel 7: Local Lead Funnel (Local Service Business)

**Best for:** Local services — plumbers, dentists, gyms, etc.

**Stages:**

| Stage | Purpose | Content | Key Metric |
|-------|---------|---------|------------|
| Traffic | Local visibility | GMB, local SEO, local ads | Visitors |
| Landing Page | Capture lead | Service page, contact form | Leads |
| Follow-up | Book appointment | Call, text, email | Appointments |
| Service | Deliver value | In-person service | Completion |
| Review | Build reputation | Review request | Review rate |
| Referral | Drive word-of-mouth | Referral program | Referrals |

**Copy Elements:**

- **Landing Page:** "{{Service}} in {{Location}} — Free Quote"
- **CTA:** "Get free quote" / "Call now" / "Book online"
- **Follow-up Text:** "Thanks for reaching out! When works for a quick call?"
- **Review Request:** "How'd we do? Leave a quick review"

**Mermaid Diagram:**

```mermaid
flowchart TD
    A[Traffic: GMB/Local Ads/SEO] --> B[Landing Page]
    B --> C{Submits form?}
    C -->|Yes| D[Instant Follow-up Call/Text]
    C -->|No| E[Retargeting]
    E --> B
    D --> F{Books?}
    F -->|Yes| G[Appointment Reminder]
    F -->|No| H[Follow-up Sequence]
    H --> D
    G --> I[Service Delivered]
    I --> J[Review Request]
    J --> K[Referral Program]
    K --> L[Repeat Business Offers]
```

---

## Output Format

When generating a funnel, provide:

### 1. Funnel Overview
```
**Funnel Type:** [Name]
**Why This Fits:** [1-2 sentences explaining match]
**Goal:** [Primary conversion goal]
```

### 2. Stage Breakdown

For each stage:
```
**Stage: [Name]**
- Purpose: [What this stage does]
- Content: [What you need to create]
- Key Copy: [Headline, CTA, or email subject]
- Metric: [What to track]
```

### 3. Mermaid Diagram

Provide copy-paste ready Mermaid code that visualizes the flow.

### 4. Quick Wins (Optional)

List 2-3 immediate actions to start building the funnel.

---

## Task-Specific Questions

If context is missing and user wants quick generation, ask:

1. What do you sell? (one sentence)
2. What's the price?
3. How do people buy? (self-serve or call)
4. What's the goal? (leads, trials, sales, calls)
