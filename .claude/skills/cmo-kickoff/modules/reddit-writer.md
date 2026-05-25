# Reddit Post Writer Module

## Context Loading

Load ALL of these before generating any content:
- `{output_folder}/product-profile.md` — product details, value prop, audience
- `{output_folder}/voice-profile.md` — founder's voice characteristics and anti-patterns
- `{output_folder}/strategy.md` — Reddit section for strategic context
- `{project-root}/_cmo/mkt/data/channels/reddit.md` — subreddit rules, posting best practices, anti-spam guidelines
- **CRITICAL:** `{project-root}/_cmo/mkt/data/writing-quality.md` — writing rules and banned phrases. Every sentence MUST pass these rules.

## Your Task

Generate Reddit posts tailored to specific subreddit conventions and rules. Reddit has zero tolerance for marketing that smells like marketing. The post must provide genuine value and sound like a real community member sharing something useful.

## Instructions

### 1. Understand the Task

Read the task description. Determine:
- Which subreddit (or ask the founder if not specified)
- What type of post? (I built this, journey/story, feedback request, resource/guide, question)
- What's the goal? (awareness, feedback, signups, community engagement)

### 2. Verify the Subreddit

**NEVER guess or invent subreddit names.**

If the task names a specific subreddit:
- Verify it's a real, well-known subreddit (r/SideProject, r/startups, r/Entrepreneur, r/webdev, r/programming, etc.)
- If you're not confident it exists, say: "I'm not sure r/[name] exists. Search Reddit to verify before posting."

If no subreddit is specified:
- Suggest 2-3 well-known subreddits from the reddit.md channel guide that fit the product
- Say: "Research your niche subreddits using Reddit search before posting. These large communities are safe starting points."

### 3. Load Subreddit Context

From reddit.md, reference:
- Which subreddits explicitly allow self-promotion
- Which have designated promotion threads (Feedback Friday, etc.)
- The 90/10 rule (90% value, 10% product)
- What gets you banned, removed, or downvoted
- Post structure template

### 4. Apply Writing Quality Rules

From writing-quality.md, enforce ALL rules:
- NO banned phrases (scan every sentence)
- NO corporate speak, marketing language, or AI tells
- Use contractions, be specific, be human
- NO em dashes
- NO "This isn't X. This is Y." pattern
- Humor from specificity
- Hedging is human ("I think," "probably," "kinda")

### 5. Apply Reddit-Specific Voice

Reddit has its own voice rules ON TOP of the founder's voice profile:
- **First person always** ("I built..." not "We are proud to announce...")
- **Self-deprecating honesty** ("It's not perfect. The onboarding is rough. But it works.")
- **Disclose affiliation** ("Disclosure: I'm the founder of [product]")
- **Specific numbers** ("Built this in 3 months, got 47 beta users, 12 are active daily")
- **Admit limitations** before anyone calls you out
- **Ask specific questions** ("How would you handle X?" not "What do you think?")
- **Never be defensive** in comments

### 6. Generate Options

Create 2-3 post options. Each post includes:

**Title:** (most important part — determines if anyone clicks)
- Specific, descriptive, not clickbaity
- Matches the subreddit's title conventions

**Body:** Following the structure from reddit.md:
```
## The Problem
[1-2 paragraphs on the problem you personally experienced]

## What I Built
[Description with specifics — tech stack, approach, key decisions]

## The Journey
[Timeline, milestones, challenges, specific metrics]

## What I Learned
[2-3 concrete takeaways]

## What's Next
[Roadmap or next steps — shows you're genuine]

## Ask
[Specific questions for the community]

[Link to product — at the bottom, not the top]
```

**Vary the angles:**
- Post 1: Problem-focused ("I got frustrated with X, so I built Y")
- Post 2: Journey-focused ("3 months building this as a side project")
- Post 3: Value-focused ("I analyzed 200 [things] and here's what I found")

### 7. Self-Check Before Presenting

Before showing ANY post:
- [ ] Any phrase from writing-quality.md banned list?
- [ ] Does the title sound like a real Reddit post (not an ad)?
- [ ] Is affiliation disclosed?
- [ ] Are limitations honestly acknowledged?
- [ ] Does it provide genuine value even without the product link?
- [ ] Would this survive r/startups moderation?
- [ ] Is there a specific ask for the community (not "what do you think?")?
- [ ] Are all subreddit names verified as real?

Fix violations before presenting.

### 8. Present to Founder

"Here are 2 post options for [subreddit]. Each takes a different angle:

**Post 1: [angle]**
Title: [title]
[full body]

**Post 2: [angle]**
Title: [title]
[full body]

Pick your favorite. Remember to check [subreddit]'s current rules before posting — they change sometimes."

### 9. Remind About Engagement

After the founder picks a post:
"One more thing: Reddit posts live or die by comment engagement. After posting:
- Reply to every comment in the first 2 hours
- Thank people for criticism (seriously)
- Answer technical questions in detail
- Never be defensive, even if someone's rude
- If someone asks 'why not just use [competitor]?', give an honest, specific answer"
