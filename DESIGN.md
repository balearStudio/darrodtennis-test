# DESIGN: Darrod Tennis Academy

**Aesthetic:** clay-court graphic
**In one line:** the page is the court seen from above: real clay red, white court lines as the grid, one ball-yellow accent, for a warm, coach-led academy where the place itself is the proof.
**Sector:** sports academy  ·  **Languages:** es, en  ·  **Chosen:** 2026-09-19, admin

## Palette
| Name | Hex | Role |
|---|---|---|
| Clay | #B4472B | dominant / background |
| Line | #F7F1E8 | text on clay, court-line rules |
| Ball | #F2C230 | accent, primary CTA only |
| Ink | #2A1610 | text on light surfaces |
| Sand | #E9D6BF | surface |
Contrast check: Line on Clay 4.82:1 (body ok). Ink on Clay 3.18:1, so **never** set Ink on Clay. Ink on Ball 10.27:1. Ball on Clay 3.23:1 (non-text only).

## Typography
| Role | Typeface | Source | Weights |
|---|---|---|---|
| Display / headings | Archivo, expanded width (wdth 125) | Google Fonts | 800 |
| Body | Archivo | Google Fonts | 400, 600 |
Scale: base 17px, ratio 1.333, sm 0.85 / base / lg 1.33 / xl 1.78 / 2xl 2.37 / display clamp(2.4rem, 7vw, 5.5rem). Line-height 1.5 body, 1.0 display; measure ≤ 65ch.
Treatment: headings uppercase, tight (-0.01em), set like court signage; body sentence case.

## Layout and spacing
- Grid / alignment: 12-col, left-aligned; 1px Line-colour court lines mark the grid and section edges; sections differ in rhythm.
- Spacing feel: generous around the hero, dense in the drill and scoreboard sections; base unit 8px.
- Hero: full clay field, photo (site-19) in a line-bounded box off-centre, headline overlapping its edge.
- Radius / borders / shadows: 0 radius, no shadows; 1px Line rules are the only ornament.
- Sections: programmes as a court diagram (singles/doubles boxes), Metodología as a numbered drill sequence (a true sequence), team as a scoreboard-style table, booking with the Ball CTA.

## Imagery
Full-colour real photos, cropped tight to a court line, no filters. Hero: `site-19` (kids on clay); wide band: `site-20`. All from the client's own site and socials. **Open:** reuse rights and parental consent for photos of children (brief GAPS); logo exists only as a small 400×200 web file.

## Signature motion
- Moment: on load, the court lines draw themselves (SVG stroke, ~1.2s), revealing the grid; a Ball-yellow ball bounces once and lands on the CTA.
- Why it fits: the page is a court; the lines and the ball are the sport.
- Durations/easing: fast 200ms, base 400ms, slow 1200ms; ease `power2.out`.
- Reduced-motion fallback: lines already drawn, ball resting on the CTA.
- Everything else: restrained; user-triggered motion only (menu, form feedback). No fade-up on sections, no hover lift on cards.

## Voice
Warm, energetic, personal, informal (tú); like a friendly coach, not a corporate sports brand. Real customer language from the brief's voice sample, original language ("Buen ambiente, profesionalismo y mucha energía"). Reviews are quoted as reviews, never re-voiced as brand copy.

## Do
- Use court geometry (lines, boxes, numbering of real drills) as structure.
- Keep Ball yellow for the primary CTA only.
- Use real photos and real coach names once the client confirms who is current.
- Write es and en each naturally, not word-for-word.

## Don't
- Set Ink text on Clay.
- Add raspberry or the old script font (the current identity is dropped by choice).
- Add stat strips, eyebrow labels, or numbered markers on non-sequences.
- Invent testimonials, stats or team bios; mark unknowns `[CONFIRM: …]`.

## Banned for this client
- Global: the anti-generic checklist (`guidelines/aesthetics.md`) and banned phrases (`guidelines/copy.md`)
- Registry: typefaces Roboto, Space Grotesk, Brillante, Editorial Today, Grift, Schibsted Grotesk; aesthetic `dark-editorial-sport` in sports-academy (the `darrodtennis` seed); near-cream dominants (panespatagonia, finaivicenc). No override logged.
- Client-specific: the current site's raspberry/script look; dark video-hero editorial (already the seed).

## Registry entry (for `registry.mjs add` after approval)
Archivo · none · #B4472B · #F2C230 · clay-court-graphic · framed-clay-field-offset-photo · court-lines-draw-then-ball-bounce · sports-academy
