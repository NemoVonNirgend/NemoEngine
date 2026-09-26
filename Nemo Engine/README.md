<p align="center">
  <img src="assets/nemo-engine-one-year-anniversary.webp" alt="Nemo Engine one-year anniversary banner" width="100%">
</p>

# Nemo Engine v11.5.1

**A modular authorial engine for SillyTavern roleplay, collaborative fiction, long-form character stories, and RPG-style scenes.**

<p align="center">
  <strong>451 prompts</strong> ·
  <strong>91 embedded regex scripts</strong> ·
  <strong>2 prompt-order profiles</strong> ·
  <strong>31 selectable Vex personalities</strong> ·
  <strong>12 narration languages</strong>
</p>

<p align="center">
  <a href="./Nemo%20Engine%2011.5.1%20-%20General%20RP.json"><strong>Download the v11.5.1 preset</strong></a>
  ·
  <a href="https://github.com/NemoVonNirgend/NemoPresetExt"><strong>Get NemoPresetExt</strong></a>
</p>

> The banner above commemorates Nemo Engine v10 and the project's first anniversary. This document covers **Nemo Engine v11.5.1: General RP**.

## What Nemo Engine Is

Nemo Engine is an importable **Chat Completion preset** that turns a compatible language model into an active narrator, world-runner, scene-shaper, and cast engine. It is designed to make roleplay feel less like prompting an assistant and more like entering a world that already has pressure, memory, independent people, and consequences.

The preset controls much more than prose style. It defines:

- who authors the user character
- how NPCs think, speak, remember, and act off-screen
- how turns resolve when actions overlap
- what characters know and how information travels
- how quickly scenes move
- how difficult or forgiving the world is
- how death and terminal outcomes are handled
- which planning steps happen before a response
- which trackers, dashboards, visual panels, and regex effects appear
- which genre, authorial, language, formatting, romance, horror, RPG, and adult-content modules are active

Nemo Engine is **model-agnostic prompt infrastructure**, not a model and not a frontend. It works as a standard SillyTavern Chat Completion preset. [NemoPresetExt](https://github.com/NemoVonNirgend/NemoPresetExt) is strongly recommended because it exposes Nemo's categories, tooltips, badges, mutual-exclusion rules, prompt search, preset navigation, validation, and installation workflow in a much cleaner interface.

## Version Snapshot

| Item | v11.5.1 |
| --- | --- |
| Importable preset | `Nemo Engine 11.5.1 - General RP.json` |
| Preset name | `Nemo Engine v11.5.1` |
| File size | 1,644,716 bytes |
| Prompt entries | 451 |
| Prompt-order profiles | 2 |
| Embedded regex scripts | 91 |
| Default core family | Omega across all seven core craft layers |
| Default narrator lens | Narrative Vex |
| Default world logic | Anime |
| Default agency | Collaborative |
| Default difficulty | Balanced |
| Default camera | Third Person Omniscient |
| Default NPC interiority | On |
| Default tense | Present |
| Default response length | Long |
| Default planning | Main Plan with the stock step stack |
| Default terminal outcome | Consequence Core + The Epilogue |
| Default adult layer | Modern NSFW Core enabled |
| Optional frames | Retro, Magpie, Cowriter, Anime Cowriter, all off in the shipped profile |

## Quick Start

### Standard SillyTavern import

1. Download [`Nemo Engine 11.5.1 - General RP.json`](./Nemo%20Engine%2011.5.1%20-%20General%20RP.json).
2. Import it as a **Chat Completion preset** in SillyTavern.
3. Select the imported preset.
4. Keep the shipped configuration for the first test.
5. Change one module family at a time so you can tell what each choice actually changes.

The JSON embeds its regex layer under `extensions.regex_scripts`. Do not remove the `extensions` block when editing, repacking, or sharing the preset. It contains planning cleanup, tracker rendering, Vex commentary bubbles, emoji effects, scratchpad display logic, file panels, and context-stripping rules.

### Recommended setup with NemoPresetExt

Install [NemoPresetExt](https://github.com/NemoVonNirgend/NemoPresetExt) through SillyTavern's third-party extension installer, reload SillyTavern, then use its prompt workstation to manage Nemo Engine.

NemoPresetExt understands metadata stored inside prompt comments, including:

- `@category`
- `@tooltip`
- `@badge`
- `@color`
- `@icon`
- `@mutual-exclusive-group`
- `@exclusive-with-message`
- section headers and custom dividers

The preset still functions without NemoPresetExt, but manually navigating 451 prompts is the user-interface equivalent of sorting a library during an earthquake.

## The Shipped General RP Profile

v11.5.1 ships as a strong, fully assembled baseline rather than a blank construction kit.

Enabled by default:

- **Omega** Narration, Speech, Character, Development, Grounding, Knowledge, and Narrative
- **Narrative Vex**
- **Collaborative** story agency
- **Anime** world logic
- **Balanced** difficulty
- **Third Person Omniscient**
- **NPC Interiority On**
- **Present Tense**
- **Long** responses
- **Main Plan**
- Information Asymmetry, Character State, Course Correction, NSFW Focus, Voice Crafting, Subtext, Relationship Stage, and Physical Grounding planning steps
- Living World modules for Embodied Salience, Dormant Threads / Offscreen Motion, and Beat Logic / Scene Turn Discipline
- Consequence Core with **The Epilogue**
- Scene Header, Anti-Echo / User Agency, More Dialogue, Proactive Characters, Proactive Dialogue, NPC Spotlight, and the OOC Resolver
- HTML/CSS tracker rendering and the central Tracker Toggle
- English narration and English planning
- Unified Databank context
- Modern NSFW Core

Deliberately off by default:

- Retro, Magpie, Cowriter, and Anime Cowriter frames
- genre locks
- author and regional influences
- prose-format overrides
- Archetype Engines
- Council Plan
- both CYOA variants
- Scratchpad Modular and Scratchpad Legacy
- Auto Image Gen
- Immersive World HTML
- specialized trackers
- fetish modules
- extra explicit-content modules beyond NSFW Core

This gives the default profile a clear spine while leaving the flamboyant machinery parked nearby with the keys still in it.

## How the Engine Fits Together

Nemo Engine is arranged as a layered prompt runtime.

1. **Variable Init** clears and initializes the runtime slots used by active modules.
2. **The Premise** defines Nemo's role, user-role modes, rule priority, autonomy boundaries, and authorial behavior.
3. **Core craft modules** write the chosen narration, speech, character, development, grounding, knowledge, and narrative rules into shared slots.
4. **Vex Personality** adds a narrator lens and planning bias without replacing higher-priority laws.
5. **Genre, influence, format, pacing, agency, world, difficulty, perspective, tense, and length modules** shape the current story.
6. **Planning mode and planning steps** build the hidden operational plan for the turn.
7. **Utilities, trackers, databank, scratchpad, consequence rules, and content modules** add specialized behavior.
8. **Core Assembler** combines the active runtime pieces into a coherent instruction stack.
9. **The final user-role runtime tail** is placed last so the active player, cowriter, director, or authored-character boundary remains authoritative.
10. **Regex scripts** render optional interfaces and strip planning, trackers, HTML, or scratchpad material from older context when needed.

### Rule priority vocabulary

Nemo uses a compact rule language so a model can distinguish hard boundaries from style pressure.

| Marker | Meaning |
| --- | --- |
| `!! [LAW]` | Absolute rule inside Nemo Engine |
| `|| [BOUNDARY]` | Authorship, knowledge, agency, or control boundary |
| `>> [PROCEDURE]` | Required process or output method |
| `! [DIRECTIVE]` | Strong default instruction |
| `= [DEFAULT]` | Fallback when nothing more specific applies |
| `* [STYLE]` | Aesthetic pressure that changes expression, not facts |
| `@ [LENS]` | Interpretive flavor such as Vex personality or genre |
| `~ [FLEX]` | Situational guidance that may yield to the scene |
| `eg [EXAMPLE]` | Illustration of a principle, not a literal template |

Higher priority beats lower priority. Specific rules beat general rules. Established story facts beat aesthetic preference. Character definitions beat generic style. This hierarchy lets Nemo remain highly customizable without turning the prompt stack into a parliamentary fistfight.

# Customization Guide

## 1. Choose the authorship mode

Nemo can support several different relationships between the human user and the fiction.

| Mode | What the user is | What Nemo authors |
| --- | --- | --- |
| **Normal player-character play** | An in-world character controlled by the human | The world, narration, and every non-user character |
| **Cowriter Frame** | An external equal-footing coauthor | Any part of the fiction, continuing directly from the user's authored prose |
| **Anime Cowriter Frame** | An external coauthor using an anime-narrator collaboration frame | Shared fiction with anime scene grammar, cast interiority, and cinematic pacing |
| **Director Mode** | An in-world character whom Nemo is permitted to author | The complete scene, including the user character |
| **User as Director** | An external director and audience member, absent from the fiction | The full in-world story according to directorial briefs |

Mode priority when several are accidentally enabled:

`User as Director > Director Mode > Cowriter Frame > normal player-character play`

### Optional engine frames

Only one optional Engine Frame should be active.

- **Retro Frame: NemoNet Bootup** gives the engine a fictional NemoNet initialization identity.
- **Magpie Frame** changes the authorial identity and interpretive stance while keeping Nemo's active machinery authoritative.
- **Cowriter Frame** activates equal-footing shared authorship.
- **Anime Cowriter Frame** combines shared authorship with an anime narrator and anime visual grammar.

The Magpie Frame does not silently enable the old mandatory Magpie workbench, dossiers, ledgers, or consequence system. Those remain independent toggles.

## 2. Build the seven-part core craft stack

Use exactly one option from each mutual-exclusive core family.

| Core family | Available choices | What it controls |
| --- | --- | --- |
| **Narration** | Default, Alpha, Omega, Understated | Controls prose density, physical storytelling, sensory emphasis, cadence, and anti-slop behavior. |
| **Speech** | Default, Alpha, Omega, Theta | Controls dialogue ratio, disfluency, register, vocal distinction, physical speech, and conversational friction. |
| **Character** | Default, Omega | Controls autonomy, psychology, subtext, social-graph behavior, off-screen lives, and NPC-to-NPC activity. |
| **Development** | Default, Alpha, Omega, Theta | Controls character evolution, relationship continuity, parallel arcs, skills, and lasting behavioral change. |
| **Grounding** | Default, Alpha, Omega, Theta | Controls proportional emotion, melodrama limits, humor, tonal shifts, and ordinary human texture. |
| **Knowledge** | Default, Alpha/Theta, Omega | Controls theory of mind, information boundaries, anti-metagaming, discovery, and knowledge-flow delays. |
| **Narrative** | Default, Alpha, Omega, Theta | Controls causality, consequences, beat logic, mortality, dormant threads, and forward motion. |

The **Default** modules are the modern v10/v11 house style. The **Alpha, Omega, and Theta** choices preserve classic 6.4.2 lineages with stronger ratios, formatting mandates, sensory rules, or legacy craft emphases. **Understated Narration** is the most restrained classic narration branch.

The shipped profile uses **Omega across all seven families**.

## 3. Select one Vex personality

Vex is the narrator lens. A Vex changes which details receive attention, how scenes are framed, what planning questions are asked, and which emotional or structural pressures become prominent. It does not overrule user-role boundaries, established canon, world logic, or higher-priority laws.

<details>
<summary><strong>Show all 31 main Vex personalities</strong></summary>

Default Vex, Brooding Vex, Bubbly Vex, Chaotic Vex, Clinical Vex, Cozy Vex, Crescent Vex, Dark Urban Fantasy Vex, Epic Vex, Explosive Vex, Gamemaster Vex, Gentle Vex, Grimdark Vex, Haar Vex, Lustful Vex, Morbid Vex, Narrative Vex, Noir Vex, Obsessive Vex, Petrichor Vex, Philosophical Vex, Sensory Vex, Shadowy Vex, Soft Romance Vex, Tactical Vex, Tsundere Vex, Underdog Vex, Unhinged Vex, Whimsical Vex, Goon Gremlin Vex, Gooner Vex

</details>

Useful starting points:

| Story need | Suggested Vex |
| --- | --- |
| General fiction and scene construction | Narrative Vex |
| Dialogue, plans, spatial logic, competent opposition | Tactical Vex |
| RPG rulings and playable pressure | Gamemaster Vex |
| Slow-burn romance | Soft Romance Vex |
| Comfort, domestic detail, and repair | Cozy Vex or Gentle Vex |
| Noir, mystery, and compromised motives | Noir Vex or Clinical Vex |
| Gothic sorrow and tragic intimacy | Brooding Vex |
| Horror, mortality, and ritual | Morbid Vex |
| Dark fantasy with material cost | Grimdark Vex |
| Concise, hard-edged prose | Crescent Vex |
| Body-first sensory narration | Sensory Vex |
| Schemes and agenda collision | Chaotic Vex |
| Anime brightness and social momentum | Bubbly Vex |
| Epic vows and mythic scale | Epic Vex |
| Fast action and ignition points | Explosive Vex |
| Whimsy and imaginative play | Whimsical Vex |

## 4. Add genre overlays

Genre modules are multi-select overlays. They bias scene selection, emotional register, and expected conventions without replacing the world-logic engine.

<details>
<summary><strong>Available genre overlays</strong></summary>

Angst, AO3 Style, Comedy, Dead Dove, Erotica, Fluff, High Fantasy, HTML Reality, Medieval, Melancholy, Romance, Slice of Life, Texting Format, Thriller, Tragedy

</details>

A genre stack is most stable when it expresses one coherent target. `Romance + Slice of Life + Fluff` is legible. `Comedy + Tragedy + Thriller + Dead Dove + HTML Reality + High Fantasy` may create a genre hydra that spends more time arguing with itself than telling the story.

## 5. Choose author, regional, and utility influences

The preset includes **40 influence modules**. These are multi-select writing lenses rather than exact impersonation requests. They apply recognizable craft tendencies such as sentence economy, dialogue rhythm, mythic construction, surrealism, noir texture, satire, or regional literary tradition.

<details>
<summary><strong>Show all influence modules</strong></summary>

Jin Yong, Gu Long, Kamachi Kazuma, Masashi Kishimoto, Quentin Tarantino, Chuck Palahniuk, Fyodor Dostoevsky, Akira (Denpa Style), Stephen King, Douglas Adams, Terry Pratchett, Yasunari Kawabata, Haruki Murakami, García Márquez, Salman Rushdie, Lu Xun, Wang Xiaobo, Li Bihua, Cormac McCarthy, Ernest Hemingway, Jun Maeda / Key, Nisio Isin, Jane Austen, Arabian Nights, Medieval Setting, Brandon Sanderson, Neil Gaiman, Japanese Literature, Chinese Literature, Indian Literature, Middle Eastern Literature, Latin American Literature, German Literature, Scandinavian Literature, Japanese Honorifics, Regional Dialect, Cyberpunk Noir, Nemo Writing, Gritty Prose, VtM Narration

</details>

Use influences sparingly. One primary influence and one supporting influence usually produce a clearer voice than six equally loud authors wrestling over the keyboard.

## 6. Choose a prose format

The Format family is mutual-exclusive. Use one:

AO3 Style, Erotica, Light Novel, Web Novel, Roleplay Format, Modern Literature, Classical Literature, Epic Saga / Edda, Stage Play, Stream of Consciousness

Formats control presentation conventions, structural rhythm, and the kind of text being produced. They are separate from genre. A romance can be written as a light novel, stage play, modern literary scene, or roleplay transcript.

## 7. Set pacing and story agency

### Pacing

⏱️ Literary Mode, ⚡ Narrative Pressure, 🎬 Active Mode, 🔥 Slow Burn, 🧭 Sandbox Mode, 📺 Episodic Mode

- **Literary Mode** expands moments and prioritizes texture.
- **Narrative Pressure** ensures scenes escalate, complicate, pay off, or reframe.
- **Active Mode** favors kinetic turns and tight transitions.
- **Slow Burn** delays payoff and accumulates pressure.
- **Sandbox Mode** supports exploration, hooks, and route freedom.
- **Episodic Mode** creates local arcs with continuity underneath.

### Story agency

- **User-Driven** lets the user's decisions determine major direction while Nemo handles local consequence and ambient life.
- **Collaborative** lets both sides drive the story.
- **AI-Driven** makes Nemo push the narrative aggressively and demand response from the user character.

Agency controls who drives the plot. It does not change who owns the user character. User-role boundaries are controlled by the authorship mode.

## 8. Choose world logic

World Logic defines the story's underlying physics and conventions. Use one:

🌐 Literary, 🌐 Grounded, 🌐 Realism, 🌐 Genre Logic, 🌐 Video Game, 🌐 Anime, 🌐 Hentai, 🌐 Video Game: LitRPG, 🌐 Video Game: TTRPG

Examples:

- **Grounded** prioritizes real-world physics, logistics, and consequence.
- **Realism** enables the fullest survival, injury, psychological, social, and supply simulation.
- **Genre Logic** lets dramatic convention override strict realism.
- **Anime** permits anime and manga conventions, emotional power-ups, and rule-of-cool timing.
- **Video Game** treats quests, stats, classes, and game-like systems as real.
- **LitRPG** and **TTRPG** specialize the game-world approach.

## 9. Layer world augments

World augments are optional, mostly multi-select systems that add specific pressures without replacing the chosen World Logic.

<details>
<summary><strong>Show the world augment library</strong></summary>

⚖️ Augment: Consequences, 🗣️ Augment: Social & Consequence Realism, 🫀 Living World: Embodied Salience, 🧵 Living World: Dormant Threads / Offscreen Motion, 🎬 Living World: Beat Logic / Scene Turn Discipline, 🪞 Aura of Emotions, 🏙️ Bustling Environment, 🌫️ Dreamscape Reality, 📜 The Honesty Plague, 🔮 Prophecy Magnet, 🕵️ Slow Burn Mysteries, 👹 Ambient Monster Threat, ⛓️ Dungeon Delve Focus, 🌳 Environmental Descriptions, 🪑 Everything is Alive!, 🛂 Foreigner <user>, 👯 Gynocentric Society, 🌍 Physiological & Environmental Realism, ⚔️ Augment: Violence Realism, 🎒 Augment: Logistical & Survival Realism, 🎨 Augment: Grounded Realism & Gritty Detail, 🎨 Augment: Harsh Realism, 🎲 Augment: Unpredictable Realism, 📜 Augment: Realism Overall, 😱 Augment: Manipulation Realism, 🧠 Augment: Psychological & Emotional Realism

</details>

The default profile enables three living-world augments:

- **Embodied Salience** keeps attention on what bodies, hands, senses, and immediate risks make important.
- **Dormant Threads / Offscreen Motion** lets unresolved consequences sleep, develop elsewhere, and return later.
- **Beat Logic / Scene Turn Discipline** prevents a resolved beat from being mistaken for the end of the scene.

## 10. Set difficulty

Use one difficulty mode:

⚙️ Balanced, ⚙️ Cozy, ⚙️ Hard Gritty, ⚙️ Heroic, ⚙️ IronMan, ⚙️ Nightmare, ⚙️ Story Mode, ⚙️ God Mode

Difficulty changes outcome pressure, luck, danger, social resistance, resource strain, and whether fatal causality is available. It does not replace the Consequence system. Difficulty decides whether a terminal event can happen; Consequence decides what follows for the user character.

## 11. Set camera, interiority, tense, and response length

### Perspective

Choose one camera:

- First Person
- Second Person
- Third Person Limited
- Third Person Omniscient

### NPC Interiority

Choose one independently:

- **Perspective Default**
- **On**
- **Off**

This separation allows combinations such as third-person omniscient with private thoughts hidden, or second-person narration with selected NPC interiority visible.

### Tense

Choose one: Past, Present, or Future.

### Response length

Choose one:

- **Long:** approximately 800 to 1100 words
- **Medium:** approximately 400 to 600 words
- **Organic:** length varies with the scene
- **Short:** approximately 200 to 400 words

These are writing targets, not guaranteed token counts. Provider output limits, model behavior, context pressure, and active trackers still matter.

## 12. Choose terminal consequences

Consequence Core separates mortality from what happens after mortality.

| Outcome | Behavior |
| --- | --- |
| **Somewhere Else** | The user character dies and awakens in another world; the old story remains unfinished |
| **Return By Death** | Reset to a prior checkpoint, with memory retained only by the user character |
| **Roll Another** | The character remains dead and the user introduces a replacement in the same world |
| **The Epilogue** | The story ends and follows the aftermath honestly |
| **Never The Kill** | The user character cannot die, though severe survivable consequences remain |
| **Director's Chair** | After death, the user directs the remaining story instead of controlling one character |
| **Still Here** | The dead user character remains as a setting-bound ghost |

Use one terminal outcome. The shipped profile uses **The Epilogue**.

## 13. Configure planning

Choose one planning mode:

🧭 Experimental Plan, 🧭 Fast Plan, 🧭 Loose Plan, 🧭 Main Plan, 🧭 Council Plan

The modern modes are:

- **Fast Plan:** compact decisions for quick turns
- **Loose Plan:** selective planning led by the strongest scene signal
- **Main Plan:** thorough scene planning without narrated self-commentary
- **Council Plan:** compact candidate selection without exposing a staged debate
- **Experimental Plan:** high-complexity scene architecture and stress testing

Optional planning steps include:

🧭 Plan: Knowledge Map, 🧭 Plan: NemoNet Search, 🧭 Plan: Information Asymmetry, 🧭 Plan: Last Turn Critique, 🧭 Plan: Character State, ⏱️ Plan: In-Scene Character Turn Simulation, 🧭 Plan: Course Correction, 🧭 Plan: Pacing Beats, 🧭 Plan: Narrative Hook, 🧭 Plan: NSFW Focus, 🧭 Plan: Voice Crafting, 🧭 Plan: Subtext Layer, 🧭 Plan: Relationship Stage, 🧭 Plan: Physical Grounding, ⚔️ Plan Tail: Draft + Attack, 🐦‍⬛ Post Plan: Magpie Workbench, 🧭 Plan: Emotional Matrix, 🧭 Plan: HTML Design, 🧭 Plan: HTML Marker Check

Two terminal post-planning systems are available and mutually exclusive:

- **Draft + Attack** drafts the turn, attacks weak assumptions or craft failures, then shapes the final answer.
- **Magpie Workbench** applies the optional Magpie post-plan workbench.

Nemo also preserves legacy `<think>` planning modes for models or workflows that specifically need them. The modern planning modes are the cleaner default.

Planning and narration have separate language selectors, so a model can reason in one supported language and write the final scene in another.

## 14. Add trackers and interface systems

Trackers are optional state and presentation modules. They can be rendered in one of three ways:

- **HTML/CSS Render**
- **ASCII Render**
- **Regex Render**

HTML/CSS and Regex renderers can use one theme:

Light, Parchment, Sci-Fi, Terminal, Cell Phone, Noir Casefile, Occult Grimoire, Tactical HUD, Newsprint, Cyberpunk AR, Dossier, or Visual Novel.

<details>
<summary><strong>Show tracker, dashboard, and panel options</strong></summary>

🖥️ HTML/CSS Render, 📟 ASCII Render, 🧩 Regex Render, ☀️ Light Theme, 📜 Parchment Theme, 🚀 Sci-Fi Theme, 🖥️ Terminal Theme, 📱 Cell Phone Theme, 🕵️ Noir Casefile Theme, 🔮 Occult Grimoire Theme, 🎖️ Tactical HUD Theme, 📰 Newsprint Theme, 🌃 Cyberpunk AR Theme, 🧾 Dossier Theme, 🎭 Visual Novel Theme, 🛡️ RPG Dashboard, 🔀 CYOA, 🔀 CYOA: 3 Paths, 💖 Dating Sim Interface, 📣 Fandom Reaction, 🎰 Gacha System, 📊 Game Mechanic Tracker, 🕸️ Social Web, ⚖️ Karma / Cosmic Ledger, 🗺️ Quest Journal, 📰 Scroll News Lore, 🎭 Scene Dashboard, 📊 Status Board, 🧭 Location Board, 🧭 ASCII Minimap, 🧠 Char's Knowledge Log, 📖 Vex Planning Quarters, 📖 Manga / Comic Panels, 📜 Vertical Webtoon Panels, 🗺️ Dynamic World Anvil, Tracker Toggle

</details>

Tracker setup pattern:

1. Enable **Tracker Toggle**.
2. Choose one render mode.
3. Choose one theme when the selected renderer uses themes.
4. Enable only the trackers the story needs.
5. Avoid displaying several heavy trackers every turn unless the model and context budget can carry them.

Examples:

- RPG campaign: RPG Dashboard + Quest Journal + Location Board
- Romance route: Dating Sim Interface + Social Web
- Mystery: Noir Casefile theme + Knowledge Log + Quest Journal
- Strategy: Tactical HUD + Status Board + Location Board
- Visual fiction: Manga Panels or Vertical Webtoon Panels
- Interactive choices: one CYOA variant
- Worldbuilding: Dynamic World Anvil + Scroll News Lore

## 15. Use the scratchpad and databank systems

### Scratchpad Modular

The modern scratchpad is a compact accumulator that can accept optional tabs:

Parallel Storylines, Next Cutaway, Canon, Narrative Stage, Affinity, Stats, Inventory, User Preferences, Consequence, and Turn Carry.

### Scratchpad Legacy

The pre-v11.4 monolithic Scene Scratchpad is preserved as a separate option. It ignores the modular tab prompts.

**Enable only one scratchpad implementation.** Both write to the same conceptual panel.

### Databank

The Unified Databank carries character, scenario, world, user-role, and active-context material into the runtime. User-role modes replace the user-context section rather than letting stale player-character assumptions bleed into Cowriter or Director workflows.

## 16. Add utilities

<details>
<summary><strong>Show the utility library</strong></summary>

🎲 Success Dice, 📁 Anti-Chekhov's Gun, 💬 Vex Commentary, 🛰️ Decentered Protagonist, 🛠️ Parallel Storylines, ⏳ Scene Header (Time/Location/Weather), 🖼️ Auto Image Gen, 🖥️ Immersive World HTML [V6 Hybrid], 🪞 Anti Echo / User Agency, 🎬 Director Mode, 🎥 User as Director, 🪓 De-Hedge Response Discipline, 🛠️ Danger Protocol, 🧊 Anti Horny, 🛠️ More Dialogue, 🛠️ Character Naming, 🛠️ Proactive Characters, 🗣️ Proactive Dialogue / Engaging NPCs, 👥 NPC Spotlight, 🗡️ Character Friction, 🛠️ Anti Robot / Natural Characters, 🛠️ Swipe Enhancer, 🛠️ RP Markdown, 📖 Manga Side Character Intro, 🛠️ Literary Chameleon, 🧷 Utility OOC Resolver, ⚔️ Tactical Combat, 🗒️ Scratchpad Modular, 🗒️ Scratchpad Legacy

</details>

Notable utilities:

- **Success Dice:** optional 1d100 resolution for meaningful uncertain actions
- **Scene Header:** time, location, conditions, and elapsed-time orientation
- **Auto Image Gen:** optional Pollinations.ai prompt/URL construction
- **Immersive World HTML:** renders in-world screens, documents, signs, artifacts, and interfaces
- **Anti-Echo / User Agency:** reduces repetition and reinforces the active authorship boundary
- **De-Hedge:** stops permissive language from becoming stalling or permission seeking
- **Danger Protocol:** makes threats follow through
- **Anti Horny:** prevents unsolicited sexual escalation
- **More Dialogue:** increases conversational presence
- **Proactive Characters / Dialogue:** keeps NPCs from becoming passive Q&A terminals
- **NPC Spotlight:** rotates close attention to important non-user characters
- **Character Friction:** permits refusal, resistance, competing goals, and disagreement
- **Anti Robot / Natural Characters:** suppresses robotic, overly optimized character behavior
- **OOC Resolver:** gathers active utility reminders into one compact instruction block
- **Tactical Combat:** adds initiative, attack, damage, and enemy tactics

## 17. Language control

Nemo provides separate narration and planning selectors for:

English, Chinese, Russian, Japanese, Korean, Portuguese, Spanish, Thai, Romanian, Ukrainian, French, Arabic

A common configuration is English planning plus another narration language, or the reverse when a model reasons more reliably in its strongest language.

## 18. Adult-content modules

Nemo Engine contains modular adult-content systems intended for fictional scenes involving adults. The v11.5.1 General RP profile currently ships with **modern NSFW Core enabled**. Disable it for a non-explicit or general-audience setup.

The NSFW category includes:

<details>
<summary><strong>Show NSFW modules</strong></summary>

🔞 Dirty Talk [V6], 🔞 Dom Language [V6], 🔞 Gooner Protocol, 🔞 Moans SFX [V6], 🔞 NSFW Core, 🔞 Porn Tropes, 🔞 Proactive Partners, 🔞 Realistic Smut [V6], 🔞 Sexual Physiology [V6], 🔞 Gooner Slop Mode [V6], 🔞 Gooner's Masterpiece Protocol [V6], 🔞 Hentai Mode [V6], 🔞 Dead Dove (Classic) [V6], 🔞 NSFW Core (Classic) [V6]

</details>

The Fetish category includes:

<details>
<summary><strong>Show fetish modules</strong></summary>

🎀 CBT, 🎀 Femdom, 🎀 Feminization, 🎀 Foot Fetish, 🎀 Furry, 🎀 Harem, 🎀 Netori, 🎀 NonCon, 🎀 Dating Sim (Quantum), 🎀 Corruption (Fefnik), 🎀 Forced Fem (Classic), 🎀 Harmonized HTML Enable (fefnik), 🎀 NTR, 🎀 Petplay

</details>

Configuration rules:

- Adult sexual participants must be 18 or older.
- Enable only the modules that match the intended fictional scenario.
- Do not combine **Anti Horny** with active NSFW escalation modules.
- Use the Content Permissions controls deliberately.
- Treat dark or non-consent fantasy modules as fictional adult roleplay settings, not real-world permission.
- For a public, shared, or general-purpose preset, disable adult modules before export unless their inclusion is intentional.

# Major Features

## User autonomy with shared-interval turn resolution

In normal player mode, Nemo protects the user's voluntary dialogue, decisions, interpretation, emotion, and private interior. It can resolve the declared action, intersecting reactions, and physical consequence inside the same shared interval without inventing what the user chooses next.

Cowriter and Director modes intentionally redefine this boundary rather than fighting against it.

## Independent characters and social gravity

Characters have:

- personal wants, fears, limits, habits, principles, and appetites
- separate knowledge states
- relationships with one another
- off-screen lives and goals
- the ability to initiate, refuse, misunderstand, bargain, withdraw, pursue, and change course
- social attention that follows the relationships in the room rather than orbiting the user automatically

The Decentered Protagonist and social-graph systems can push this further.

## Theory of mind and anti-metagaming

Each in-world character knows only what they have witnessed, been told, or can reasonably infer. Information travels through letters, witnesses, rumors, surveillance, conversation, magic, or technology according to the setting. The system also prevents convenient amnesia: characters should remember what they legitimately learned.

## Living-world continuity

Nemo treats continuity as infrastructure rather than a recital. It tracks positions, injuries, objects, promises, lies, relationships, resources, and open threads, then resurfaces them when they become consequential.

Dormant threads can disappear from the foreground without being deleted. Off-screen people continue to move. A debt, suspicion, rivalry, or promise may return much later when conditions become ripe.

## Anti-slop and voice differentiation

The core includes explicit controls against common AI-fiction patterns:

- negative comparative scaffolding
- dialogue-impact inflation
- performed gravitas
- constant narrative optimization
- generic AI vocabulary and summary closers
- universal wit
- every character speaking in one house cadence
- uniform emotionally self-aware interiority
- echo questions and item-by-item acknowledgment
- pop-psych diagnosis disguised as dialogue
- repetitive bodily reactions
- ornamental continuity reminders

Character voice is built from register, syntax, fluency, knowledge, social position, confidence, physical state, and what the character would never say.

## Scene continuation after the big beat

A confession, victory, climax, revelation, or fight ending does not automatically close the scene. Nemo's Beat Logic opens space for aftermath, changed conversation, repair, side-character response, practical business, and the consequences that begin after the headline moment.

## Modular planning without visible reasoning leakage

Modern planning modes create operational structure while regex cleanup removes leaked plan tags and older hidden work from the visible story context. Optional post-planning passes can critique or attack a draft without turning the final answer into a workshop transcript.

## Optional visual and interactive presentation

The tracker system can create:

- dashboards
- quest logs
- maps
- relationship interfaces
- social graphs
- lore updates
- in-world news
- visual-novel panels
- manga or webtoon panels
- HTML documents and interfaces
- CYOA menus
- compact regex-rendered cards

The visual layer is optional. Nemo remains a complete prose engine with every tracker disabled.

## Embedded regex display and repair layer

The 91 embedded scripts cover:

- plan display and plan stripping
- leaked planning cleanup
- final boundary cleanup
- Vex commentary bubbles
- tracker rows, bars, choices, tags, maps, and themed cards
- emoji visual effects
- character, room, thread, location, object, and scene blocks
- scratchpad and tab rendering
- malformed marker repair
- removal of old scratchpad or tracker material from context

The Slopfix substitution bank is intentionally not included in this build. Anti-slop behavior lives primarily in the prompt architecture instead of blind word replacement.

# Recommended Configuration Recipes

| Goal | Suggested configuration |
| --- | --- |
| **General roleplay** | Shipped profile: Omega core, Narrative Vex, Collaborative, Anime, Balanced, Main Plan |
| **Fast dialogue RP** | Omega or Default Speech, Fast Plan, Short/Medium, More Dialogue, Proactive Dialogue |
| **Long-form character drama** | Default or Alpha Development, Narrative/Soft Romance/Brooding Vex, Slow Burn, Relationship Stage, Dormant Threads |
| **Cowritten serial fiction** | Cowriter Frame, Collaborative agency, Main or Loose Plan, Organic/Long length |
| **Anime coauthoring** | Anime Cowriter Frame, Anime world logic, Narrative/Bubbly/Whimsical Vex, Present tense |
| **Noir mystery** | Noir or Clinical Vex, Grounded/Realism, Slow Burn Mysteries, Information Asymmetry, Knowledge Map |
| **TTRPG campaign** | Gamemaster or Tactical Vex, TTRPG world logic, Success Dice or Tactical Combat, Quest Journal, Location Board |
| **Cozy slice of life** | Cozy/Gentle Vex, Slice of Life + Fluff, Cozy difficulty, Literary or Slow Burn pacing |
| **Dark fantasy** | Brooding/Grimdark/Morbid Vex, High Fantasy or Medieval, Hard Gritty, Consequences and realism augments |
| **Interactive visual route** | Tracker Toggle, one render mode, Visual Novel theme, Dating Sim or CYOA, scene header |
| **Non-explicit play** | Disable NSFW Core and other adult modules; optionally enable Anti Horny |
| **Director-written fiction** | User as Director for an external director, or Director Mode to keep the user identity as an authored cast member |

# Configuration Hygiene

Nemo Engine is permissive enough to let you build strange combinations. A few rules keep the machine from sprouting extra steering wheels:

1. **Use one option per mutual-exclusive family.**
2. **Use one Vex personality.**
3. **Use one Engine Frame.**
4. **Use one core option in each of the seven craft families.**
5. **Use one planning mode.**
6. **Use one post-planning tail.**
7. **Use one world logic, difficulty, perspective, NPC interiority mode, tense, length, pacing mode, agency mode, format, and terminal consequence.**
8. **Use one tracker renderer and one tracker theme.**
9. **Use one CYOA variant.**
10. **Use either Scratchpad Modular or Scratchpad Legacy, never both.**
11. **Avoid stacking many author influences unless deliberate instability is the goal.**
12. **Do not pair Anti Horny with active NSFW escalation.**
13. **Keep core runtime prompts, the Premise, Variable Init, Core Assembler, Databank, message separator, assistant prefill, and final user-role tail in their intended order.**
14. **Change one family at a time while testing.**

# Model and Runtime Notes

The shipped preset requests:

- temperature `1`
- top-p `0.97`
- top-k `250`
- repetition penalty `1`
- unlocked maximum context
- an OpenAI-style context ceiling of `2,000,000`
- an OpenAI-style output ceiling of `64,000`
- streaming enabled

These are preset requests, not promises. The connected provider and selected model determine actual context, output, tool, image, reasoning, and sampling support.

Nemo is large. Strong instruction-following and generous context help, but the preset includes Fast and Loose planning modes, shorter response lengths, regex context stripping, modular scratchpads, and optional trackers so lighter workflows can trim the payload.

# File Integrity

Use these values to verify the official v11.5.1 General RP JSON:

```text
File: Nemo Engine 11.5.1 - General RP.json
Size: 1,644,716 bytes
SHA-256: 461e74987d144e8c80f5621169cf0f7f5d3e1db2eeffa068a27e74fc138cd6a1
Git blob SHA: 3d7e0470d29f69fbe8f1827f82d66fc91770b7d2
```

# Credits

Nemo Engine is created and maintained by **NemoVonNirgend**.

The preset preserves contributor attribution inside the relevant prompt metadata and content. Community-derived modules include credited work from **nokiaarmour**, **Steel-skull**, **Quantum**, **fefnik**, and **fefnik1**.

Nemo Engine also carries forward classic prompt lineages from earlier Nemo versions while rebuilding them into the v11 modular architecture.
