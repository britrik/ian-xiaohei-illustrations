---
name: ian-xiaohei-illustrations
description: Generate Ian-style inline illustrations for articles. For when the user asks to create "absurd", "Xiaohei", "hand-drawn", "inline illustration", "article illustration", "illustration suggestions", "shot list", "remove title/edit image", etc. for articles, posts, blogs, Notion documents, workflow docs, methodology, process, structure, state, metaphor, or opinion. Default style uses the Xiaohei IP, pure white hand-drawn, sparse red/orange/blue annotations, concise yet wildly creative visual style.
---

# Ian Xiaohei Absurd Inline Illustrations

## Core Positioning

Design and generate 16:9 landscape inline illustrations for articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — it is to turn the article's key judgment, workflow, structure, state, or metaphor into a crisp, absurd, creative, readable but non-instructional hand-drawn explanatory diagram.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression, earnestly doing something absurd but plausible. Xiaohei must participate in the core action of the image, not just stand by as decoration.

## Read These References First

Read by task need — do not stuff the full context at once:

- `references/style-dna.md`: Style DNA, colors, text, taboos.
- `references/xiaohei-ip.md`: Xiaohei IP image, personality, action library, and taboos.
- `references/composition-patterns.md`: Structure types, original metaphor methods, and anti-recycling rules.
- `references/prompt-template.md`: Single-image generation prompt template.
- `references/qa-checklist.md`: Post-generation checking and iteration rules.
- `assets/examples/`: Only for low-frequency visual calibration, not the default generation path. Do not copy the composition, objects, or annotations from these examples.

## Workflow

### 1. Digest the Article

First read the user's article, link, Notion page, Markdown file, or screenshot content. Extract:

- What is the core point
- Which paragraphs carry cognitive turns
- What content is suitable for illustration
- What should remain text-only

Do not illustrate evenly. Prioritize "cognitive anchors", such as: core judgments, two breakpoints, input-output loops, branching, before/after, multi-use, handoff paths, common pitfalls, character state changes.

### 2. Output Illustration Strategy First

If the user only says "analyze where to illustrate / think about illustration needs", provide a shot list first. For each image specify:

- Which paragraph it follows
- Image theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested annotation words

Default 4-8 images. 1-3 for very short articles; don't exceed 9 even for long ones. Good enough is enough — avoid turning the article into a picture book.

### 3. Generate Individual Images

If the user explicitly says "generate / output / make image / help me generate", don't stop for confirmation; generate each image individually using the built-in `image_gen`. Do not combine multiple images into one.

Each image tells only one core structure. Prompts must include:

- 16:9 landscape inline illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue handwritten annotations
- Lots of white space
- Xiaohei as the core action subject
- No PPT, commercial illustration, cutesy childishness, complex architecture, top-left type titles

Do not recycle old cases. Examples only provide style density and Xiaohei participation patterns — do not directly reuse compositions like "conveyor belt breakpoints / Xiaohei pulling wires / material fish / stamp toolbox / common pit path" unless the user explicitly asks to recreate a specific image. Reinvent a weird but plausible metaphor fresh from the current article each time.

### 4. Check and Iterate

After generation, check against `references/qa-checklist.md`. If any of the following occur, prioritize regeneration or local editing:

- Xiaohei is just decoration
- Image is too crowded
- Too much like a flowchart/PPT
- Too many Chinese characters or severe typos
- Top-left titles like "Common Pitfalls / Flowchart / System Architecture"
- Style too cute, childish, or stiff
- Background is not clean white

### 5. Save and Deliver

If the user is working in a workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Name in order:

```text
01-topic-name.png
02-topic-name.png
```

Preserve original generation files; do not overwrite existing assets unless the user explicitly requests replacement.

## Output Tone

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- Each image's purpose
- Save path
- Which images are solid, which are optional

Don't write long explanations of style theory; let the images speak for themselves.
