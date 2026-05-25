# Step 7: Strategy Generation

## Context Loading

Load from `{output_folder}/` (if exists):
- `product-profile.md` — product, stage, platform presence, budget
- `personas.md` — audience details
- `voice-profile.md` — communication style

Load channel knowledge base (for recommended channels):
- `{project-root}/_cmo/mkt/data/channels/` — relevant channel guide files

Also available in memory from previous steps:
- Positioning statement and core messages (from step-05)
- Channel recommendations with WHY reasoning (from step-06)

## Your Task

Generate a complete, tailored marketing strategy that the founder reads and thinks "wow, this really understands my product." Every recommendation must be specific to THIS product — no generic advice. The strategy must account for the founder's starting position (audience size, budget, stage).

**CRITICAL RULES:**
- Every recommendation must explain WHY it fits this specific product and audience
- Reference the channel knowledge base for specific tactics — don't make them up
- If the founder has zero audience on a recommended channel, include audience-building phase BEFORE product marketing
- Adapt ALL recommendations based on budget ($0 = organic strategies only)
- Never suggest subreddits, communities, or influencers without verifying they exist (use web search or say "research communities in [niche]")
- Strategy must be actionable — not "increase brand awareness" but "write 3 tweets per week about [specific topic] because [reason]"

## Instructions

### 1. Synthesize All Context

Review everything gathered so far:
- Product details and differentiator
- Target personas and their pain points
- Voice profile
- Positioning and core messages
- Recommended channels with priorities
- Current platform presence (critical — this determines what's realistic)
- Budget (critical — this determines what's possible)

### 2. Generate Strategy Document

Structure the strategy around the recommended channels. For each channel:

```
## [Channel Name]

**Why this channel for [product_name]:** [Specific reasoning tied to product + audience, NOT generic]

**Your starting position:** [Based on actual platform presence from product-profile]
[If zero audience: include warm-up plan before product marketing]
[If existing audience: how to leverage what you have]

**Strategy:**
[Phase 1: If zero audience — audience building (2-4 weeks)]
[Phase 2: Content strategy — what to post, what topics, what format]
[Phase 3: Product marketing — how to introduce your product authentically]

**Specific tactics:**
1. [Specific, actionable tactic with reasoning from channel guide]
2. [Specific, actionable tactic with reasoning from channel guide]
3. [Specific, actionable tactic with reasoning from channel guide]

**Content themes for YOUR product:**
- [Theme tied to specific persona pain point]
- [Theme tied to product differentiator]
- [Theme tied to building journey / authenticity]

**What to avoid:**
- [Channel-specific anti-patterns from channel guide]
```

### 3. Add Cross-Channel Strategy

After individual channels:
- How channels work together (e.g., "repurpose IH journey post into Twitter thread")
- Content calendar overview (what goes where, when)
- How to measure what's working (specific metrics per channel)

### 4. Add AI SEO/GEO Section

If relevant to the product:
- How to appear in AI-assisted search results
- Specific pages to create (comparison pages, FAQ pages)
- How to structure content for AI citation
- Reference the ai-seo-geo.md channel guide

### 5. Validate with Founder

Present strategy and ask:
- "Does this feel achievable with your current time and budget?"
- "Any tactics that feel off for your product?"
- "Anything missing that you know works for your audience?"

### 6. Save Strategy

Copy template from `../templates/strategy.template.md` to `{output_folder}/strategy.md`.
Populate with complete strategy. Update frontmatter with `product_stage` and `channels_recommended`.

## Output

Creates `{output_folder}/strategy.md` with complete, tailored marketing strategy.

## Menu

"Strategy saved! Now let's break this into tasks you can start on today.

[C] Continue to task breakdown
[S] Skip tasks — keep the strategy as-is"

- If C: Read fully and follow `./step-08-tasks.md`
- If S: Read fully and follow `./step-08-tasks.md`

## Completion

Load next step as directed by menu selection.
