# Contact Form — freeCodeCamp CSS Lab

A personal contact form built as a [freeCodeCamp](https://www.freecodecamp.org/) CSS project, restyled as **private correspondence** (an invitation card / visit card) rather than a corporate contact page.

## Goal of this project

The purpose of this repository is to **explore the capabilities of the design "taste" skill in agent-driven development**, using the freeCodeCamp CSS labs as a controlled, well-scoped sandbox. The lab's pass/fail tests keep the work grounded in concrete, verifiable requirements, while the design skill is given freedom to apply a distinct visual direction on top of those requirements.

## Executors

The build and iteration of this project were driven by multiple AI coding agents acting as executors:

- **Cline** — primary implementation agent (works in the VS Code / JetBrains environment), responsible for scaffolding, CSS styling, and passing the lab tests.
- **HY3** — additional execution / iteration pass.
- **HY4** — additional execution / iteration pass.

All three operate under the same `AGENTS.md` lab specification and the design direction produced by the taste skill.

## The Design Taste Skill

Styling is guided by the **design taste skill** (`design-taste-frontend`, sourced from [`Leonxlnx/taste-skill`](https://github.com/Leonxlnx/taste-skill)).

Instead of defaulting to a generic template, the skill deals a concrete **design direction** and the agent is expected to adopt it rather than blend it with the layout it "would have made anyway." For this build the dealt direction was:

- **Direction:** *The page is the object* — the contact form is treated as a physical printed artefact (a card / piece of correspondence).
- **Brief:** A personal contact form with three fields written to one person, styled as private correspondence.
- **Type:** Gambarino (display serif) / General Sans (body grotesk).
- **Colour:** Orange and black on white paper.
- **Sections:** intro → contact (visit card on a photograph) → footer (the back of the card).

The resolved direction is persisted in `.taste-skill/direction.json` and `.taste-skill/sheet.txt` for inspection and reproducibility.

## Project structure

```
.
├── index.html          # Markup: intro, contact form, footer ("the back of the card")
├── styles.css          # All styling, driven by the taste-skill direction
├── AGENTS.md           # freeCodeCamp lab spec + user stories + tests
├── assets/             # Atmosphere photographs (People set) used as the contact backdrop
├── skills-lock.json    # Pinned design-taste-frontend skill
└── .taste-skill/       # Resolved design direction (direction.json + sheet.txt)
```

## Lab requirements covered

The form satisfies all 24 freeCodeCamp user-story tests, including:

- A `.form-container` holding the `<form>` with an `<h2>`, a `text` input (#name), an `email` input (#email), a `<textarea>` (#message), and a `type="submit"` button.
- Labels with `for` attributes matching each field's `id`.
- `.form-container` styled with `background-color`, `border-radius`, `padding`, and `width`.
- Inputs / textarea with `width`, `padding`, and bottom margin.
- Labels with `margin` and `color`.
- A submit button with a `background-color`, a non-default `font-size`, and a `:hover` background change.

## Running it

It is a static site — open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

The freeCodeCamp test suite can be run against the page to confirm all 24 tests pass.
