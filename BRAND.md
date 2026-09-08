# Personal brand notes

Kept here so the profile, slides and any future site stay consistent, and so the
palette does not get re-invented from scratch each time.

## The mark

**Six nodes in a ring inside four nested frames.** It is not a generic glyph — it
encodes the architecture the profile is built around: a six-tool autonomous reasoning
loop held inside four layers of hallucination guardrails. The nodes are the tools, the
frames are the guardrails, and the frames get fainter outward because the outer checks
are the loosest.

Use it at 200px or larger. Below that the four frames stop reading as distinct and it
should be replaced by the innermost frame plus the six nodes only.

## Palette — "petrol and signal"

Chosen to sit apart from the default developer-profile look (neon on black) and from
the VCreaTek indigo/orange kit, so this reads as a person rather than as a company page.

| Role | Dark | Light | Notes |
|---|---|---|---|
| Ground | `#0E1418` | `#F5F2EC` | Petrol-black, and a warm bone rather than pure white |
| Surface | `#141C21` | `#FFFFFF` | Cards |
| Primary text | `#F5F2EC` | `#12181C` | |
| Secondary text | `#8FA3A8` | `#5C6B70` | |
| Petrol (structure) | `#2E7F84` / `#5FB3B0` | `#14494F` | Frames, section labels |
| Signal (metrics) | `#E8A33D` | `#A8681A` | **Reserved for numbers and accents only** |
| Hairlines | `#23343A` | `#D6D0C4` | Borders, pills |

The discipline that makes it work: **signal amber is only ever used for a quantity or
a single accent bar.** The moment it becomes decoration the whole thing looks like
every other gradient profile.

## Type

No web fonts — GitHub renders these SVGs sandboxed, so external fonts never load.
Everything uses a system stack that resolves everywhere:

```
Segoe UI, Inter, system-ui, -apple-system, Helvetica Neue, Arial, sans-serif
```

Section labels are 11–13px, weight 600, letter-spaced 2–3.6. That letter-spaced
small-caps label is the one recurring typographic gesture; it does the work that
icons and badges were doing before.

## Theme handling

Both graphics ship as a dark and a light SVG, selected with `<picture>` and
`prefers-color-scheme`. GitHub honours this in READMEs. Never ship a single
graphic with a transparent background — it borrows whichever theme the reader is on
and the text disappears half the time.

## What this brand deliberately avoids

- Animated GIFs and waving-hand emoji
- Walls of technology icons
- Profile view counters and streak cards
- Gradient headers

Not because they are ugly, but because they are the visual grammar of a first
portfolio. Seniority reads as specificity and restraint: a number, a diagram, and a
sentence about a tradeoff.
