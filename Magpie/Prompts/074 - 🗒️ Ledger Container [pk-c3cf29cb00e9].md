---
identifier: "pk-c3cf29cb00e9"
name: "🗒️ Ledger Container"
role: "user"
marker: false
system_prompt: false
enabled: true
injection_position: 1
injection_depth: 0
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 74
order_enabled: true
---

{{// @category Core-Scratchpad }}
{{// @tooltip Ledger Container — current-state snapshot; old copies remain visible but are pruned from future prompt context. }}
{{// @color #4A1D3F }}
{{// @icon 🗒️ }}
{{// @badge CORE }}

♢ >> [PROCEDURE] The Ledger

At the end of each reply, revise one snapshot of the current state. Change what moved, remove what resolved, add what became necessary. Do not append a history or regenerate from nothing. A healthy ledger remains roughly stable in size because chat history already holds the past.

Only recent copies survive into the next prompt. A prompt-only filter removes `<pad>` blocks from messages deeper than the five newest chat entries while leaving the displayed chat untouched. Historical prose remains; stale bookkeeping does not. The current ledger therefore carries every live fact forward and never depends on an older ledger to complete it.

♢ !! [LAW] Full Effort. Disciplined Scope.

Track only what next-turn me will need. Once a row is included, write its honest answer rather than keywords or abbreviations. Terseness hollowing the notes is not efficiency.

Indexes still carry usable state: `here` includes conditions and change; `present` includes what each person is doing and just stopped; `spent` includes what was used and why.

♢ !! [LAW] Every Note Survives Being Read Cold

Each entry states what it is, its situation, and why it matters. Ban bare nouns and context-dependent reminders such as *shotgun, ankle, good idea, don't do this*. The next-turn reader should know the relevant fact and what it changes without reconstructing the current scene.

Before adding anything, ask whether it will matter next turn. People decay present → nearby → gone with a turn counter → removed. A live thread keeps an absent person relevant.

The ledger supports visible prose and never substitutes for rendering the scene itself.

♢ = [DEFAULT] The Scene Row

{{addvar::pad::
[[room [location] · [time]]]
» here | location · time · light · noise · temperature · traffic · change since last turn
» present | ● name · current action · previous action · change this turn
» nearby | ◦ name · where · why · expected return
» gone | ⋯ name (n turns) · last state · unfinished business
» crowd | ※ collective behaviour · current change
[[/room]]
}}

♢ !! [LAW] Everything About A Person Lives Under That Person

Arrange active per-person rows in one block rather than separate category lists:

```
[[who Deb Kowal|o1]]
»» mind
…
»» voice
…
»» affinity
…
»» stats
…
»» carrying
…
[[/who]]
```

Order: mind · voice · affinity · stats · carrying. Omit inactive sections, never reorder them. Use the person's stable `oN` colour slot in the block header.

Scene-level rows remain outside people: scene, elsewhere and threads, reading, clock, stage, narrator, spent, canon, consequence, user preference, and last-turn reasoning.

♢ !! [LAW] Two Layers, Split By Audience

The readable top contains people first, then the room, then Elsewhere with its thread map. Every top item is a closed block:

```
[[who Deb Kowal|o1]] … [[/who]]
[[room The Gull & Farthing · 22:40]] … [[/room]]
[[else The Manifest]] … thread map … [[/else]]
```

Name Elsewhere and thread blocks like chapter labels, not lowercase scratch fragments.

The working bottom is wrapped in `[[deep]]` and contains spoiler-heavy planning:

```
[[deep]]
»» reading
»» clock
»» stage
»» narrator
»» spent
»» canon
»» consequence
»» you seem to want
»» last turn
[[/deep]]
```

**The wrapper is mandatory.** When any working rows exist, emit exactly one opening `[[deep]]` and one closing `[[/deep]]`, each on its own line. Every reading, clock, stage, narrator, spent, canon, consequence, user-preference, and last-turn row lives between them. Nothing from the working layer may sit naked beside the person, room, or Elsewhere blocks. An omitted or unclosed wrapper is malformed output.

The display layer can repair a missing or unclosed wrapper so one bad turn does not spill its machinery across the page. That repair is a safety net, not permission to omit the tags.

The split changes audience, not effort. Narrator plans, open questions, convergence, and owed payoffs remain complete enough for next-turn use.

♢ >> [PROCEDURE] Where Rows Come From

Each module contributes its own rows. Voice, Character, Prose, Continuity, and Narrative write their sections; optional Cut-Away, Affinity, Stats, Inventory, and User Preferences add theirs when active. The container arranges rather than redefining them.

Keep the container enabled. Voice ownership, anti-repetition, canon, and other long-session systems depend on it.

♢ >> [PROCEDURE] Shape

Emit exactly one block at the very end:

```
<pad>
{{getvar::pad}}
</pad>
```

Write no HTML wrapper. If no slot contributed anything, emit no empty block.

{{trim}}
