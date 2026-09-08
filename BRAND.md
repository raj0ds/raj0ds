# Personal brand notes

Kept here so the profile, slides and any future site stay consistent.

## The idea

The work is turning **unstructured language into validated structure** — consumer
complaints into scored aspects, bilingual pharma PDFs into FHIR R5 bundles. The
through-line of the career, chemistry included, is provable correctness.

So the visual world is a **validated record**: a certificate of analysis, a
regulatory filing. Not a developer banner. There is no logo mark, because the
subject matter is documents, and a document does not need a badge.

The banner reads left to right as **who → what → result**: identity, then one real
record being transformed, then the outcome that transformation produced. The graphic
explains the work rather than decorating it.

## Palette — cool document

| Role | Light | Dark |
|---|---|---|
| Ground | `#E9EBEE` | `#12151A` |
| Ink | `#15181D` | `#E9EBEE` |
| Secondary ink | `#3A4150` | `#AEB6C4` |
| Muted / field labels | `#697180` | `#868FA0` |
| Cobalt | `#2440C8` | `#8AA0FF` |
| Hairline | `#C6CAD2` | `#2C323C` |

**Cobalt is the only colour, and it is never decoration.** It marks exactly three
things: the rule under the name, validation (the check and "schema valid"), and the
one or two lines that state a real decision. Everything else is ink, muted ink, or a
hairline. The moment cobalt appears on something that is not structural, the design
starts to look like every other profile.

A cool grey ground rather than warm cream is deliberate: cream-plus-terracotta is
currently the most recognisable AI-generated look, and near-black-plus-neon is the
second. This is neither.

## Type

Two families, clearly distinct in job:

- **Georgia** (fallbacks: Iowan Old Style, Palatino Linotype, Palatino, serif) —
  name, headings, stage names, and the italic lines that carry an argument. A serif
  is the point: GitHub profiles are uniformly sans, so this reads as considered.
- **Consolas** (fallbacks: SF Mono, Menlo, DejaVu Sans Mono, monospace) — record
  fields, figures, stack values. Monospace only where alignment does real work, in
  table columns and key/value pairs. Never for labels or headings.

No web fonts. GitHub renders these SVGs sandboxed, so anything external silently
fails to load; only system stacks are safe.

## Structure

Hairlines and column positions do the organising. No cards, no border radius, no
shadows, no fills behind content. Columns sit at fixed x positions (72 / 270 / 656 in
the pipeline table) so the eye tracks down a column as easily as across a row.

## Theme handling

Every graphic ships as a light and a dark SVG, chosen with `<picture>` and
`prefers-color-scheme`. GitHub honours this in READMEs. Never ship one graphic with a
transparent background — it borrows the reader's theme and the text disappears for
half the audience.

## Deliberately avoided

Animated GIFs, waving-hand emoji, technology icon walls, profile view counters,
streak cards, gradient headers, tracked-out all-caps eyebrow labels, meta strings
joined with middle dots, numbered `01 / 02 / 03` markers, and arrows appended to
link text.

Not because any of these is ugly, but because they appear on every profile
regardless of subject. Seniority reads as specificity: one real record, two real
decisions, three real numbers.

## Reviewing changes

These SVGs were first built without ever being looked at, and the result was bad —
an icon-like mark, 340px of dead space, and four of the five commonest generated-design
tells. **Render before judging.** Headless Chrome is enough:

```bash
chrome --headless=new --disable-gpu --hide-scrollbars \
  --window-size=1200,414 --screenshot=out.png file:///path/to/asset.svg
```
