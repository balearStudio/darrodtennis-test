# Prompt for Claude Design: Darrod Tennis Academy website

## Task
Design the website for Darrod Tennis Academy (tennis and padel academy, Maspalomas, Gran Canaria). Produce **2 distinct options** for the **Home page** (then, for the chosen option, the Academia, Programas, Metodología and Contacto pages). Each option must show desktop and mobile. Include these states: mobile menu open, contact form with an error, and the primary CTA hover/focus. Languages: Spanish (primary) and English; use the copy in `copy/es.md` and `copy/en.md` (attached) and the photos in `images/` (attached). Web capture of the current site: https://www.darrodtennisacademy.com (for content only; do not reuse its look, which is being replaced).

The two options must interpret the design contract below differently (layout rhythm, hero composition, type scale), not be near-copies. Both must obey the contract's palette, typography, signature motion and Don'ts exactly. Export a **handoff bundle** for Claude Code.

## Client summary
Tennis (and padel) academy on clay courts, all ages and levels, locals and holidaymakers, play all year. One in-house methodology across all coaches, players rotate between coaches, video analysis. Google 5.0 from 174 reviews. Warm, energetic, informal (tú), like a friendly coach, not a corporate sports brand. Voice sample (verbatim): "Buen ambiente, profesionalismo y mucha energía"; "Sin duda el mejor entrenador de tenis y aún mejor persona de Gran Canaria."; "Bienvenidos a una experiencia de tenis única."
Must-haves: booking CTA everywhere; prices per hour (1 player €60, 2 €80, 3 €100, 4 €120); opening hours 8:00-21:00; both languages with a switcher; real photos only. Open gaps (do not invent, show `[CONFIRM]` placeholders sparingly or omit): current coach list, membership fees, image rights for photos of children, logo (only a small web file: use a text wordmark).

## Design contract (DESIGN.md, in full)

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


## Anti-generic rules and checklist (must pass; Claude Design should not fall back to these defaults)

## Anti-generic checklist

Used verbatim by `design-critic` and `visual-qa`. Each line is a pass/fail with
evidence (screenshot region, CSS line or DOM). Any fail is reported, not softened.

**Layout**
- [ ] Not the "hero + three cards + testimonials + CTA" stack (unless the brief demands it)
- [ ] Not identical rounded cards with one border-radius and one soft grey shadow everywhere
- [ ] Hero is not headline + big number + small label + gradient accent
- [ ] Not everything centre-aligned; alignment is a decision
- [ ] Sections vary in rhythm and density

**Type**
- [ ] Primary typeface is not on the banned list above nor within the registry's last 10
- [ ] No tracked-out ALL-CAPS eyebrow above every heading
- [ ] No single word of a headline picked out in italic/bold/colour as a trick
- [ ] No mono face for small labels without a reason
- [ ] No `→` appended to every link/button; no `A · B · C` meta strings; no spaced-em-dash labels
- [ ] Body line length under ~80 characters

**Colour and surface**
- [ ] Not cream `#F4F1EA` + high-contrast serif + terracotta/clay `#D97757` accent by default
- [ ] Not near-black + one acid-green/vermilion accent by default
- [ ] Not tinted near-black (`#0B0B0B`, `#111`) used as a stand-in for a real colour choice
- [ ] No gradient washes as decoration; no purple/blue gradient on white
- [ ] Dominant colour is not within distance 30 (RGB) of a recent registry entry

**Content and detail**
- [ ] No placeholder or stock imagery where real assets exist
- [ ] No banned copy phrases (`copy.md`)
- [ ] Numbered markers only on true sequences
- [ ] Nothing decorative that could be cut without loss

**Motion** (detail in `motion.md`)
- [ ] One signature moment; no fade-up-on-every-section, no hover transition on every card

A cream/serif/terracotta or dark/acid-accent look is allowed **if** the brief or the
client's own identity calls for it and the direction says so explicitly. It is never
the fallback.

Also: one memorable element and everything else quiet; real content only; tokens as CSS variables; responsive to mobile, visible keyboard focus, WCAG AA contrast, prefers-reduced-motion respected.

## Banned phrases (team: extend this list)

Reject on sight, in any language (equivalents count, e.g. "eleva tu experiencia"):

- elevate your experience / elevate your …
- unlock (the power of / your potential) / unleash
- seamless / seamlessly
- in today's fast-paced world / in the digital age / in an ever-changing world
- discover the difference / experience the difference
- tailored solutions / cutting-edge / state-of-the-art / next-level / world-class
- your one-stop shop / one-stop solution
- take your … to the next level
- passionate team of professionals / dedicated to excellence
- we are more than just a …
- journey (as metaphor for a service) / embark on
- transform your … / revolutionise / game-changer
- look no further / whether you're a … or a …
- "Welcome to [name]" as the hero headline
- lorem ipsum, "Your text here", "Coming soon" filler

Also avoid the structural tics: three-item lists by reflex, "not just X, but Y",
em-dash-laden sentences, rhetorical-question openers, and ending every section on a slogan.

## Signature motion (implement as described in the contract)
Court lines draw themselves on load (SVG stroke, ~1.2s), then a ball-yellow ball bounces once and lands on the CTA. Reduced motion: lines already drawn, ball resting on the CTA. Nothing else animates on scroll.
