# Step 4: Brand Voice Builder

## Context Loading

Load from `{output_folder}/` (if exists):
- `product-profile.md` — for product context
- `personas.md` — for audience context

Load voice presets directory:
- `{project-root}/_cmo/mkt/data/voices/` — available preset files

## Your Task

Capture the founder's authentic writing voice so all generated content sounds like them, not AI. This is critical — if content sounds AI-generated, it damages the founder's personal brand, which is often their #1 distribution channel.

Two paths: import their own writing, or choose a preset that feels right.

## Instructions

### 1. Introduce the Voice Builder

"Now for something important — your voice. The #1 way people spot AI-generated content is that it doesn't sound like the person. I want everything we create to sound like YOU.

Two options:

**Option A: Import your writing** (recommended)
Paste 5-10 examples of your writing — tweets, blog posts, messages, whatever feels like 'you.' I'll analyze your style and use it for all content.

**Option B: Pick a preset**
Choose a voice profile that matches how you want to come across. We have:
- **Casual Builder** — 'just shipped this, here's what I learned'
- **Technical Authority** — deep expertise, specific insights, no fluff
- **Storyteller** — narrative-driven, behind-the-scenes, personal journey

Which feels right?"

### 2. Handle Import Path (Option A)

If founder chooses to import:

"Great choice. Copy and paste 5-10 examples of your writing directly here. These can be:
- Tweets or tweet threads (copy the text, don't share links — I can't browse URLs)
- Blog post paragraphs
- Slack/Discord messages
- Email excerpts
- Anything that sounds like 'you'

The more variety, the better I can capture your voice."

After receiving samples, analyze and extract:
- **Tone:** Is it casual? Formal? Humorous? Direct? Warm?
- **Vocabulary:** What words do they use often? What do they avoid?
- **Sentence patterns:** Short and punchy? Long and flowing? Mixed?
- **Signature habits:** Do they use emoji? Parenthetical asides? Questions? Lists?
- **Anti-patterns:** What does their writing NEVER sound like?

Present analysis: "Here's what I'm hearing in your voice: [analysis]. Does this feel right?"

Refine until confirmed.

### 3. Handle Preset Path (Option B)

If founder chooses a preset:

Load the selected preset file from `{project-root}/_cmo/mkt/data/voices/[preset-name].md`

Read the full preset and present it:
"Here's what [preset name] sounds like: [show examples from preset]

Does this feel like you? Or want to try a different one?"

Let them switch presets until they find one that fits.

### 4. Save Voice Profile

Copy template from `../templates/voice-profile.template.md` to `{output_folder}/voice-profile.md`.

**If import path:**
Populate with:
- Frontmatter: `method: import`, `sample_count: [number]`
- Voice Characteristics: extracted tone, vocabulary, patterns
- Voice Rules: always/never/signature phrases
- Examples: 2-3 example outputs in their voice

**If preset path:**
Populate with:
- Frontmatter: `method: preset`, `preset_name: [name]`
- Copy full preset content into voice profile
- Note which preset was selected

## Output

Creates `{output_folder}/voice-profile.md` with complete voice profile.

## Menu

"Your voice is locked in. From now on, everything I generate will sound like you, not like a robot.

[C] Continue to positioning & strategy
[S] Skip — proceed without voice profile"

- If C: Read fully and follow `./step-05-positioning.md`
- If S: Read fully and follow `./step-05-positioning.md` (content modules will use neutral professional tone)

## Completion

Load next step as directed by menu selection.
