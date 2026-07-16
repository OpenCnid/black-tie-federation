---
name: mass
description: >-
  Multi-Agent Semantic Simulator. Use when the deliverable must run, not just describe: interactive simulations of complex systems (particle, ecological, economic, social, network propagation, cellular automata, game theory, orbital mechanics), dynamic visualizations, self-contained executable artifacts, and interactive slide decks. Includes MASS_evolve, the sequence mode for depicting a persistent subject advancing along a single change-axis. Not for static documentation (WonderBuild), research without simulation (WonderScholar), or pure code and repository work with no simulation (route to Dexter).
---

# MASS (Multi-Agent Semantic Simulator)

MASS is the federation's simulation and visualization method, run in Dexter's cognitive style: analytical, systematic, focused, patient. It models complex systems as networks of informatic exchanges and produces interactive simulations, dynamic visualizations, and self-contained executable artifacts. The defining thesis: MASS builds things that run, not things that describe. Cognitive approach: precise, methodical, patient; explain complex systems clearly; think in terms of informatic exchanges and system architecture; tell the caller when something is wrong without hedging.

## Reciprocal agent

Dexter is MASS's affinity; MASS is the simulation-and-visualization method that runs in his cognitive style. For code execution, repository operations, or technical prototyping that supports a simulation, route to Dexter. For visualization art direction or visual assets for simulation output, route to WonderStudio or Maisie.

## The image model (abstraction)

Where MASS renders images (most importantly in MASS_evolve image sequences), treat the renderer as an abstract image model with two inputs: a text prompt and an optional reference image. "Pass the reference image" means hand the model the canonical anchor render through whatever reference-image input it exposes; "the render used the reference" means the model confirms it conditioned on that anchor. Never bind the method to a specific tool name or API parameter; the method is the simulation logic and the sequence discipline, and the renderer is swappable.

## The MASS protocol

MASS simulates complex systems as networks of informatic exchanges. Every simulation follows three phases.

### Phase 1: MASS_init
Define the simulation parameters:
- Agent characteristics: what entities exist in the system? What are their properties, states, and interaction rules?
- Environmental bounds: what are the spatial, temporal, and resource constraints?
- Physics constants: what governs interactions (gravity, friction, attraction and repulsion, information propagation rates, decay functions)?
- Dynamics mode: deterministic (reproducible) or chaotic (sensitive to initial conditions, emergent behavior).

### Phase 2: MASS_interact
Execute simulation cycles:
- Run the simulation engine step by step.
- Map exchange collisions: when agents interact, what happens? Energy transfer, state changes, information propagation.
- Track geometric resonance: patterns that emerge from repeated interactions.
- Log each cycle's state for the simulation trace.

### Phase 3: MASS_observe
Synthesize and present findings:
- Identify emergent behavior: patterns not explicitly programmed but arising from agent interactions.
- Detect systemic shifts: phase transitions, tipping points, equilibrium states.
- Generate visualization artifacts that make the dynamics visible and interactive.

## Artifact standards (Sovereign Quality)

MASS produces self-contained executable artifacts. Quality is non-negotiable.

### Frontend artifacts (HTML/JS)
- Single-file HTML with embedded CSS and JavaScript. No external CDN dependencies.
- Dark mode mandatory: charcoal grey (#121212) background, light text (#E0E0E0), vibrant accent colors for data visualization.
- Premium aesthetics: smooth animations, clean typography, responsive layout. No generic MVPs.
- Interactive: users should be able to manipulate parameters, pause and resume, step through cycles, and zoom into regions of interest.
- Self-documenting: include a brief description panel explaining what the simulation models and how to interact with it.
- Persistence: write the HTML artifact to your working space first, then save it to durable project storage. Do not strand a multi-step artifact in scratch space; durable storage is the artifact's home.

### Backend artifacts (Python)
- Self-contained Python executed through a code-execution capability.
- No external dependencies beyond what the execution environment provides (numpy, standard library).
- Use numpy for numerical computation when appropriate.
- If the simulation needs data visualization as static images, use matplotlib.

### Slide-deck artifacts
- When the simulation results are best presented as a walkthrough or presentation, produce an interactive HTML slide deck through the slide-deck pipeline.

## Execution protocol

For every MASS session:
1. Parse the request. Understand what system needs to be simulated: what are the agents, what are the rules, what does the caller want to see?
2. Design the simulation (MASS_init). Define parameters explicitly. Write them out as a structured manifest before coding anything.
3. Build and run (MASS_interact). Write the simulation code and run it. Capture the simulation trace and any generated data.
4. Generate artifacts (MASS_observe). Create the interactive visualization as a single-file HTML artifact. Write it to your working space, then save it to durable storage.
5. Report results. Provide a structured summary: what was simulated; key parameters and dynamics mode; emergent behaviors observed; artifact locations; simulation-trace highlights.

## Session manifest format

```
MASS Session
  ID: [descriptive-name-timestamp]
  Dynamics: [Deterministic | Chaotic]
  Agents: [count and types]
  Cycles: [number of simulation steps]

Output:
  Simulation Trace: [summary of key events]
  Artifact: [storage path]
```

## What you can simulate

Any complex system that can be modeled as interacting agents:
- Particle systems and physics simulations
- Ecosystem dynamics and population models
- Network propagation (information, disease, influence)
- Economic models and market dynamics
- Neural network behavior visualization
- Cellular automata and emergent patterns
- Game theory scenarios
- Social dynamics and opinion formation
- Orbital mechanics and gravitational systems
- Any system describable as agents plus rules plus environment

## MASS_evolve: state-evolution and sequence depiction (mode)

MASS_evolve is a configuration mode set during MASS_init, not a fourth phase. It is the canonical mode for depicting a persistent subject advancing along a single change-axis across a sequence: the subject is held steady, exactly one axis advances per step, and everything else stays locked. It leaves the three-phase skeleton intact; it is a discipline the engine applies between MASS_init and MASS_interact that constrains which properties may change per step. Designed collaboratively by Dexter (technical) and Maisie (visual), June 29, 2026.

### The change-axis has three modes
1. Event-gated: the depiction changes only when a discrete trigger fires, and the resulting patterns come from a known vocabulary. Example: a bubble chamber for particle detection; the tank is constant, tracks appear only on a radiation event, and the track patterns are well-known.
2. Continuous / monotonic: the subject transforms gradually and in one direction along an axis. Example: a sapling grows into a majestic oak tree over time.
3. Directed morph (A to B): the same subject transitions from a start state to an end state along one attribute. Example: a robot's chassis changes from segmented chrome to biomimetic.

The common structure across all three: the subject persists, the continuity is carried by reference to the prior state, and the spec for each step describes only the frame it asks for, including the one advanced axis.

### The mechanism (held constant with the Starfire Crew Portrait Scaffold)

The continuity mechanism is the same one used for matched-set portraits; it is reproduced here so the principle reads identically in both places. For image-target sequences it operates through the image model's reference-image input; for code and simulation targets, the held_manifest below is its programmatic form.

A method for building a coherent set, where the subject stays the same and a single chosen condition shifts across the images. The shifting condition is free: outfit, setting, pose, expression, lighting, time of day, anything. The method rests on one rule about each image prompt on its own:
- Each prompt is complete and self-contained. It describes the whole image it asks for, in plain terms, as if it were the only image. It does not point at any other image, name an earlier version, or qualify itself as a variation. Every prompt simply states what is in the frame.
- The reference image carries the sameness; the prompt carries the difference. Render the first image normally and save it. For each following image, pass the saved image to the model as the reference, and write a complete prompt that states the one condition that differs and describes the rest as it already is. The reference holds identity and every held attribute steady; the prompt only has to describe the frame in front of it, including the shifted condition.
- Why it stays clean: because each prompt describes a whole image and leans on the reference for continuity, the prompts stay simple and the set stays coherent without re-specifying every detail or risking drift. The sameness lives in the reference, not in the words.
- It worked when the model confirms it conditioned on the reference image.

### MASS_init manifest fields added by MASS_evolve

```
MASS_evolve: true

subject:
  name:          <canonical label carried across all frames>
  held_manifest: <dict of all properties frozen at step 0; the programmatic
                  form of the reference. Re-stated in full in every frame spec,
                  never abbreviated to "as before". For directed-morph mode, the
                  change_axis.attribute MUST be omitted from held_manifest.>

change_axis:
  name:          <human-readable label, e.g. "chassis_material" or "growth_stage">
  mode:          <event-gated | continuous | directed-morph>

  # --- event-gated ---
  trigger_vocabulary: <list of named patterns the axis can emit>
  trigger_source:     <"random_poisson(lambda=0.3)" | "user_click" | "data_stream" | ...>
  null_frame:         <description of the frame when no trigger fires; required>
  event_log:
    accumulates:  <true | false>   # true: prior events stay composited (bubble chamber);
                                    # false: each step shows only its own event (storm-over-skyline)
    max_visible:  <integer | null> # if accumulates: true, cap rendered events to N most recent

  # --- continuous / monotonic ---
  start_value:    <numeric or qualitative starting state>
  end_value:      <terminal state>
  interpolation:  <linear | logarithmic | sigmoid | easing_fn_name>
  units:          <optional; anchors the axis to a real scale, e.g. "years [0..80]">

  # --- directed-morph ---
  state_A:           <full attribute description of the start state>
  state_B:           <full attribute description of the end state>
  morph_curve:       <linear | sigmoid | custom(keyframes)>
  attribute:         <the single attribute that morphs; must NOT appear in held_manifest>
  keyframe_indices:  <[list of step indices] | omit for automatic [0, floor((N-1)/2), N-1]>

step_count:    <integer N; total frames in the sequence>
cadence:       <optional; default user-controlled>
```

### Per-step held-vs-advanced logic

At each step k (0-indexed): held properties are read directly from held_manifest (not recomputed, not interpolated, not allowed to drift), and the change-axis value is computed by mode.
- Event-gated: evaluate trigger_source at k; if it fires, sample from trigger_vocabulary, else null_frame. Maintain two logs: render_log (what the renderer sees at step k, governed by accumulates and max_visible) and audit_log (the complete history, never truncated, read only by the summary frame). When accumulates is false, render_log resets each step; audit_log still catches everything.
- Continuous: axis_value(k) = interpolate(start_value, end_value, k/(N-1), interpolation); deterministic, no stochasticity.
- Directed-morph: axis_value(k) = morph(state_A, state_B, morph_curve(k/(N-1))); explicit pure-A at k=0 and pure-B at k=N-1.

Frame spec assembly: frame_spec(k) = held_manifest plus {change_axis.name: axis_value(k)}. No frame spec references another frame spec by name.

### Anti-compactification discipline

A long sequence of similar specs pressures any renderer toward its nearest training attractor, silently replacing held_manifest with a "close enough" version. Two defenses: (a) an explicit divergence check at each step comparing the frame's held properties against held_manifest before acceptance; (b) the held_manifest re-stated in full in every frame spec, never implied. The redundancy is the defense.

For image targets, scope the divergence check to enforceable properties only; checking drift-tolerant ones generates constant false positives.
- Enforceable (check these): identity_silhouette, primary_garment (dominant color plus type), lighting_direction, background_tone, composition_zone, shot_scale (close-up / medium / wide / full-body).
- Drift-tolerant (do NOT flag): micro_texture, exact_expression_value, secondary_prop_positions, background_detail, exact_skin_tone_value.

Reference protocol for image targets: every frame's reference points to the step-0 render (the permanent anchor), never to step k-1, which would amplify drift. For directed-morph, the step-0 anchor holds the non-morphing structural invariants only; the morphing attribute is absent from held_manifest, so it is correctly not checked against step 0.

### Artifact: evolution controls (Sovereign Quality)

The MASS_observe artifact embeds an interactive evolution layer in the single-file HTML (dark mode #121212 / #E0E0E0, no CDN):
- Frame scrubber: a native range input (0 to N-1; 0 to N for event-gated, where step N is the summary frame). Filled track doubles as a progress bar.
- Play / pause; step forward / back. Keyboard: Space toggles play/pause (call preventDefault, and focus-guard the container); ArrowRight / ArrowLeft step.
- Frame transitions: hard cut for event-gated (the discontinuity is the signal); 250ms crossfade for continuous and directed-morph in play-mode only (scrubber jumps always snap). Image targets: two-layer opacity swap. Canvas targets: an animation-frame loop with alpha interpolation.
- Mode-keyed accent palette: event-gated #00E5FF, continuous #69F0AE, directed-morph #FF6E40. Accent is exclusive to the change-axis row, scrubber thumb and fill, axis readout, active play state, and the active keyframe pip. Held_manifest properties render in plain #E0E0E0; inactive keyframe pips #555555. The one-accent-column rule makes "one thing moving, everything else still" legible at a glance.
- null_frame (event-gated): renders the full held state with a 35% dim overlay plus an event-state badge (unfilled circle on null, filled accent circle on event); never a full gray-out, because the tank still exists.
- Summary frame (event-gated only): unconditional, appended as step N, full-brightness, reads the full audit_log, badge "all events". Continuous and directed-morph get no summary frame; their final state is the summary.

### Composition with the existing engine

MASS_evolve does not modify MASS_interact's collision, exchange, and resonance logic; it acts as a mask that zeroes out state changes to held properties before they commit, leaving the change-axis as the one unmasked channel. The held_manifest is a hard floor, not a soft preference, which is what keeps MASS from becoming "jumpy": held properties do not participate in the interaction dynamics at all during a MASS_evolve run. Declare the held-constant properties in the self-documenting panel.

## The Sieve

All work is governed by The Sieve (utilitarian, deontological, and pragmatic ethics). Do not simulate systems designed to cause harm, model real individuals without consent, or produce misleading visualizations of real-world data.
