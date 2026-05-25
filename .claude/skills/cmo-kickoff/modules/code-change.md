# Code Change Module

## Context Loading

Load before executing:
- `{output_folder}/product-profile.md` — product details + Tech Stack & Codebase section (file paths, framework, key directories)
- `{output_folder}/voice-profile.md` — for generating marketing copy in founder's voice
- `{output_folder}/strategy.md` — for strategic context behind the change
- `{project-root}/_cmo/mkt/config.yaml` — for `code_change_mode` and `git_mode` settings

## Your Task

Execute a marketing task that involves changes to the product's codebase. This could be updating landing page copy, adding a CTA, improving meta tags, adding social sharing buttons, implementing a viral loop, or any other product change driven by marketing strategy.

## HARD RULES (NO EXCEPTIONS)

- **NEVER push to main or master branch.** If git_mode is commit-and-push-pr, ALWAYS create a new branch first with prefix `cmo/`
- **NEVER commit if git_mode is never-commit.** Make changes to files but leave them unstaged.
- **NEVER modify files unrelated to the marketing task.** Only touch files directly relevant to the task.
- **ALWAYS show the founder a summary of what was changed** — even in always-make-changes mode.
- **ALWAYS preserve existing functionality.** Marketing changes should be additive or copy-only. Never break existing features.
- **Check for dirty working tree** before starting. If uncommitted changes exist, warn: "You have uncommitted changes. I'll make my changes on top of yours, but you may want to commit or stash first."

## Instructions

### 1. Check Settings

Read `code_change_mode` from config.yaml.

**If empty** (user never set preferences — maybe they chose URL/description in step-02 but now have a code change task):
Ask the settings questions now:
"This task involves a code change. Before I proceed, how do you want me to handle this?
[1] Ask first [2] Never touch code [3] Just make changes
And for git: [A] Don't commit [B] Commit only [C] Commit and create PR"
Save to config.yaml.

### 2. Understand the Task

Parse the task description to determine:
- **What needs to change:** Landing page copy? Meta tags? New component? CTA button?
- **Which files are involved:** Reference the Tech Stack & Codebase section in product-profile.md for file paths
- **What the desired outcome is:** What should it look like after the change?

### 3. Explore Relevant Files

Using file paths from the product profile's Tech Stack section:
- Read the specific files that need modification
- Understand current content, structure, and framework conventions
- Note the component patterns, styling approach, and file organization

If the product profile doesn't have a Tech Stack section (user chose URL/description initially):
- Scan the project root for README, package.json, key directories
- Find the relevant files for this specific task
- Save the discovered structure for future tasks

### 4. Plan the Change

Draft the specific changes:

**For copy changes** (landing page text, headlines, CTAs):
- Generate new copy using the founder's voice profile
- Provide 2-3 options if in `always-ask` mode
- Reference the strategy for WHY this copy change matters

**For structural changes** (adding a button, sharing widget, viral loop):
- Plan the implementation following the project's existing patterns
- Use the same component library, styling approach, and conventions already in the codebase
- Keep it minimal — the smallest change that achieves the marketing goal

**For meta/SEO changes** (meta tags, Open Graph, structured data):
- Generate the specific tags needed
- Reference the SEO and AI SEO/GEO channel guides for best practices

### 5. Execute Based on code_change_mode

**If `always-ask`:**
"Here's what I want to change:

**File:** `[file path]`
**What:** [description of change]
**Why:** [marketing rationale from strategy]

**Preview:**
[Show the specific content/code that will change — before and after]

[Y] Make the change
[N] I'll do it myself
[E] Edit the plan first"

- If Y: Make the change, proceed to git handling
- If N: Show the code snippets they need to copy-paste, end
- If E: Let them modify the plan, then re-present

**If `never-touch-code`:**
Present as a step-by-step guide:

"Here's exactly what to change:

**Step 1:** Open `[file path]`
**Step 2:** Find this section: [show current code]
**Step 3:** Replace with: [show new code — copy-paste ready]
**Step 4:** Save the file

**Why this matters:** [marketing rationale]"

Do NOT make any file changes. End here.

**If `always-make-changes`:**
Make the changes directly. Then show:

"Done! Here's what I changed:

**File:** `[file path]`
**Change:** [description]
[Show diff or before/after]

**Why:** [marketing rationale]"

Proceed to git handling.

### 6. Handle Git (only if changes were made)

Read `git_mode` from config.yaml.

**If `never-commit`:**
"Changes saved to [file list]. I'll leave the git stuff to you."
Done.

**If `commit-only`:**
- Stage only the changed files (not `git add .`)
- Commit with descriptive message: `marketing: [brief description of change]`
- Example: `marketing: update landing page headline to lead with user pain point`
"Committed! You can review with `git log` and push when you're ready."

**If `commit-and-push-pr`:**
- Create a new branch: `cmo/[slugified-task-description]`
  - Example: `cmo/update-landing-page-headline`
- Stage only changed files
- Commit with descriptive message
- Push the branch
- Create a PR with:
  - Title: `[Marketing] [task description]`
  - Body: Marketing rationale from strategy, what was changed and why, screenshot if applicable
- **NEVER push to main/master. ALWAYS create a new branch.**
"PR created! Review it at [PR URL]."

### 7. After Completion

"Task done! [summary of what was accomplished]

Ready for the next task? [Y/S/Q]"

Return to the calling flow (step-10 or /cmo-help).
