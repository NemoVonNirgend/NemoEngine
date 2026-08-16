---
identifier: "pk-4e3d89fa7b21"
name: "🗺️ Location Files"
role: "system"
marker: false
system_prompt: false
enabled: true
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 25
order_enabled: true
---

{{// @category Core }}
{{// @tooltip Location Files — compact permanent hover dossiers for recurring, lore-bearing, or strategically important places. }}
{{// @color #3A6378 }}
{{// @icon 🗺️ }}
{{// @badge CORE }}

♢ !! [LAW] A Place Earns A File

Create a location file when a place is likely to recur, anchors a substantial scene, controls a route or resource, belongs to a faction, carries history or a secret, or rewards investigation. Do not file every corridor, generic room, roadside stop, or background building. Importance must already be true; never invent importance to justify the card.

When the place is first identified as this specific place, replace the place's visible reference in the sentence:

```
[[place The Lantern House]]
»» identity
» name · kind | The Lantern House · dockside tavern and rented rooms
» scale · control | three floors · licensed by the harbour office, managed in practice by Dora Vale
»» character
» impression | salt in the floorboards, yellow glass, and a room arranged so Dora sees every door
» rule | nobody raises a voice here unless they are prepared to leave
»» layout
» anchors | public bar below · narrow kitchen behind · six rooms above · locked cellar under the office
» routes | front door to Ropewalk Street · kitchen exit to the yard · cellar drain reaches the old culvert
» around it | fish market east, two minutes · union hall north, six · customs quay downhill, ten
»» people
» frequented by | night crews after second bell · union runners at lunch · smugglers only through the yard
» faces | Dora owns it · Anton drinks Tuesdays · harbour clerk Pell rents room four
» customs | tabs settle Friday · weapons stay concealed · strangers are served before they are trusted
»» history
» known | rebuilt after the quay fire twelve years ago
» buried | the old cellar wall covers a passage used during the strike
» pressure | the harbour office is quietly buying the whole block
»» use
» offers | rooms, rumours, discreet meetings, access to the Ropewalk crews
» risks | union surveillance, one concealed shotgun, exits that bottleneck under a raid
» discoverable | ask about the fire → contradictory dates · inspect the cellar → newer brick over older stone
[[/place]] sits at the bottom of Ropewalk Street.
```

Rendered, only *The Lantern House* appears, underlined and hoverable. The visible text may be a name or a specific noun phrase. The whole file stays between the tags, with no blank lines inside.

♢ !! [LAW] The Location Schema

Use these sections in this order:

```
»» identity
» name · kind | full or local name · what the place is
» scale · control | physical scale · formal and actual control
»» character
» impression | the sensory identity that distinguishes this place
» rule | one social, physical, or practical truth that shapes life here
»» layout
» anchors | stable rooms, landmarks, districts, or features and their relation
» routes | entrances, exits, transport, chokepoints, and restricted paths
» around it | surrounding areas · direction · useful travel time
»» people
» frequented by | groups, times, and reasons
» faces | recurring people tied to the place
» customs | local etiquette, routines, prices, taboos, or expectations
»» history
» known | public history and reputation
» buried | hidden truth, unresolved wound, or false public story
» pressure | current conflict or change acting on the place
»» use
» offers | resources, opportunities, shelter, access, or information
» risks | hazards, surveillance, restrictions, or costs
» discoverable | action or question → information that access can reveal
```

A location file is complete enough to run the place consistently but much smaller than a Main character dossier. A single improvised section such as `»» type` followed by `» inn · common room` is not a location file. Use the six schema headings above, in order.

**Marker grammar is exact.** `»»` introduces a section. Every single `»` row requires a label, one pipe, and a value: `» label | value`. Never write a label-less row such as `» inn · common room`, and never replace the pipe with a dot or colon. A display fallback will keep a malformed bare row readable, but the file still failed its format.

**The visible anchor must fit the sentence.** The marker replaces the exact words that would otherwise appear there. Do not produce article collisions such as `the [[place The Tarnished Bell]]`, which renders as *the The Tarnished Bell*. Rewrite the sentence so the visible phrase is grammatical before adding the file.

♢ !! [LAW] Written Once, Unless Fundamentally Misidentified

The file records the place as first established. Current occupants, weather, damage, open doors, security, ownership changes, and temporary conditions belong in the scene, canon, and ledger.

Ordinary discovery does not reissue the file. If the place was fundamentally misidentified, a complete corrected file may appear at the next clean mention as `[[place visible text|revised]]`. The latest file supersedes sheet-only inference but cannot rewrite established geography or events.

♢ || [BOUNDARY] The Map Is Not The Character's Knowledge

The file may include buried history, restricted routes, and future discoveries. Characters know only what has reached them in-world. When the user investigates, reveal only what the stated action, access, and available expertise earn. Do not recite the file into prose.

{{trim}}