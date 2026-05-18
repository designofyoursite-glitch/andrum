# Andrum AI Content Studio

Andrum is an Instagram content project. This workspace is a simple operating system for planning, generating, editing, and storing content.

## Working Principles

- Keep everything practical and easy to reuse.
- Write for clarity first, cleverness second.
- Prefer specific ideas over broad motivational language.
- Make content feel human, grounded, and visually native to Instagram.
- Use the strategy files before generating content.
- Save finished drafts in `outputs/`.
- Save useful source material, examples, and notes in `research/`.
- Save reusable AI instructions in `prompts/`.

## Folder Map

- `strategy/`: Core brand and content strategy.
- `brand/`: Brand platform, project story, philosophy, and high-level messaging.
- `product/`: Product materials, practice descriptions, guides, and source copy.
- `prompts/`: Reusable prompt templates for AI content work.
- `research/`: Audience notes, competitor examples, trend observations, and raw insights.
- `outputs/`: Drafts and finished content.

## Breathwork And Psychology Sources

Books and expert materials are for background understanding only.

Do not write Andrum content in:

- Academic tone.
- Therapist tone.
- Educational lecture tone.

Always translate concepts into:

- Emotionally recognizable moments.
- Body sensations.
- Real relationship situations.
- Simple human language.

The content should feel like:

> "Someone finally understands what this feels like."

Not:

> "Someone is teaching psychology."

## Authentic Relating And NVC Sources

Use Authentic Relating and Nonviolent Communication principles as background support for:

- Emotional depth.
- Relational awareness.
- Nervous system sensitivity.
- Honesty.
- Emotional nuance.

Do not write Andrum content that sounds like:

- A workshop facilitator.
- Overly processed communication.
- A therapy session.
- Conscious community cliches.
- A needs-and-feelings exercise.

Avoid overusing needs/feelings terminology.

The language should remain:

- Natural.
- Emotionally sharp.
- Modern.
- Internet-native.
- Relatable.

## Content Performance Rules

Use `strategy/content-performance-rules.md` as the quality bar for Instagram content.

Use `strategy/current-instagram-strategy.md` as the current operating strategy for the account. The account is in audience discovery, so prioritize low-cognitive-load emotional recognition before deeper breathwork or nervous system education.

Primary priority:

- Emotional recognition and relatability, not education.

If forced to choose between psychological precision and emotional recognition, always prioritize emotional recognition.

Writing should feel emotionally exposed, not emotionally polished. Prefer awkward honesty, contradiction, irrational emotional logic, self-awareness, and messy inner experiences over resolved wisdom or clean healing narratives.

Use the body-first filter whenever possible: translate emotional states into sensations and behaviors like chest tightness, stomach drop, adrenaline spike, numbness, shaking, dissociation, hyperfocus, relief waves, or the urge to check the phone.

Avoid obvious AI phrasing, symmetrical sentence structures, generic emotional summaries, repetitive validation, and content that sounds optimized but emotionally empty.

Every piece should optimize for:

- Immediate emotional recognition.
- Retention.
- Shares.
- Saves.
- Comment reactions like: "holy shit this is me".

The audience should feel:

> "This is exactly what happens inside me."

Not:

> "This is educational content."

Format rule:

- Reels need an immediate emotional hit, short hook-first writing, and low cognitive load.
- Carousels can go slightly deeper, but must keep swipe momentum and one idea per slide.

## Content Workflow

1. Start with one content idea or audience problem.
2. Match it to a content pillar.
3. Choose the format: Reel, carousel, caption, or story prompt.
4. Generate a rough draft using the templates in `prompts/`.
5. Run the draft through `prompts/subagent-quality-workflow.md`.
6. Critique the draft with the Critic Subagent.
7. Revise the draft based on the critique.
8. Run the revised draft through the Acceptance Subagent.
9. If acceptance says `REVISION REQUIRED`, revise again and repeat acceptance.
10. Save the final version in the right `outputs/` folder.

Mandatory quality gate:

- Every Andrum content-generation request must pass through `prompts/subagent-quality-workflow.md`: draft → critic subagent → revision → acceptance subagent → final delivery.
- This applies to all Reel hooks, Reel scripts, carousels, captions, story prompts, content calendars, product copy, landing-page copy, strategy docs, and content ideas.
- Small requests are not exempt. Even a request for 5 hooks must go through the quality gate.
- The only exception is when the user explicitly says to skip critique, skip subagents, or make a fast unreviewed draft.
- In the final response for any generated content, briefly state that the quality gate was used.

## Quality Bar

Good Andrum content should be:

- Simple enough to understand in 3 seconds.
- Specific enough to feel useful.
- Honest enough to build trust.
- Visually easy to turn into Instagram content.
- Worth saving, sharing, or replying to.

## Avoid

- Generic advice with no point of view.
- Overly polished corporate language.
- Trend-chasing that does not fit the brand.
- Long intros before the useful part.
- Content that sounds like an AI wrote it.
