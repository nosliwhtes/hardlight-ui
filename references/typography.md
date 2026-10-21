# Typography: compose information with a specific voice

## Assign jobs before picking families

Create roles for display, page/section heading, prose, control/label, annotation and data/code. A role needs a family/fallback, weight, size, line height, measure and wrapping rule. Start with the fewest families that can do those jobs; add a second because it changes reading or establishes a subject-specific voice, not because every design needs a serif/sans pairing.

The subject can be the typography. A type foundry can show its actual products as huge specimens; an instrument can align real measurements; a publication can reveal an argument through a carefully set title. “Modern” is not a font name, and monospace does not make an unrelated product technical. Preserve established brand type in refinement and extension.

## Set a specimen with difficult real content

Use the longest actual destination label, a realistic heading, a paragraph, a price or measurement and the most complex input help. Include I/l/1, O/0, punctuation, accented names, mixed scripts and relevant currency/units. Inspect the actual loaded font and the fallback; missing weights or synthetic italic can change the whole page. Check licenses and hosting constraints before committing a webfont. External fonts need a delivery/performance plan; offline demonstrations should not depend on a remote font service.

As starting hypotheses, not standards: ordinary prose around 1–1.125rem, roughly 50–75 characters per line and comfortable leading; UI labels often need a tighter line box than prose. Read the result instead of enforcing one universal size. Dense expert tools may use smaller data labels when the full task, contrast and hit regions hold. Browser zoom and user text settings must remain usable.

## Compose at three distances

1. **Page:** identify the primary topic and reading/action path without reading every line. If every heading has equal size and weight, revise the hierarchy, not just the color.
2. **Paragraph/row:** keep related labels with their content, make lists scan consistently and avoid stranded captions. Long prose usually benefits from rag-right setting; fully justified text requires actual typographic care, not a switch flipped for elegance.
3. **Glyph:** tune display tracking, punctuation and optical alignment at the real rendered size. Do not use negative tracking to force a title into an arbitrary box. Small uppercase needs enough space and contrast to read; it is not a required section eyebrow.

For data, align comparable quantities and use tabular numerals when appropriate. Show units and precision consistently. Do not use whitespace characters to simulate columns; use semantic tables or layout.

## Responsive type is a composition decision

A fluid heading can use bounded `clamp()` sizing, but avoid a viewport-only formula that fights text zoom. Allow min-width-zero wrapping in flex/grid children. Use intentional line breaks only for short art-directed titles and test a fallback without them; do not impose display breaks on translated prose. Balance/wrap features are progressive enhancements, not a solution for missing layout constraints.

At narrow width, adjust column structure and line length before shrinking text. A brand can retain expression through a changed crop, title silhouette or rhythm instead of keeping an impossibly wide title. Never truncate essential destination labels, errors or prices to preserve a screenshot.

## Verification record

Capture a wide heading/prose specimen and a narrow difficult-content specimen. Confirm the font actually loaded; inspect fallback, long labels, zoom and selected/error/disabled text. Check text/background contrast for every role and state using `hardlight_contrast` for supported opaque colors. Document the final role table in the shipped system, including exceptions and their reasons. Clean font tokens do not prove the page reads well: inspect hierarchy and rhythm in the actual composition.
