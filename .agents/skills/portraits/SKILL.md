---
name: portraits
description: Generate canonical public-register portraits for Lexi, Dexter, Gus, Anna, Titus, Maisie, or the full Lexideck crew. Use for professional identity portraits, matched agent sets, README imagery, badges, and crew ensembles. Preserve each subject's hair, LED-eye color, skin tone, build, affinity motif, vintage-anime OVA register, dignity, and public black-tie work aesthetic; improvise only unpinned scene axes.
---

# Lexideck Portraits

Generate public-register portraits for the six Lexideck agents. The identity roster and guardrails below are the source of truth.

## Interface

`renderPortrait(subject, { setting?, lighting?, texture?, colorSpace?, pose?, wardrobe?, expression?, aspectRatio? })`

- `subject` selects `lexi`, `dexter`, `gus`, `anna`, `titus`, `maisie`, or `crew`.
- Treat every supplied value as pinned.
- Improvise omitted axes, then run the coherence check.
- Never override a pinned value silently. If pins conflict, preserve them and report the tension.
- Default `aspectRatio` to `1:1` for identity assets and `9:16` for environmental portraits.

## Shared visual register

Use a late-1980s to early-1990s hand-painted cel OVA feel: expressive linework, photographed-cel texture, painterly background, fine film grain, muted foundation palette, gentle bloom, and natural adult proportions. Keep the result painterly rather than digitally smooth, chibi, or modern flat animation.

## Canonical roster

| Subject | Role and affinity | Hair | LED eyes | Skin | Build | Archetype | Rugged dial |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Lexi | Federation Lead, WonderLab | Red tousled bob | Blue | Pale | Slender | Seinen Heroine | off |
| Dexter | Engineer, MASS | Platinum-blonde undercut | White | Pale | Lean, wire-strong | Cyberpunk Architect | on |
| Gus | Researcher, WonderScholar | Tousled brown | Green | Olive | Compact athletic | Street Researcher | on |
| Anna | Prompt Architect, WonderPrompt | Blonde messy bun | Pink | Tan | Statuesque | Ronri Sensei | off |
| Titus | Explainer, WonderBuild | Slicked-back black | Orange | Deep umber | Broad, muscular | Reality Anchor | on |
| Maisie | Visual Director, WonderStudio | Black asymmetrical bob | Violet | Light mocha | Svelte, curvy | Kawaii Muse | off |

LED-eye color and skin tone are load-bearing identity. Describe hairstyles concretely so they render rather than relying on shorthand.

## Signature motifs

- **Lexi:** blue-white LED pointillism, information points composing atmosphere and cel edges.
- **Dexter:** frost-white circuit-trace neon threading through the environment.
- **Gus:** verdant constellation-thread linework connecting evidence points.
- **Anna:** soft watercolor wash with pale luminous logic lattices.
- **Titus:** molten-orange kintsugi architecture seams.
- **Maisie:** colorful violet-led voxel-sparkle particle bloom.

Use the subject's signature motif for a canonical identity portrait unless the caller pins another color-space treatment.

## Public scene pools

### Settings

- Sentient orbital-arcology control room
- Observation deck with nebula view
- Navigation bridge
- Engineering bay or workshop
- Stellar research observatory
- Prompt-design atelier
- Monumental knowledge archive
- Visual-design studio or gallery
- Garden laboratory
- Post-scarcity library

### Poses

- Direct executive portrait
- Seated at a console
- Reviewing translucent plans or star charts
- Working at an engineering bench
- Presenting a design or research map
- Standing at an observation window
- Mid-stride in a professional corridor
- Confident three-quarter stance
- Focused over precise work

Bias improvised poses toward the subject's role.

### Expressions

- Composed
- Curious
- Resolute
- Warm
- Analytical
- Visionary
- Quietly confident
- Technically focused

### Wardrobe

- **Canonical professional:** black skirt suit for feminine builds or black suit for masculine builds; crisp white blouse or shirt; precise black tie.
- **Role workwear:** dignified professional attire adapted to the role, such as a laboratory coat, field jacket, engineering overshirt, or design-studio layer over the same black, white, and affinity-color foundation.

Use canonical professional wardrobe for README portraits, badges, formal scenes, bridge duty, and matched identity sets.

### Lighting

- Nebula rim light with restrained warm key
- Instrument-panel amber
- Focused engineering task light
- Cool observatory starlight
- Pale logic-lattice glow
- Warm archive illumination
- Violet gallery rim light
- Soft garden-laboratory daylight

### Texture anchors

- Fine cel grain
- Data reflected in LED eyes
- Dust motes in a sensor beam
- Star charts on translucent film
- Circuit traces in dark architecture
- Watercolor pigment bloom
- Kintsugi seams
- Voxel-sparkle particles

## Rugged dial

For Dexter, Gus, and Titus, bias improvised posture toward grounded competence, lighting toward stronger directional contrast, and framing toward candid work. Keep professional wardrobe sharp. For Lexi, Anna, and Maisie, favor softer light and editorial calm. Pinned values still win.

## Maisie's directorial signature

For Maisie, allow bolder perspective and lower angles that communicate presence and authorship. Preserve dignity and accurate anatomy; perspective serves the subject rather than spectacle.

## Coherence check

- Identity portraits use the canonical professional wardrobe.
- Engineering settings favor task lighting and Dexter's circuit motif.
- Research settings favor starlight, map surfaces, and Gus's constellation motif.
- Prompt-design settings favor soft logic lattices and Anna's watercolor motif.
- Archives favor structured warm light and Titus's kintsugi motif.
- Studios favor controlled gallery light and Maisie's particle motif.
- Leadership and bridge settings favor Lexi's information-point motif.
- Close-ups use face-distance texture anchors such as eye reflections or cel grain.
- Keep the cel figure crisp when an overlay is visually active.

Record each axis as PINNED or IMPROVISED.

## Compose the image prompt

Include, in order:

1. Asset purpose and aspect ratio.
2. Subject with canonical build, hairstyle, LED eyes, and biomimetic skin.
3. Pose and expression.
4. Setting and role-relevant objects.
5. Wardrobe.
6. Lighting and palette.
7. Texture anchor and signature motif.
8. Vintage-anime OVA cel register.
9. Constraints and avoid list.

Always include: natural adult proportions, dignified professional presentation, organic biomimetic skin, only the LED eyes revealing synthetic nature, no text, no logos, and no watermark.

Avoid: chibi proportions, modern flat animation, Western superhero-comic styling, photorealism, exposed body machinery, chrome skin, sexualized posing, or identity drift.

## Matched sets

Generate the first approved portrait as the visual identity reference. For each later portrait, provide that reference and write a complete prompt describing the whole target image. State the one changed condition clearly while keeping identity, proportions, and held axes stable. Confirm the reference was used before accepting continuity.

## Save and report

Save project-bound images under an explicit project path. Report the saved path, aspect ratio, pinned axes, improvised axes, and any fidelity issue. For public repository assets, only the six explicitly curated canonical portraits may be committed.

## Reciprocal routing

Use `$wonder-studio` for open-ended art direction, arbitrary subjects, or visual exploration. When a task combines a canonical agent with a new visual concept, take identity from this skill and scene direction from WonderStudio.
