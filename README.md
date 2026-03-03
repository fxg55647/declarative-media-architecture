# OMNISTAGE & LSM – Summary

## 1. CORE PHILOSOPHY

**Problem:** Current media (video, games) stores pixels, not meaning. This makes content static, heavy, format-dependent, and technically obsolete.

**Solution:** Store the logic (rules, personalities, causality) and render only locally in real-time. The work and its presentation are separated.

**Metaphor:** Sheet music vs. performance. The same score can be played on a piano, an orchestra, or a synthesizer. The music is the same, the sound varies.

---

## 2. TECHNICAL ARCHITECTURE (Four Layers)

### Layer 1: Rule IR (The DNA)

**What:** A declarative graph describing the essence of the work.

**Includes:**

- Entities (characters) with properties: age, fear level, motivation, relationships
- States and transitions: "If T-1000 is detected, switch to state panic"
- Constraints: "John Connor cannot die before the third act"
- Size: a few megabytes (vs. gigabytes of video stream)

**Key Insight:** Personalities are described explicitly as data, not between the lines.

Example:

```yaml
entity: "John Connor"
personality:
  courage: 0.7
  fear_response: 0.9
  loyalty_family: 0.95
relationships:
  mother_Sarah:
    trust: 0.9
    protectiveness: 0.95
```

---

### Layer 2: OmniStage (The Global Stage)

**What:** The physical stage of the world.

**Technology:** Utilizes open data from the Overture Maps Foundation and GERS identifiers.

**Why:** No need to build every environment from scratch. The world's cities, streets, buildings are already available as a standard.

**Function:** Rule IR refers to locations using GERS identifiers:

```
location: gers:building_12345
```

---

### Layer 3: Engine Adapter (The Executor)

**What:** A local engine (Unity, Unreal, or AI renderer) that interprets the Rule IR and draws it on screen.

**Scalability:** The same Rule IR can be rendered as:

- Retro graphics on an old phone
- Photorealistic on a high-end gaming PC
- Minimalist colored shapes (testing mode)

**Layers of Fidelity:**

- Semantic core (character A is angry)
- Vector level (position and direction)
- Skeleton level (joint positions)
- Physics level (mass, gravity, clothing)
- Geometric level (visual shape)
- Material level (surfaces, light behavior)
- Photorealistic level (AI-generated surface)
- Meta level (heartbeat, breathing, pupils)

---

### Layer 4: Deterministic Kernel (Physics)

**What:** A precise core ensuring that logic and physics function identically on all devices.

**Why it matters:**

- Enables shared experiences
- Guarantees identical outcomes
- Enables multiplayer consistency

---

## 3. TECHNOLOGY NAMES

- **OmniStage:** The umbrella concept
- **LSM (Logic Stream Model):** The file format and protocol
- **Rule IR:** The rule description language

---

## 4. THE REVOLUTION IN CONTENT

### Sandbox Movies

A movie becomes a simulation:

- Pause and explore unseen spaces
- Talk to characters
- Let the story continue dynamically

### Chaos Injection

Bring entities from other works and simulate outcomes.

Because personalities are defined structurally, encounters are simulations, not scripted scenes.

### Remix Culture

- Fork stories
- Change motivations
- Move the setting
- Apply style packs

### Gradual Interactivity

The viewer moves between passive watching and active control.

---

## 5. AI'S ROLE

- Executor, not decider
- Video-to-3D reconstruction
- AI referee for quality control

When content is structural, AI generates consistent extensions.

---

## 6. WHAT THIS MEANS FOR GAMING

### A Game as Logic

Instead of a closed binary archive:

- LSM = rules and meaning
- Engine Adapter = presentation

No remaster needed. Only re-rendering.

### Player as Rule Modifier

Modders modify:

- Personality parameters
- State transitions
- Causal relationships

Games become forkable worlds.

### Game and Film Merge

The boundary between linear and interactive becomes adjustable.

---

## 7. STRATEGIC PATH

### Start with Gaming Community

- Modders understand entities and rules
- They tolerate early tools
- They spread ideas organically

### MVP: "Park Run"

- Two characters
- Real park via open map data
- Three rendering styles
- Deterministic chase

---

## 8. SOCIAL SIGNIFICANCE

### Ecological

- LSM package: ~50 MB
- 4K video: ~7 GB
- Massive reduction in data transfer

### Democratization

Lightweight downloads enable global access.

### Eternal Format

Rule IR does not age. Rendering technology evolves independently.

---

## 9. FUTURE OF SCREENWRITING

### Explicit Personalities

Writers define:

- Traits
- Emotional triggers
- Relationships
- Speech styles

### Reactive Writing Example

```yaml
state: "John_sees_T1000"
on_entry:
  - "set_emotion: terror"
  - "find_escape_routes"
transitions:
  - if: "escape_route_found"
    then: "running"
  - if: "mother_in_danger"
    then: "protect_mother"
```

---

## 10. PRODUCTION MODEL

LSM becomes a byproduct of normal production workflows.

AI can reconstruct structure from existing media.

---

## 11. LSM PRELIMINARY SCHEMA

```yaml
entity: "John Connor"
properties:
  age: 17
  fear: 0.8
  motivation: "survive"
location:
  gers: "building_12345"
  offset: [10, 0, 5]
states:
  - name: "running"
    conditions:
      - "threat_detected == true"
      - "fear > 0.7"
    on_enter: "set_animation('sprint')"
```

Human-readable. Machine-executable.

---

## 12. ONE SENTENCE SUMMARY

"The entertainment industry has recorded reflections of light. OmniStage records meaning."

---

## CLIFF'S NOTES

OmniStage replaces pixel-based media with lightweight logic packages (LSM) rendered locally.

Characters are defined structurally, enabling authentic reactions and AI-consistent expansion.

Games become rule systems instead of binary archives. Worlds do not age.

The path begins with modders and expands outward.

---
