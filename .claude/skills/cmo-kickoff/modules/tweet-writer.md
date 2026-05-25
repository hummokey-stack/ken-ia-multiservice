# Tweet Thread Writer Module

## Context Loading

Load ALL of these before generating any content:
- `{output_folder}/product-profile.md` — product details, value prop, audience
- `{output_folder}/voice-profile.md` — founder's voice characteristics, rules, anti-patterns
- `{output_folder}/strategy.md` — Twitter/X section for strategic context
- `{project-root}/_cmo/mkt/data/channels/twitter-x.md` — channel best practices, hook patterns, thread structure
- **CRITICAL:** `{project-root}/_cmo/mkt/data/writing-quality.md` — writing rules and banned phrases. Every tweet MUST pass these rules. Scan output for banned phrases before presenting.

## Your Task

Generate tweet threads in the founder's authentic voice for a specific marketing task. The output must be indistinguishable from the founder's natural writing. If it sounds like AI wrote it, you failed.

## Instructions

### 1. Understand the Task

Read the task description passed from the task-flow. Determine:
- What type of tweet? (launch thread, build-in-public, hot take, milestone, engagement)
- What's the core message?
- What product context is relevant?

### 2. Load Voice Profile

Read voice-profile.md carefully. Extract:
- Tone (casual? technical? storytelling?)
- Vocabulary (words they use, words they avoid)
- Sentence patterns (short and punchy? mixed? long-form?)
- Anti-patterns (what their writing NEVER sounds like)
- Example tweets from their profile

If no voice profile exists, use a neutral, direct tone and warn: "No voice profile found. Content will be in a generic voice. Run the voice builder in /cmo-kickoff to sound like you."

### 3. Load Channel Best Practices

From twitter-x.md, reference:
- Thread structure template (hook → context → insights → takeaway → CTA)
- Hook patterns that work
- Optimal thread length (4-8 tweets)
- What the algorithm favors
- What to avoid

### 4. Apply Writing Quality Rules

From writing-quality.md, enforce:
- NO banned phrases (check every single tweet against the full banned list)
- Use contractions naturally
- Short paragraphs (1-3 sentences)
- Specific claims with numbers, not vague superlatives
- Physical verbs over abstract ones ("sanded down" not "improved")
- NO em dashes. Use commas, periods, or parentheses
- NO "This isn't X. This is Y." pattern or any variation
- NO engagement bait ("let that sink in", "read that again")
- NO AI cringe ("supercharge", "unlock", "game-changer")
- Humor from specificity, not from jokes

### 5. Generate Options

Create 3-5 thread options. Each thread:
- 4-7 tweets long
- Starts with a hook that stops the scroll (first tweet is 80% of the battle)
- One idea per tweet, use line breaks
- Ends with a clear takeaway or soft CTA
- Links go in a reply to tweet 1, never in the thread body
- Matches the founder's voice exactly

**For each thread, vary the angle:**
- Thread 1: Lead with the problem/pain
- Thread 2: Lead with a specific result or number
- Thread 3: Lead with a contrarian take or surprising insight
- Thread 4 (if applicable): Lead with a story/narrative
- Thread 5 (if applicable): Lead with a question

### 6. Self-Check Before Presenting

Before showing ANY thread to the founder, scan every tweet for:
- [ ] Any phrase from the writing-quality.md banned list?
- [ ] Does it sound like something the founder would actually type?
- [ ] Is every claim specific (numbers, names, concrete details)?
- [ ] Are there em dashes? (replace with commas or periods)
- [ ] Does it use "Furthermore," "Additionally," or any dead transition?
- [ ] Does it have the "This isn't X. This is Y." pattern?
- [ ] Would you scroll past this hook? (if yes, rewrite the hook)

Fix any violations before presenting.

### 7. Present to Founder

"Here are 3 thread options for [task]. Each takes a different angle:

**Thread 1: [angle]**
[full thread]

**Thread 2: [angle]**
[full thread]

**Thread 3: [angle]**
[full thread]

Pick your favorite, or I can remix elements from different ones. You can also edit any tweet before posting."

### 8. Handle Feedback

- If founder picks one: present final version clean for copy-paste
- If founder wants edits: apply changes and re-present
- If founder wants to regenerate: create new options with different angles
- If founder says "this sounds too AI": re-read voice profile, strip out any remaining AI patterns, rewrite with more personality
