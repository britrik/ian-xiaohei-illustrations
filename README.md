# Ian Xiaohei Illustrations

> Turn the judgments, workflows, states, and metaphors in articles into hand-drawn, absurd yet crisp inline illustrations on a white background.
>
> 16:9 landscape | Xiaohei IP | Pure white hand-drawn | Sparse red/orange/blue annotations | Codex Skill

---

## What This Repository Is

Ian Xiaohei Illustrations is a Codex Skill that guides AI agents to generate inline illustrations for articles, posts, blogs, Notion documents, and methodology content.

It is not a generic illustration prompt, nor a PPT infographic template. Its core goal is: first understand the cognitive anchors in the article, then turn one judgment, workflow, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory diagram.

The default visual IP is "Xiaohei" (Little Black): a solid black creature with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, not a corner decoration — he is an absurd worker earnestly participating in the system.

In one sentence: **Don't just "add an image" — draw the key cognitive action in the article.**

---

## Who This Is For

Especially suitable for:

- People writing articles who need inline illustrations
- Those creating knowledge content, methodology content, or AI workflow content
- Those who want to turn abstract judgments into concrete metaphors
- Those who want a lighter, weirder, more personally recognizable illustration style than PPT infographics
- Codex users doing content production who want a stable, reusable visual language

Not suitable for:

- Those wanting commercial illustrations, brand key visuals, or refined flat illustrations
- Those wanting traditional PPT infographics, complex architecture diagrams, or flowcharts
- Those wanting children's cartoons, cute IP, or sticker-style images
- Those trying to cram large amounts of body text, long explanations, or full course pages into one image
- Those who need strictly editable vector source files

---

## What It Produces

Default output:

- 16:9 landscape inline illustrations
- A shot list of 4-8 images per article
- Each image's theme, core meaning, structure type, Xiaohei action, and suggested annotation words
- Final PNG images, saved to `assets/<article-slug>-illustrations/` in the workspace

Does not output by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover key visuals
- Large text-based infographics

---

## Visual Style

This skill uses Ian's "Xiaohei Absurd Inline Illustration" style by default:

- Pure white background — no paper texture, beige, shadows, gradients
- Black hand-drawn line art — thin lines, slight wobble
- Lots of white space — subject occupies about 40%-60% of the frame
- Sparse red, orange, and blue handwritten annotations in the article's language
- One image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action, not just decorate
- Absurd, creative, crisp — but not childish, not cutesy

---

## Example Results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish, Many Uses

![One Fish, Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration samples, not composition templates. When using, invent metaphors fresh from the current article — do not copy the objects and compositions from old cases.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/britrik/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill to the Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use in Codex:

```text
Use $ian-xiaohei-illustrations Design and generate 5 Xiaohei absurd inline illustrations for this article.
```

---

## How to Use

### Just Plan the Illustrations

```text
Use $ian-xiaohei-illustrations Don't generate images yet.
Please analyze where this article deserves illustrations and output a shot list of about 5 images.
For each image, specify: which paragraph it follows, theme, core meaning, structure type, what Xiaohei is doing, suggested elements, and suggested annotation words.

<paste article>
```

### Generate Inline Illustrations Directly

```text
Use $ian-xiaohei-illustrations Generate 4 Xiaohei absurd inline illustrations for this article.
Requirements: 16:9 landscape, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten annotations.

<paste article>
```

### Generate One Image for a Single Concept

```text
Use $ian-xiaohei-illustrations Generate one inline illustration for "Trust is not shouted — it's built piece by piece with evidence."
The image should be absurd yet crisp, and Xiaohei must perform the core action.
```

### Remove Titles or Fix Text in an Image

```text
Use $ian-xiaohei-illustrations Help me edit this image — remove the "Flowchart" title in the top-left corner, keeping everything else.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

The skill's workflow is:

1. Read the article, Markdown, Notion content, screenshots, or user-provided topic
2. Extract core points, cognitive turns, workflow structures, and paragraphs suitable for visualization
3. First output a shot list: each image selects only one cognitive anchor
4. For each image, choose a structure type: Workflow, System Detail, Before/After, Character State, Conceptual Metaphor, Method Layers, Map Route, or Mini Comic
5. Invent a low-tech, absurd but plausible physical metaphor fresh for this article
6. Have Xiaohei perform the core action
7. Generate each image individually using an image model
8. Check against the QA checklist: white background, white space, Xiaohei action, annotations, non-PPT feel, non-recycled composition
9. Save final PNGs and report usage and paths

---

## Directory Structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory to install into Codex is:

```text
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub sharing documents.

---

## Notes

- The shorter the text in images, the more stable the generation.
- Each image should tell only one core structure — don't turn the article into an instruction manual.
- Xiaohei must perform the core action; if removing Xiaohei still leaves the core metaphor fully intact, he's too decorative.
- Example images are only for calibrating line density, white space, color restraint, and Xiaohei participation — do not copy compositions.
- AI image models may produce wrong characters, hallucinated labels, style drift, or extra titles — check after generation.
- If Chinese characters are severely wrong, prioritize reducing annotation words and regenerating.

---

## Related Projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — Chinese hand-drawn technical PPT-style page generation skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Obsidian + Claude AI personal knowledge base setup guide

---

## About the Author

**Ian (伊恩)** — Product Designer / Solo Company Practitioner / AI Builder

Building solo companies with AI teams.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## English Fork

This English-language fork is maintained by [britrik](https://github.com/britrik).
All content translated from the original by Ian, with attribution preserved per the MIT License and NOTICE.

Original: [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)

---

## License

MIT License. See [LICENSE](LICENSE).
