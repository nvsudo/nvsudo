---
# METADATA (Machine-readable - Do not edit manually unless you know YAML)
project: "project-name"
created_at: "YYYY-MM-DD"
updated_at: "YYYY-MM-DD"
current_stage: "idea_validation" # idea_validation | market_research | mvp_scoping | building | launching | live
confidence_level: "low" # low | medium | high
next_agent: "research_agent" # research_agent | mvp_scoping_agent | cto_agent | launch_agent
priority_focus: [] # List of high-priority items to focus on next
---

# {{project_name}} - Knowledge Base

**Last Updated:** {{updated_at}}
**Current Stage:** {{current_stage}}
**Overall Confidence:** {{confidence_level}}

---

## Idea

**Summary:**
_2-sentence elevator pitch: What is this? Who is it for?_

**Problem Statement:**
_What problem are you solving? For whom? How painful is it?_

**Proposed Solution:**
_How does your solution solve this problem? What's unique about your approach?_

**Target Customer:**
_Be specific: "Solo founders building side projects" NOT "everyone"_

**Type of Play:**
_Data aggregation | Network effects | Process improvement | Distribution | Marketplace | SaaS tool | Other_

### Core Components

```yaml
problem: "Brief problem statement"
solution: "Brief solution statement"
target_customer: "Specific customer segment"
type_of_play: "data_aggregation" # or network_effects, process_improvement, etc.
value_proposition: "What do users get that they can't get elsewhere?"
```

**Narrative Context:**
_Explain the idea in more detail. Why now? Why you? What's your unfair advantage?_

### Info Gaps (Idea)

```yaml
- question: "What's the ONE core problem we're solving?"
  status: unknown # unknown | in_progress | answered
  assigned_to: idea_validator_agent
  priority: high # high | medium | low
  answer: null
  source: null
  confidence: null

- question: "Who is the target customer (specific segment)?"
  status: unknown
  assigned_to: idea_validator_agent
  priority: high
  answer: null
```

---

## Value Creation

**For Customers:**
_What do they get? How does this make their life better?_

**For the Business:**
_What's the moat? Data? Network effects? Brand? Switching costs?_

**For Other Stakeholders:**
_(If applicable: e.g., brands, suppliers, partners)_

### Stakeholder Map

```yaml
customers:
  segment: "Solo founders, indie hackers"
  get: "Honest idea validation without paying $200 consultant"
  pay: "$15 per validation"
  alternative: "ChatGPT (free but useless), Reddit (slow), consultant ($200)"

business:
  revenue_model: "Per-validation fee ($15)"
  moat: "Proprietary validation framework, brand trust"
  data_capture: "Validation data = market intelligence"

other_stakeholders: []
```

---

## Assumptions

_What needs to be true for this to work? List all critical assumptions and track their validation status._

```yaml
- id: a1
  assumption: "Target customers will pay $X for this solution"
  evidence_tier: 4 # 1 (payment) | 2 (behavior) | 3 (stated intent) | 4 (hypothesis)
  status: unvalidated # unvalidated | validating | validated | invalidated
  priority: high # high | medium | low
  validation_method: "Landing page test with pricing"
  estimated_cost: "$100 (ad spend)"
  estimated_time: "1 week"
  info_gaps:
    - "What's willingness to pay?"
    - "What do competitors charge?"
  blockers: []

- id: a2
  assumption: "We can acquire customers via [channel]"
  evidence_tier: 4
  status: unvalidated
  priority: high
  validation_method: "Post in 3 communities, measure click-through"
  info_gaps:
    - "Which communities have our target customers?"
    - "What messaging resonates?"

- id: a3
  assumption: "We can build MVP in X weeks"
  evidence_tier: 4
  status: unvalidated
  priority: medium
  validation_method: "Tech stack research + prototype"
  info_gaps:
    - "What's the simplest tech stack?"
    - "What's the core feature set?"
```

**Narrative - Riskiest Assumptions:**
_Which 1-2 assumptions are most likely to kill this idea? Why? What's the plan to validate them?_

---

## Market

### Market Size

```yaml
tam: null # Total Addressable Market
sam: null # Serviceable Addressable Market
som: null # Serviceable Obtainable Market (realistic first year)
growth_rate: null
trends: []
```

**Narrative:**
_Estimated market size and growth trends. Is this growing or shrinking? Why?_

### Competitors

```yaml
competitors:
  - name: "Competitor A"
    url: "https://..."
    pricing: "Free / $X per month"
    strengths: ["Fast", "Accessible", "Trusted brand"]
    weaknesses: ["Too generic", "No personalization", "Expensive"]
    market_position: "Market leader"
    founded: "2020"
    funding: "$XM Series A"

  - name: "Competitor B"
    url: "https://..."
    pricing: "$X-Y"
    strengths: []
    weaknesses: []
    market_position: "Niche player"
```

**Competitive Landscape Summary:**
_Who dominates? What are they missing? Where's the gap? What's your wedge?_

**Competitive Advantage:**
```yaml
our_wedge: "What we do that no one else does (or does well)"
why_now: "Why is this the right time to build this?"
defensibility: "What prevents others from copying us?"
```

### Info Gaps (Market)

```yaml
- question: "Who are the top 5-10 direct competitors?"
  status: unknown
  assigned_to: research_agent
  priority: high

- question: "What's the estimated TAM/SAM/SOM?"
  status: unknown
  assigned_to: research_agent
  priority: medium

- question: "What do users love/hate about competitors?"
  status: unknown
  assigned_to: research_agent
  priority: high
  source_hint: "Scrape reviews on G2, Capterra, Reddit, App Store"
```

---

## Customer Intelligence

**Where They Hang Out:**
_Reddit subs, Twitter hashtags, Discord servers, forums, conferences, etc._

```yaml
communities:
  - platform: "Reddit"
    location: "r/startups, r/entrepreneur"
    size: "2M+ members"
    engagement: "High"

  - platform: "Twitter"
    location: "#indiehackers, #buildinpublic"
    size: "Unknown"
    engagement: "Medium"
```

**What They Complain About:**
_Common pain points, frequently asked questions, unmet needs_

**Language & Messaging:**
_How do they describe their problem? What words do they use? What resonates?_

### Info Gaps (Customers)

```yaml
- question: "Where do target customers hang out online?"
  status: unknown
  assigned_to: research_agent
  priority: high

- question: "What are the top 5 pain points they discuss?"
  status: unknown
  assigned_to: research_agent
  priority: high
  source_hint: "Scrape Reddit threads, Twitter complaints, forum posts"

- question: "What language/phrases do they use to describe the problem?"
  status: unknown
  assigned_to: research_agent
  priority: medium
  use_case: "Marketing copy, landing page headlines"
```

---

## Technical Intelligence

**Tech Stack Recommendations:**

```yaml
tech_stack:
  frontend: null # e.g., Next.js, React, Vue
  backend: null # e.g., Next.js API routes, Express, FastAPI
  database: null # e.g., Postgres, Supabase, Firebase
  hosting: null # e.g., Vercel, Railway, AWS
  payments: null # e.g., Stripe, Paddle
  ai: null # e.g., OpenAI API, Anthropic API
  rationale: "Why this stack? (Speed? Cost? Familiarity?)"
```

**Build Complexity:**

```yaml
estimated_build_time: null # e.g., "1 week", "2-4 weeks", "3 months"
technical_risks: [] # e.g., "Scaling AI API costs", "Real-time data sync"
build_vs_buy: [] # e.g., "Use Stripe for payments (don't build)"
```

### Info Gaps (Technical)

```yaml
- question: "What tech stack do similar products use?"
  status: unknown
  assigned_to: research_agent
  priority: medium
  source_hint: "Check BuiltWith, StackShare, job postings"

- question: "What's the fastest way to build an MVP?"
  status: unknown
  assigned_to: mvp_scoping_agent
  priority: high
```

---

## Distribution & Go-to-Market

**Channels:**

```yaml
channels:
  - name: "Reddit"
    cost: "Free"
    effort: "Low"
    timeline: "Immediate"
    expected_reach: "100-500 impressions"
    conversion_estimate: "5-10%"

  - name: "SEO / Content"
    cost: "$0"
    effort: "High"
    timeline: "3-6 months"
    expected_reach: "1000+ organic visits/month"

  - name: "Paid Ads (Google/Twitter)"
    cost: "$500-1000/month"
    effort: "Medium"
    timeline: "Immediate"
    expected_reach: "5000+ impressions"
```

**How Competitors Acquired Users:**
_Case studies, founder interviews, what worked/failed?_

**Viral/Word-of-Mouth Potential:**
_Is this shareable? Do users refer others? Built-in virality?_

### Info Gaps (Distribution)

```yaml
- question: "How did top 3 competitors get their first 100 users?"
  status: unknown
  assigned_to: research_agent
  priority: high
  source_hint: "Founder interviews, Indie Hackers case studies"

- question: "Which distribution channels work best for this customer segment?"
  status: unknown
  assigned_to: research_agent
  priority: high

- question: "What content goes viral in our target communities?"
  status: unknown
  assigned_to: research_agent
  priority: medium
  use_case: "Launch strategy, content marketing"
```

---

## Pricing & Monetization

**Pricing Model:**

```yaml
pricing:
  model: null # e.g., "Per-use", "Subscription", "Freemium", "Marketplace fee"
  tiers:
    - name: "Free"
      price: "$0"
      features: []
      target: "Try before buy, build trust"

    - name: "Single Use"
      price: "$15"
      features: ["1 validation"]
      target: "First-time users"

    - name: "3-Pack"
      price: "$40"
      features: ["3 validations", "Save $5"]
      target: "Serial ideators"

    - name: "Unlimited"
      price: "$50/month"
      features: ["Unlimited validations", "Priority support"]
      target: "Active founders iterating fast"
```

**Competitive Pricing:**

```yaml
competitor_pricing:
  - competitor: "ChatGPT"
    pricing: "Free"

  - competitor: "YC Feedback Services"
    pricing: "$200-500 one-time"

  - competitor: "Consultant"
    pricing: "$200-500 per session"
```

**Willingness to Pay Signals:**
_What do users say in reviews/forums about pricing? What would they pay?_

### Info Gaps (Pricing)

```yaml
- question: "What do competitors charge?"
  status: unknown
  assigned_to: research_agent
  priority: high

- question: "What's the willingness to pay for this solution?"
  status: unknown
  assigned_to: research_agent
  priority: high
  source_hint: "Reddit threads, reviews mentioning price"

- question: "What pricing model works best (per-use vs. subscription)?"
  status: unknown
  assigned_to: research_agent
  priority: medium
```

---

## Decisions

_Key decisions made during the journey. Track what was decided, why, and confidence level._

```yaml
- question: "What's the target customer segment?"
  answer: "Solo founders and indie hackers (not enterprise)"
  decided_by: "founder"
  decided_at: "2025-10-08"
  confidence: "high" # low | medium | high
  based_on: ["idea_validation", "founder_intuition"]
  alternative_considered: "Enterprise customers"
  why_rejected: "Too long sales cycle, different pain points"

- question: "What's the pricing model?"
  answer: "$15 single, $40 3-pack, $50/month unlimited"
  decided_by: "founder"
  decided_at: "2025-10-08"
  confidence: "medium"
  based_on: ["competitive_analysis", "founder_intuition"]
  needs_validation: true
  validation_method: "Landing page A/B test ($10 vs $15 vs $20)"
```

---

## Metrics & Success Criteria

**North Star Metric:**
_The ONE metric that matters most. E.g., "Monthly revenue", "Active users", "Retention rate"_

**Success Criteria by Stage:**

```yaml
validation_stage:
  - metric: "Email signups"
    target: "50+ in 1 week"
    actual: null

  - metric: "Completed validations (free beta)"
    target: "20+ in 2 weeks"
    actual: null

  - metric: "Would pay $15 (survey)"
    target: "50%+ say yes"
    actual: null

launch_stage:
  - metric: "Paid validations"
    target: "20+ in first month"
    actual: null

  - metric: "Conversion rate (visitor → paying)"
    target: "5%+"
    actual: null

  - metric: "Helpful rating"
    target: "80%+"
    actual: null

growth_stage:
  - metric: "Monthly revenue"
    target: "$1000+ by month 2"
    actual: null
```

---

## Risks & Mitigations

```yaml
- risk: "AI output quality is inconsistent"
  impact: "high" # low | medium | high
  probability: "medium" # low | medium | high
  mitigation: "Manual review of first 50 reports, quality checks, prompt versioning"
  status: "mitigated"

- risk: "No one will pay $15"
  impact: "high"
  probability: "low"
  mitigation: "Run landing page test before building, offer refunds"
  status: "monitoring"

- risk: "Distribution is harder than expected"
  impact: "high"
  probability: "medium"
  mitigation: "Test 3 channels (Reddit, SEO, paid) in parallel"
  status: "unmitigated"
  blocker: "Need market research to identify best channels"
```

---

## Next Steps & Action Items

**Immediate Next Steps (This Week):**

```yaml
- action: "Complete market research"
  assigned_to: "research_agent"
  deadline: "2025-10-10"
  status: "in_progress"
  blockers: []

- action: "Define MVP scope (core feature set)"
  assigned_to: "mvp_scoping_agent"
  deadline: "2025-10-12"
  status: "blocked"
  blockers: ["Waiting on market research"]
  dependencies: ["market_research"]
```

**Upcoming Milestones:**

```yaml
- milestone: "MVP Built & Deployed"
  target_date: "2025-10-20"
  status: "not_started"

- milestone: "First Paying Customer"
  target_date: "2025-10-25"
  status: "not_started"

- milestone: "$1K MRR"
  target_date: "2025-11-30"
  status: "not_started"
```

---

## Agent Activity Log

_Chronological log of agent actions and outputs._

```yaml
- date: "2025-10-07"
  agent: "idea_validator_agent"
  action: "Stress-tested idea, identified riskiest assumptions"
  output: "idea-validation.md"
  key_findings:
    - "Riskiest assumption: Distribution (will consumers find/use this?)"
    - "Evidence tier: 4 (hypothesis only)"
    - "Type of play: Data aggregation"
  info_gaps_created: 5
  info_gaps_filled: 0

- date: "2025-10-08"
  agent: "research_agent"
  action: "Market research (in progress)"
  output: "research.md"
  status: "in_progress"
  eta: "2025-10-10"
```

---

## Appendix

### Glossary

- **Evidence Tier 1:** Payment (someone paid money)
- **Evidence Tier 2:** Behavior (observed action, not just words)
- **Evidence Tier 3:** Stated Intent ("I would pay for this")
- **Evidence Tier 4:** Hypothesis (founder assumption, no validation)

### Related Documents

- [Idea Validation Report](./idea-validation.md)
- [Market Research Report](./research.md)
- [MVP Scoping Doc](./mvp-scope.md)

---

**Status Summary:**
- **Stage:** {{current_stage}}
- **Confidence:** {{confidence_level}}
- **Next Agent:** {{next_agent}}
- **Open Info Gaps:** {{count_open_info_gaps}}
- **Unvalidated Assumptions:** {{count_unvalidated_assumptions}}
- **Blockers:** {{count_blockers}}
