# Step 8: Task Breakdown & Prioritization

## Context Loading

Load from `{output_folder}/` (if exists):
- `product-profile.md` — product stage, platform presence, budget
- `strategy.md` — the strategy we're breaking into tasks
- `voice-profile.md` — for task descriptions that involve content creation

Load routing table:
- `{project-root}/_cmo/_config/task-modules.csv` — to assign correct task types

## Your Task

Break the marketing strategy into concrete, specific, actionable tasks that a founder can execute. Each task must be specific enough that the founder knows EXACTLY what to do — "write a tweet about your product" is too vague. "Write a 5-tweet thread about [specific topic] targeting [specific audience] using [specific hook format]" is what we want.

**CRITICAL RULES:**
- Every task must be specific enough to execute without further clarification
- Tasks must include the WHAT, WHERE, WHY, and HOW
- Task types must match values in task-modules.csv for routing
- Prioritize by impact: "this-week" tasks should be the highest-impact, lowest-effort actions
- For zero-audience channels, first tasks should be audience-building (not product promotion)
- Tasks must be realistic for a solo founder's schedule
- If the strategy includes product code changes (landing page copy, CTAs, meta tags, sharing buttons, viral loops) AND product-profile.md has a "Tech Stack & Codebase" section, assign type `product_code_change`. If no codebase section exists, use `landing_page_copy` or the closest guide-only type instead

## Instructions

### 1. Extract Tasks from Strategy

Go through each channel in the strategy and extract specific tasks:

For each task, determine:
- What exactly to do (specific action, not vague goal)
- Which channel it's for
- What type it is (from task-modules.csv: tweet_thread, reddit_post, indie_hackers_post, email_sequence, seo_content, etc.)
- Why it matters (connected to strategy reasoning)
- How long it'll roughly take (5 min, 30 min, 1 hour, etc.)

### 2. Format Each Task

```
### Task N: [Specific action verb] + [specific deliverable]

- **Channel:** [which channel]
- **Type:** [task_type matching task-modules.csv]
- **Priority:** [this-week / next-week / this-month]
- **Status:** pending
- **Time estimate:** [5 min / 30 min / 1 hour / 2 hours]
- **Description:** [Detailed, specific description that includes:]
  - WHAT: exactly what to create/do
  - WHY: why this matters for your product specifically
  - HOW: specific format, structure, or approach
  - EXAMPLE: a brief example or hook to get started
```

**Good task example:**
```
### Task 3: Write a "Show HN" post draft

- **Channel:** Hacker News
- **Type:** hacker_news_post
- **Priority:** this-week
- **Time estimate:** 1 hour
- **Description:** Write your Show HN submission. Title format: "Show HN: [Product] — [one-line description of what makes it different]". Body: 3-4 paragraphs covering (1) what problem you solve, (2) why existing solutions fall short, (3) your approach and key technical decisions, (4) link and what you're looking for (feedback, users, etc.). HN values technical depth and genuine problem-solving — lead with the problem, not features. Prepare 5-10 answers to likely comments: "Why not just use X?", "How is this different from Y?", pricing questions.
```

**Bad task example:**
```
### Task 3: Post on Hacker News
- **Description:** Share your product on HN.
```

### 3. Prioritize Tasks

**this-week (3-5 tasks):** Highest impact, lowest effort. These should give the founder momentum and early wins.
- If zero audience: first tasks should be audience-building, not product promotion
- If existing audience: first tasks can be product-focused

**next-week (3-5 tasks):** Important but can wait. Build on this-week's results.

**this-month (remaining tasks):** Longer-term or higher-effort tasks.

### 4. Ensure Task Coverage

Verify:
- Every recommended channel has at least 1-2 tasks
- Zero-audience channels have warm-up tasks BEFORE product tasks
- AI SEO/GEO has concrete tasks if it was in the strategy
- The first 3 tasks feel immediately doable (not intimidating)

### 5. Present and Validate

Show the full task list. Ask:
- "Do these feel doable for your schedule?"
- "Any tasks that feel too vague or too ambitious?"
- "Should we reprioritize anything?"

### 6. Save Tasks

Copy template from `../templates/tasks.template.md` to `{output_folder}/tasks.md`.
Populate with all tasks. Update frontmatter `total_tasks`.

## Output

Creates `{output_folder}/tasks.md` with 10-20 specific, prioritized marketing tasks.

## Menu

"Tasks ready! Let's create your launch schedule next.

[C] Continue to launch schedule
[S] Skip schedule"

- If C: Read fully and follow `./step-09-schedule.md`
- If S: Read fully and follow `./step-09-schedule.md`

## Completion

Load next step as directed by menu selection.
