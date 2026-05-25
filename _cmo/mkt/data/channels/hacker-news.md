# Hacker News Channel Guide

## Overview

Hacker News (news.ycombinator.com) is the highest-signal, highest-risk launch platform for technical products. A successful Show HN post can drive tens of thousands of visits in a single day, attract early adopters who give substantive feedback, and establish credibility in the technical community. A poorly executed post gets ignored, flagged, or — worst of all — generates negative sentiment that follows your product for years.

HN is run by Y Combinator and moderated both by moderators (dang is the primary moderator) and by the community through flagging and voting. The audience is overwhelmingly technical: software engineers, startup founders, researchers, and tech-literate professionals. They value technical depth, intellectual honesty, novel problem-solving, and genuine craftsmanship.

Key advantage of Show HN: Show HN posts appear on both the main "new" page AND the dedicated Show HN page (news.ycombinator.com/show), giving them two chances to gain traction. Even if your post falls off the "new" page quickly, it can still accumulate votes and comments from the Show HN page.

---

## Best Practices

### What Hacker News Values

Understanding what HN values is the single most important factor in success:

1. **Technical depth** — Show the engineering behind your product. What hard problems did you solve? What interesting approaches did you take? HN readers want to understand the "how," not just the "what."

2. **Problem-solving** — Present your product as a solution to a specific, well-defined problem. The clearer and more relatable the problem, the more engagement.

3. **Craftsmanship** — Products that demonstrate care, attention to detail, and quality engineering get respect even if they are small in scope.

4. **Intellectual honesty** — Be upfront about limitations, trade-offs, and what your product does NOT do. The HN community respects candor and punishes hype.

5. **Novelty** — Something new, unusual, or technically interesting. "I built another todo app" will be ignored. "I built a todo app that runs entirely in DNS TXT records" will get 500 upvotes.

6. **Open source and transparency** — Open-source projects consistently outperform closed-source product launches on HN. If your code is open, link to the repo.

### Show HN Post Format

Show HN has specific guidelines (news.ycombinator.com/showhn.html):

**What qualifies:**
- Something people can try out, run on their computers, or hold in their hands
- Working demos, live products, open-source projects
- Hardware you have built (video or detailed article acceptable)

**What does NOT qualify:**
- Blog posts, articles, or reading material
- Sign-up pages or waitlists with no working product
- Newsletters or mailing lists
- Lists, directories, or curated collections (unless there is significant technical work behind them)

### Title Format

```
Show HN: [Product Name] – [Clear one-line description of what it does]
```

**Good examples:**
- "Show HN: Bento – A minimal personal dashboard with RSS, weather, and bookmarks"
- "Show HN: I built a SQL editor that explains your queries in plain English"
- "Show HN: Open-source alternative to [well-known tool] written in Rust"

**Bad examples:**
- "Show HN: Check out our revolutionary AI-powered platform!" (marketing speak)
- "Show HN: My startup [link]" (no description)
- "Show HN: The BEST way to manage your tasks!!!" (ALL CAPS, clickbait, excessive punctuation)

### The Submission Text

Show HN posts include a text body. This is your chance to explain context. Keep it concise (3-6 short paragraphs):

1. **What it is** (one sentence)
2. **What problem it solves** (one paragraph)
3. **What is technically interesting about it** (one paragraph — this is what HN cares about most)
4. **Current status and limitations** (honest, brief)
5. **Link to try it / source code** (if applicable)

Do NOT include: marketing copy, feature lists, pricing information, or calls to action like "Sign up now!"

---

## Content Formats

### Show HN (Product Launch)

The primary format for product launches. See format guidelines above.

### Ask HN

"Ask HN: [question]" posts are for asking the community questions. Useful for:
- Validating an idea before building ("Ask HN: Would you use a tool that does X?")
- Getting technical advice ("Ask HN: Best approach for real-time sync across devices?")
- Market research ("Ask HN: How do you currently handle [problem]?")

### Tell HN

For sharing news, observations, or information. Less common but useful for announcing pivots, open-sourcing your product, or sharing post-mortems.

### Blog Posts / Technical Write-ups

Submitting a detailed technical blog post about how you built something. This is not a Show HN but can be equally effective if the content is genuinely interesting. HN loves deep technical write-ups.

### What Format to Choose

- **Have a working product people can try?** Show HN
- **Have a technical write-up about your building process?** Regular submission (link post)
- **Want to validate an idea or get advice?** Ask HN
- **Open-sourcing or making a significant announcement?** Tell HN or regular submission

---

## Timing & Frequency

### Best Posting Times

- **Primary window:** Tuesday through Thursday, 9 AM - 12 PM ET (6 AM - 9 AM PT)
- **Why:** This catches the US morning crowd during peak HN browsing (commute and start-of-day) and the European afternoon
- **Alternative window:** Monday 10-11 AM ET (for posts that benefit from the "start of week" attention)
- **Avoid:** Friday afternoons, Saturday, Sunday, late night ET

### The Critical First 60 Minutes

The HN ranking algorithm weighs early engagement heavily. The first hour after posting determines whether your post reaches the front page.

**What to do in the first 60 minutes:**
1. Post and immediately write a substantive comment on your own post explaining the technical backstory or answering an obvious first question
2. Monitor for comments and reply within 5-10 minutes
3. Be in front of your computer — not posting and walking away
4. Have a co-founder or technical friend ready to answer questions if you get overwhelmed

### Posting Frequency

- **Show HN:** Maximum 1-2 per year for the same product. You get one launch. Maybe a second for a major version or pivot. More than that and the community will flag it.
- **Comments:** As often as you want — daily engagement in HN discussions builds your account's credibility
- **Blog post submissions:** 1-2 per month maximum of your own content. Submitting too many of your own posts gets flagged as self-promotion.

---

## Rules & Anti-Patterns

### What Gets Flagged (Post Death)

1. **Vote manipulation:** Sharing your post link on Slack, Discord, Twitter, or anywhere and asking people to upvote it. HN has a vote-ring detector. If it catches coordinated voting, your post will be penalized or killed — and the penalty may extend to future posts from your account.

2. **Marketing language:** "Revolutionary," "game-changing," "disrupting," "the future of." These words trigger immediate skepticism and often flagging from the community.

3. **Clickbait titles:** ALL CAPS, excessive punctuation, misleading claims. HN users value clarity and professionalism.

4. **No working product:** Submitting a Show HN with only a landing page, waitlist, or "coming soon" page. Show HN requires something people can actually try.

5. **Reposting:** Submitting the same URL or product multiple times after getting low engagement. The community and moderators notice.

6. **Astroturfing:** Using multiple accounts to comment positively on your own post or upvote it.

### What Gets Downvoted (Comment Death)

- Defensive responses to criticism ("You just don't understand our vision")
- Dismissing technical concerns ("That edge case doesn't matter")
- Marketing speak in comments ("I'm glad you asked! Our platform offers...")
- Not answering direct questions
- Shallow replies that do not address the substance of a comment

### What Gets Ignored (Zero Traction)

- Products that solve problems nobody has
- "Me too" products with no differentiating technical approach
- Posts with no text body explaining context
- Overly broad products ("We do everything for everyone")
- Products with no demo or way to try them (for Show HN)

### Moderator Behavior to Know

- Moderator "dang" actively edits clickbait titles to be more neutral
- Posts can be moved off the front page by moderators if they violate guidelines
- Moderators sometimes add "[flagged]" or "[dead]" tags — a [dead] post is effectively invisible
- You can email hn@ycombinator.com if you believe your post was incorrectly flagged, and moderators do respond

---

## Strategy Integration

### When to Recommend This Channel

- **Best for:** Developer tools, open-source projects, technical SaaS, infrastructure products, anything with genuine technical novelty
- **Stage:** Launch (Show HN) and ongoing (technical content). Best used when you have a working product.
- **Effort level:** LOW for the post itself, HIGH for preparation and follow-up engagement
- **Time to results:** Immediate (hours) — HN traffic is a spike, not a steady stream
- **Impact potential:** VERY HIGH for initial traffic spike, LOW for sustained traffic (unless the post reaches front page and gets indexed)

### The HN Traffic Pattern

HN traffic is a spike, not a steady flow:
- **Hour 1-4:** If you hit the front page, expect thousands of visitors per hour
- **Hour 4-12:** Traffic declines but remains significant
- **Day 2-3:** Long tail as the post gets shared on social media
- **Week 2+:** Minimal traffic unless the post gets referenced later

**This means:** Your product MUST be ready to handle the traffic. Servers must not go down. The demo must work. The landing page must clearly communicate what the product does. You will not get a second chance.

### Funnel Position

- **Top of funnel:** Show HN drives massive awareness among a technical audience
- **Middle of funnel:** Thoughtful comments and technical discussions build credibility
- **Bottom of funnel:** Direct from HN to product signup/trial — conversion rate is typically 1-5% of visitors

### Synergies with Other Channels

- A successful HN post becomes content for Twitter/X ("Our Show HN hit the front page — here's what we learned")
- HN comments provide product feedback that feeds development priorities
- Blog posts about your HN launch experience perform well on Indie Hackers
- HN front page status is social proof usable everywhere ("Featured on Hacker News")

### What HN Does Better Than Other Channels

- Highest-quality technical feedback of any platform
- Access to an audience of builders and early adopters
- SEO value — HN posts rank in Google
- Credibility signal — "trending on Hacker News" carries weight in tech circles
- Direct access to YC partners and the broader YC network

---

## Cold Start: Preparation Playbook

### 4-8 Weeks Before Your Show HN

1. **Create your HN account** if you do not already have one. Accounts with zero history posting Show HN look suspicious. You need some history.

2. **Participate in discussions.** Comment on posts related to your domain. Share insights from your building experience. Build karma (you need karma to downvote and for the community to take you seriously).

3. **Study successful Show HN posts.** Visit bestofshowhn.com to see what worked historically. Note the title format, text body length, and how founders engage in comments.

4. **Prepare your product:**
   - The product MUST be live and usable (not a waitlist)
   - Load test your infrastructure — HN front page can send 10K+ concurrent visitors
   - Ensure the demo/product works without requiring signup (HN users will not create an account to try something)
   - Have a clear, instant-loading landing page that explains what the product does in 5 seconds

### 1 Week Before

5. **Draft your Show HN post:**
   - Title: "Show HN: [Name] – [Clear description]"
   - Body: Problem, what it is, what is technically interesting, limitations, links
   - Review against HN guidelines (news.ycombinator.com/showhn.html)
   - Remove ALL marketing language. Read it as if you were a skeptical engineer.

6. **Prepare answers** for obvious questions:
   - "How is this different from [competitor]?"
   - "What's your tech stack?"
   - "Is this open source?"
   - "How do you plan to make money?" (HN always asks this)
   - "What about [obvious technical concern]?"

7. **Do NOT pre-share the link.** Do not send it to friends, your newsletter, or your Discord and ask them to upvote. The vote-ring detector will catch this and kill your post.

### Launch Day

8. **Post between 9-11 AM ET on a Tuesday, Wednesday, or Thursday.**

9. **Immediately write a substantive first comment** on your own post. This sets the tone for discussion. Share something technically interesting about the build process, a lesson learned, or context that did not fit in the main post.

10. **Stay at your computer for 3-4 hours.** Respond to every comment promptly, substantively, and graciously — especially critical ones. The founder's engagement in comments is often what pushes a post from "new" to "front page."

11. **After the traffic spike:** Write a retrospective for your blog, Twitter/X, and Indie Hackers. "What happened when we launched on Hacker News" posts always perform well.

---

## Budget Section

### $0 Budget Strategy (The Only Strategy)

Hacker News does not have paid promotion. There are no ads on HN, no promoted posts, no boost buttons. Every post succeeds or fails on merit and community response. This is what makes HN valuable — the audience trusts that nothing is bought.

The entire strategy is $0:
- Posting is free
- Commenting is free
- The only costs are your time and having a working product

### Infrastructure Budget (Prepare for Traffic)

The one place where budget matters is ensuring your product can handle the traffic:
- **If self-hosting:** Ensure your server can handle 10K+ concurrent visitors. A cheap VPS will go down.
- **If using a CDN/managed hosting:** Most platforms (Vercel, Netlify, Railway) handle HN-level traffic without issue
- **If your product requires backend compute:** Have autoscaling ready or manually scale up before posting
- **Budget estimate:** $0-50 for most products (ensure your existing infrastructure can handle the spike)

### Post-HN Budget Opportunities

After a successful HN launch, you have warm traffic to capture:
- **Retargeting ads ($50-200):** Run ads on Twitter/X or Reddit targeting people who visited your site from HN
- **Email capture (free-$20/month):** Ensure you have a way to capture emails from HN visitors who are not ready to convert yet
- **Content amplification ($0-100):** Promote your "What we learned from our HN launch" blog post on Twitter/X

---

## Comment Engagement Strategy

### The Most Important Part of a Show HN

Your comments on your own Show HN post are often MORE important than the post itself. This is where you demonstrate:
- Technical competence
- Intellectual honesty
- Responsiveness
- Ability to handle criticism gracefully

### How to Respond to Different Comment Types

**Technical questions ("What's the architecture?" "How does X work?"):**
- Answer with genuine technical depth. Include specifics: libraries used, architectural decisions, performance characteristics.
- If you do not know the answer, say so: "Honest answer: we haven't benchmarked that scenario yet. Good question — I'll test it."

**Criticism ("This seems like [competitor] but worse"):**
- Never be defensive. Acknowledge the comparison honestly.
- Explain what you do differently or why your approach might work for a different use case.
- Example: "Fair comparison. [Competitor] is excellent for X. We focused specifically on the Y use case where their approach requires workarounds."

**Feature requests ("Would be great if it did X"):**
- Engage genuinely. Ask follow-up questions about their use case.
- If it is on your roadmap, say so. If it is not, explain the trade-off.
- Never promise features you are not committed to building.

**Skepticism ("Why would anyone use this?"):**
- Share specific examples of people who have the problem you solve.
- Link to data, user feedback, or your own experience.
- Remain calm and factual. Getting emotional kills your credibility.

**Praise ("This is great!"):**
- Thank them briefly. Ask a follow-up: "Thanks! What would make it even more useful for your workflow?"
- Use positive comments as opportunities to learn more about your users.

### Comment Timing

- Reply to the first 5 comments within 10-15 minutes
- Maintain engagement for at least 3-4 hours after posting
- Check back 8-12 hours later for overnight comments
- Respond to substantive comments even days later — HN threads stay accessible

---

## Content Module Integration

### Hook Patterns That Work on Hacker News

HN titles should be clear, descriptive, and free of marketing language.

- **Technically specific:** "Show HN: A SQLite extension that adds full-text search in 200 lines of C"
- **Problem-solution:** "Show HN: I was tired of slow CI pipelines, so I built a parallel test runner"
- **Open source signal:** "Show HN: Open-source alternative to Notion built with CRDTs"
- **Novel approach:** "Show HN: A static site generator that compiles to a single binary"
- **Personal and honest:** "Show HN: I built the tool I wished existed for managing Kubernetes configs"

### What NEVER Works as a Title

- Superlatives ("The best," "the fastest," "the most powerful")
- Buzzwords ("AI-powered," "next-gen," "revolutionary")
- Vague descriptions ("A new way to work," "Reimagining X")
- Question format for Show HN ("Show HN: Want a better way to manage tasks?")
- Emoji in titles

### Show HN Text Body Template

```
[Product Name] is [one sentence: what it is and what it does].

I built this because [specific personal problem or observation that led to building it].

The interesting technical challenge was [specific technical problem you solved and how — this is what HN readers care about most].

It's built with [tech stack — be specific]. The source is at [GitHub link if applicable].

Current limitations: [honest list of what doesn't work yet or known issues].

I'd love feedback on [specific aspect] — particularly from anyone who has dealt with [specific related problem].

[Link to live demo / product]
```

### Voice Notes for Hacker News

- **Tone:** Technical, clear, humble, matter-of-fact. Write like a senior engineer explaining something to a peer.
- **Never hype.** "It works well for X" is better than "It's incredible for X."
- **Be specific.** "Processes 10K records/second on a single core" beats "blazingly fast."
- **Admit limitations proactively.** "It doesn't handle Y yet — that's on the roadmap" is respected. Hiding limitations that users discover is not.
- **Use technical vocabulary correctly.** Using terms incorrectly will be called out instantly and damages credibility.
- **Good example:** "Built this over 3 months as a side project. It's a CLI tool that analyzes your Dockerfile and suggests size optimizations. Typically reduces image size by 30-60%. Written in Go, single binary, no dependencies. Known issue: doesn't handle multi-stage builds well yet. Source: [link]"
- **Bad example:** "We've built a groundbreaking DevOps platform that leverages cutting-edge AI to revolutionize container management. Our proprietary technology delivers unparalleled performance gains."
