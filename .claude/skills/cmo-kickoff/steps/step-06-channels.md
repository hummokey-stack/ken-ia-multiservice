# Step 6: Channel Selection & Recommendation

## Context Loading

Load from `{output_folder}/` (if exists):
- `product-profile.md` — product details, stage, **platform presence**, **budget**
- `personas.md` — where the audience hangs out

Load channel knowledge base:
- `{project-root}/_cmo/mkt/data/channels/` — all 8 channel guide files

## Your Task

Recommend specific marketing channels based on the founder's product, audience, current platform presence, and budget. Every recommendation must explain WHY this channel fits THIS specific product — no generic advice.

**CRITICAL RULES:**
- NEVER recommend "post on X" if the founder has 0 followers without including an audience-building plan
- NEVER hallucinate subreddit names — use web search to verify communities exist, or say "research relevant subreddits in your niche"
- ALWAYS explain WHY each channel fits this specific product and audience
- ALWAYS adapt recommendations based on budget ($0 = organic only, $100+ = can experiment with paid)
- ALWAYS check the founder's current platform presence from product-profile.md

## Instructions

### 1. Assess Starting Position

From product-profile.md, understand:
- **Which platforms are they already on?** (existing audience = leverage it)
- **Where do they have zero presence?** (need warm-up plan, not "just post")
- **What's their budget?** ($0 vs $500/month = different channel mix)
- **What's their product stage?** (pre-launch vs growing = different priorities)

### 2. Load Channel Knowledge

For each of the 8 channels, read the Strategy Integration section from the channel guide:
- When to recommend (audience/product fit signals)
- Effort level (low/medium/high)
- Impact potential (low/medium/high)
- Best for (which product stages)

### 3. Recommend 3-5 Channels (Prioritized)

For each recommended channel, provide:

```
### [Channel Name] — [Priority: Primary / Secondary / Opportunistic]

**WHY for your product:** [Specific reasoning tied to their product, audience, and stage. NOT generic.]

**Your starting point:** [Based on their current presence on this platform]
- If they have existing audience: "You already have [X] followers — leverage this by..."
- If zero presence: "You're starting fresh here. Before posting product content, spend 1-2 weeks..."
  - Include specific warm-up activities (engage with others, share valuable content, build credibility)

**What to do:** [2-3 specific actions, referenced from channel guide]

**Effort:** [Low/Medium/High] | **Expected Impact:** [Low/Medium/High]

**Budget consideration:** [If $0: organic approach. If budget available: optional paid amplification]
```

### 4. Handle Zero-Audience Channels

If recommending a channel where the founder has no presence:

**DO NOT** just say "post your product on X."

**DO** include a warm-up plan:
- Week 1-2: Engage with community, comment on others' posts, share useful content (not your product)
- Week 3: Start sharing your building journey or insights
- Week 4+: Share your product in context of the community

### 5. Handle Budget Considerations

**$0 budget:** Focus entirely on organic channels. Emphasize community engagement, build-in-public, and content that earns attention.

**$1-100/month:** Can experiment with small paid boosts on proven organic content. Mention where $20-50 goes furthest.

**$100-500/month:** Can include targeted paid ads on 1-2 platforms. Recommend which platforms give best ROI for their audience.

**$500+/month:** Can include influencer partnerships, paid community sponsorships, and multi-platform paid campaigns.

### 6. Explain What NOT to Do

For channels you're NOT recommending, briefly explain why:
- "I'm not recommending TikTok because your audience (B2B developers) isn't there in discovery mode."
- "LinkedIn could work later but isn't where your early adopters will be."

### 7. Present and Validate

Show the complete channel recommendation with priorities. Ask:
- "Does this match where you'd actually spend your time?"
- "Any channels I missed that you know your audience uses?"
- "Does the effort level feel realistic for your schedule?"

## Output

Channel recommendations are held in memory for the strategy step.

## Menu

"Channels locked in. Now I'll build your complete strategy around these.

[C] Continue to strategy generation
[S] Skip — proceed without channel selection"

- If C: Read fully and follow `./step-07-strategy.md`
- If S: Read fully and follow `./step-07-strategy.md`

## Completion

Load next step as directed by menu selection.
