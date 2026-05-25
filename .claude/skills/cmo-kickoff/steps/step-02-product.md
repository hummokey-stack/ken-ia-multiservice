# Step 2: Product Analysis

## Context Loading

- Config loaded from step-01 (product_name, user_name available)
- Alex persona active

## Your Task

Deeply understand the founder's product — what it does, who it's for, what makes it different, and what stage it's at. This is the foundation everything else builds on. If this step doesn't nail the product understanding, every subsequent step will generate generic output.

## Instructions

### 1. Ask for Product Info

"Let's get to know your product. You can share it any way that works for you:

- **Paste a URL** — I'll analyze your landing page or site
- **Describe it** — just tell me what it does in your own words
- **Point me to docs** — if you have a README or docs I can read
- **Check out the codebase** — I'm in your project folder, so I can explore the code directly and understand your product from the source

Whatever's easiest for you."

### 2. Analyze Product Info

**If URL provided:**
- Analyze the URL content to extract: product name, what it does, who it's for, value proposition, pricing (if visible), competitive positioning
- Present your understanding back to the founder

**If description provided:**
- Extract what you can from their description
- Note what's missing for a complete product profile

**If docs/README provided:**
- Read the document fully
- Extract product details

**If codebase option chosen:**
1. Read README.md (or README) at project root
2. Read package.json, Cargo.toml, pyproject.toml, go.mod, or equivalent to identify tech stack
3. List top-level directory structure
4. Search for landing pages and marketing-related files: glob for `**/index.html`, `**/landing*`, `**/pages/**`, `**/app/**`, `**/public/**`
5. Read key source files to understand what the product does — focus on routes, pages, and main components, not utility code
6. Extract: product name, what it does, who it's for, value proposition, tech stack, key pages/components, landing page file paths
7. Present understanding back to the founder (same flow as URL/description)

**Important:** Don't try to read the entire codebase. Focus on: README → package manifest → pages/public directories → landing page content. Stop once you understand the product.

### 2b. Code Change Settings (Only if codebase option was chosen)

"Since I can see your codebase, I can help with marketing tasks that involve code changes — like updating landing page copy, adding social sharing buttons, or improving meta tags.

**How should I handle code changes?**

[1] **Always ask first** — I'll show you what I want to change and you decide
[2] **Never touch the code** — I'll give you step-by-step instructions instead
[3] **Just make the changes** — go ahead and do it, show me what you changed after

And for git:

[A] **Don't commit** — make changes but I'll handle git myself
[B] **Commit only** — commit changes but don't push
[C] **Commit and create a PR** — push to a new branch and create a pull request"

Save selections to config.yaml as `code_change_mode` and `git_mode`.

If the user doesn't want to decide now, default to `always-ask` and `never-commit` — safest options.

### 3. Ask Follow-Up Questions

After initial analysis, check for gaps. Ask targeted follow-up questions for anything missing or vague:

- **If value prop is unclear:** "I can see what your product does, but help me understand — what's the ONE thing that makes someone choose this over alternatives? What's the 'aha' moment?"
- **If audience is vague:** "Who's using this right now? Or if you haven't launched yet, who do you imagine using it? Be as specific as you can — 'developers' is too broad, 'freelance web developers tired of invoicing' is perfect."
- **If stage is unclear:** "Where are you at with this? Pre-launch (still building), just launched (first users), or growing (have users, want more)?"
- **If differentiator is missing:** "What do people currently use instead of your product? And what's frustrating about those alternatives?"

Don't ask all of these at once. Ask the 2-3 most relevant based on what's missing.

### 4. Detect Product Stage

Based on their answers, classify the product stage:
- **pre-launch** — still building or about to launch, no real users yet
- **just-launched** — recently shipped, early users, figuring out distribution
- **growing** — has users/revenue, wants to scale

This matters because strategy recommendations differ significantly by stage.

### 5. Understand Their Current Reach & Budget

These two questions fundamentally change the strategy, so ask them now:

**Platform presence:**
"Quick question about your current online presence — are you active on any of these platforms? And roughly how many followers/connections do you have?

- Twitter/X: [active / have account / don't have one] — followers?
- Reddit: [active / lurker / don't use it]
- LinkedIn: [active / have profile / don't use it] — connections?
- TikTok/Instagram: [active / nah]
- Email list: [have one / no]
- Any communities you're part of? (Discord, Slack, forums)

It's totally fine if the answer is 'zero everywhere' — most founders start from scratch. I just need to know so I don't tell you to 'post on X' when you have 3 followers. Different starting points need different strategies."

**Marketing budget:**
"And budget — how much are you willing to spend on marketing per month?

- $0 (free only — my time is my investment)
- Low ($1-100/month — some small experiments)
- Medium ($100-500/month — willing to invest in what works)
- More ($500+/month)

No wrong answer here. Most indie hackers start at $0 and that's completely fine — some of the best marketing is free. I just want to know if paid options (ads, influencer partnerships, etc.) are on the table."

### 6. Confirm Understanding

Present your product analysis back to the founder:

"Here's what I understand about [product_name]:

**What it does:** [one paragraph summary]
**Who it's for:** [specific audience]
**What makes it special:** [key differentiator]
**Stage:** [pre-launch / just-launched / growing]
**Current reach:** [platform presence summary — highlight if starting from zero]
**Budget:** [budget level]
**Current situation:** [what they've tried, where they are]

Does this capture your product accurately? Anything I'm missing or getting wrong?"

Let them correct or add context until they confirm.

### 7. Save Product Profile

Copy template from `../templates/product-profile.template.md` to `{output_folder}/product-profile.md`.

Populate with:
- Frontmatter: `product_name`, `product_url` (if provided), `product_stage`, `created_at`
- Body sections: Product Overview, Value Proposition, Target Audience Signals, Competitive Positioning, Current Platform Presence (with follower counts), Marketing Budget

## Output

Creates `{output_folder}/product-profile.md` with complete product analysis.

## Menu

"Great — I've saved your product profile. This is the foundation everything else builds on.

[C] Continue to audience & personas
[S] Skip — I'll work with what I have"

- If C: Read fully and follow `./step-03-audience.md`
- If S: Read fully and follow `./step-03-audience.md` (no artifact created, downstream steps adapt)

## Completion

Update config.yaml with `product_name`, `product_url`, `product_stage` if not already set. Then load next step as directed by menu selection.
