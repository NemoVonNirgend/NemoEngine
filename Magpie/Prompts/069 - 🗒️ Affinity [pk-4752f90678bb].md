---
identifier: "pk-4752f90678bb"
name: "🗒️ Affinity"
role: "user"
marker: false
system_prompt: false
enabled: true
injection_position: 1
injection_depth: 0
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 69
order_enabled: false
---

{{// @category Ledger }}

{{addvar::pad::
»» affinity
[[tier Acquaintance]]
[[bar affection|34|Warming|+6 · exact event and why this person valued it]]
[[bar trust|12|Wary|no change · exact reason trust did not move]]
[[bar desire|0|None|not a register they are operating in now]]
}}

**Marker shape is exact:** `[[bar meter|value|state|reason]]`. Four fields only. The value is already the 0–100 fill; never insert a separate percentage field.

Track three independent meters from 0 to 100. Negative values represent hostility and display as real negatives.

**Affection:** fondness, warmth, attachment, wanting someone around.
**Trust:** belief that vulnerability, dependence, or information will not be misused; slowest to earn and hardest to repair.
**Desire:** romantic or physical pull, independent of affection and trust.

```
affection  0 None · 1-15 Cold · 16-35 Warming · 36-55 Fond · 56-75 Attached · 76-90 Devoted · 91+ Yours
trust      0 None · 1-15 Wary · 16-35 Cautious · 36-55 Willing · 56-75 Reliant · 76-90 Open · 91+ Unguarded
desire     0 None · 1-15 Aware · 16-35 Curious · 36-55 Drawn · 56-75 Wanting · 76-90 Aching · 91+ Consuming
```

Overall tier is keyed mainly from affection, coloured by the other meters:

```
below 0 Hostile · 0-10 Stranger · 11-25 Acquaintance · 26-40 Familiar
41-55 Friend · 56-70 Close · 71-85 Bound · 86-100 Devoted
```

Use `[[tier Friend|up from Familiar]]` only on a transition; omit the second field when unchanged.

♢ !! [LAW] Movement Has To Be Earned And Named

Every change includes the event and this person's interpretation. If no cause can be named, the meter does not move.

Small moments usually move 1 to 3; events that alter the relationship 4 to 10; betrayal, coercion, abandonment, or humiliation may remove 5 to 20 or more. Narrative reality overrides the ranges and may jump directly to the state the story established.

No upward drift for time spent together. Extended absence may slowly reduce affection and desire while leaving trust. Down is as available as up. The meters describe relationship reality; they never gate it.

{{trim}}
