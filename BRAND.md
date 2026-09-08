# Brand notes

**The GitHub profile follows the portfolio, not the other way round.** The palette,
type roles and signature devices below are lifted from `rajeev_portfolio/static/css/style.css`
so the two never drift. If the portfolio's tokens change, re-derive these.

## Palette (both taken from the portfolio's two themes)

| Role | Dark | Light |
|---|---|---|
| Ground | `#020810` | `#f8fafc` |
| Surface | `#0a1225` | `#ffffff` |
| Surface raised | `#0f1a30` | `#f1f5f9` |
| Border | `#1a2d4a` | `#e2e8f0` |
| Border strong | `#243a5c` | `#cbd5e1` |
| Cyan (primary) | `#00e5ff` | `#0891b2` |
| Violet | `#7c3aed` | `#6d28d9` |
| Green | `#10b981` | `#059669` |
| Amber | `#f59e0b` | `#d97706` |
| Text | `#e2e8f0` | `#0f172a` |
| Text muted | `#94a3b8` | `#475569` |
| Muted | `#475569` | `#94a3b8` |

Colour carries meaning and is not decoration: **cyan** = structure and keys,
**green** = a validated or passing result, **amber** = the decision or the thing that
got caught, **violet** = storage and identity.

## Type

The portfolio uses JetBrains Mono, Inter and Space Grotesk. GitHub renders README
SVGs sandboxed, so **web fonts never load** — these files fall back to
`Consolas, 'SF Mono', Menlo, monospace` and `'Segoe UI Semibold', 'Segoe UI', sans-serif`.
Close in spirit, and safe everywhere. Do not add a Google Fonts link to an SVG; it
fails silently.

## Signature devices

- **The code window** — titlebar with three dots, a filename tab, line numbers,
  syntax colours. Straight from the portfolio hero; it is the element that makes the
  profile and the site read as one thing.
- **The status pill** — green dot, thin border, mono caps.
- **The gradient name** — cyan → violet on the surname only.

## Diagrams must show, not list

The first version of this profile described the architecture in prose and a table.
It was text-heavy and said less than a picture would. The rule now: **if a stage can
be drawn as the thing it does, draw it.**

- record volume → a dense field of marks
- K-Means sampling → real clusters with the chosen representative lit
- concurrency → parallel lanes, each with a worker
- token reduction → three bars whose widths *are* the reduction
- guardrails → gates, with one answer passing and one caught and sent back

Never invent specifics to fill a diagram. The four guardrail gates are unlabelled
because the real layer names are not known; label them once they are.

## Generated, not hand-placed

`assets/*.svg` come from the generator scripts. Hand-editing coordinates is how the
first version ended up with 340px of dead space. Regenerate, then **look at it**:

```bash
chrome --headless=new --disable-gpu --hide-scrollbars \
  --window-size=1200,360 --screenshot=out.png file:///path/to/asset.svg
```
