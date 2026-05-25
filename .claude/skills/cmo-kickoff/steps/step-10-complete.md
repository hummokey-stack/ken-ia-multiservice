# Step 10: Summary & Task Execution Flow

## Context Loading

Load from `{output_folder}/`:
- `product-profile.md`
- `personas.md` (if exists)
- `voice-profile.md` (if exists)
- `strategy.md` (if exists)
- `tasks.md` (if exists)
- `launch-plan.md` (if exists)

**CRITICAL — Load before generating ANY content:**
- `{project-root}/_cmo/mkt/data/writing-quality.md` — Writing rules, banned phrases, and anti-AI-detection patterns. ALL generated content must follow these rules.

Load routing table:
- `{project-root}/_cmo/_config/task-modules.csv`

Load channel guides as needed:
- `{project-root}/_cmo/mkt/data/channels/`

## Your Task

Present a summary of everything created, then flow directly into executing the founder's first tasks. This is the "plan → action" moment — the founder should leave this session having DONE something, not just having a plan.

## Instructions

### 1. Present Summary

"Here's your complete marketing plan:

**Product:** [product name] — [one-line positioning]
**Stage:** [stage]
**Voice:** [voice type]
**Channels:** [list of recommended channels]
**Tasks:** [total] tasks, [this-week count] due this week
**Launch:** [launch schedule summary]

Everything is saved in your `_cmo-output/` folder. You can review and edit any file anytime.

**Ready to knock out your first task?**"

### 2. Start Task Execution Flow

Load `tasks.md` and find the first task with `Priority: this-week` and `Status: pending`.

Present it:
"**Your #1 task:** [task title]

[task description]

Want to do this now?
[Y] Let's do it
[S] Skip to next task
[Q] Quit for now — I'll remember where you left off"

### 3. Execute Task (if Y)

Load `task-modules.csv` and check the task's `Type` field.

**If module_available = true:**
Load the module from `module_path`. The module will:
- Read product-profile.md for product context
- Read voice-profile.md for voice matching
- Read strategy.md for strategic context
- Read the relevant channel guide for best practices
- Generate content options for the founder to review

**If module_available = false:**
Invoke the task-guide logic:
- Break the task into numbered steps
- Include channel-specific rules and best practices from channel guide
- Include timing recommendations
- If any sub-step involves content creation AND a module exists for it, embed content generation
- Provide actionable advice for every step

### 4. After Task Completion

"Done! That's one off the list.

**Next up:** [next this-week task title]

[Y] Let's do the next one
[S] Skip this one
[Q] That's enough for today — great start!"

### 5. Continue Until Done or Quit

Repeat the task execution flow for each remaining this-week task until:
- All this-week tasks are offered
- Founder selects [Q] to quit

### 6. Session End

When founder quits or all tasks are offered:

"Great session! Here's what you accomplished:
- [list tasks completed or content generated]

**What's saved:**
All your marketing artifacts are in `_cmo-output/`. They persist across sessions.

**Coming back later?**
Just type `/cmo-help` and I'll pick up right where we left off — I'll know your product, your voice, your strategy, and what tasks are still pending.

You've got this. Marketing isn't scary — it's just telling people about something you built. And you've already started."

## Output

No new artifact created. Tasks may be updated (status changes) in tasks.md.

## Menu

No menu — this is the final step. The session ends naturally when the founder quits or completes all tasks.

## Completion

Workflow complete. Founder can return via `/cmo-help`.
