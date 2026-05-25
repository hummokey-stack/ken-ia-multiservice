# Step 3: Audience Discovery & Persona Generation

## Context Loading

Load from `{output_folder}/` (if exists):
- `product-profile.md` — for product context to inform persona generation

If product-profile.md doesn't exist (step was skipped), ask about the product inline before generating personas.

## Your Task

Help the founder define their target audience and generate 2-3 realistic customer personas. For founders who are vague about their audience ("everyone"), guide them to specificity through conversation.

## Instructions

### 1. Check for Product Context

**If product-profile.md exists:**
"Based on your product profile, I already have some ideas about who your audience might be. Let me share what I'm seeing, and you can tell me if I'm on track."

Present initial audience hypothesis based on product analysis.

**If no product profile (step was skipped):**
"To create great personas, I need to understand your product a bit. Quick question — what does your product do and who's it for?"

Get minimum product context before proceeding.

### 2. Explore the Audience

Ask conversational questions to understand the audience deeply:

- "Who's using this right now? Or who do you imagine using it first?"
- "What do they do for work? What's their day like?"
- "What problem are they solving when they reach for your product?"
- "Where do they hang out online? Twitter? Reddit? Discord?"

**If they give a vague answer ("everyone", "developers", "businesses"):**
Don't accept it. Gently push for specificity:
- "I hear you — it could be useful for lots of people. But who would love it MOST? Who's your first 100 users?"
- "Think about the people who've actually tried it or asked about it. What do they have in common?"
- "If you could only tell ONE type of person about this, who would benefit most?"

Keep asking until you have a specific audience (e.g., "freelance web developers who are tired of using spreadsheets for invoicing").

### 3. Generate 2-3 Personas

For each persona, create a vivid, realistic profile:

**Persona structure:**
```
## Persona [N]: [Name] the [Title/Role]

**Demographics:** Age, role, experience level, location, company size
**Psychographics:** Values, attitudes, lifestyle, what they care about
**Current Behavior:** How they currently solve the problem (or don't)
**Pain Points:** Specific frustrations (3-4 bullet points)
**What would make them switch:** The trigger that would make them try your product
```

Make personas feel like real people, not marketing archetypes. Use specific details, not generic descriptions.

### 4. Validate with Founder

Present all personas and ask:
"Do these feel like your actual users? Anyone missing? Anyone who doesn't fit?"

Refine based on feedback until founder confirms.

### 5. Save Personas

Copy template from `../templates/personas.template.md` to `{output_folder}/personas.md`.

Populate with all confirmed personas. Update frontmatter `persona_count`.

## Output

Creates `{output_folder}/personas.md` with 2-3 detailed customer personas.

## Menu

"Your personas are saved. These will inform everything from strategy to content voice.

[C] Continue to brand voice builder
[S] Skip voice builder — I'll use a default voice for content"

- If C: Read fully and follow `./step-04-voice.md`
- If S: Read fully and follow `./step-04-voice.md` (no voice artifact, downstream uses neutral tone)

## Completion

Load next step as directed by menu selection.
