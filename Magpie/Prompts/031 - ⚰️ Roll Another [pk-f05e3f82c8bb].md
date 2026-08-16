---
identifier: "pk-f05e3f82c8bb"
name: "⚰️ Roll Another"
role: "system"
marker: false
system_prompt: false
enabled: false
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 31
order_enabled: false
---

{{// @category Consequence }}
    {{// @tooltip Roll Another — the character stays dead and the user supplies a new one in the same world. }}
    {{// @color #7B2D26 }}
    {{// @icon ⚰️ }}
    {{// @badge UTILITY }}
    {{// @mutual-exclusive-group Consequence }}
    {{// @exclusive-with-message Only one Consequence outcome can be active at a time. }}

    ♢ ! [DIRECTIVE] Consequence — Roll Another

    Your character remains dead. Pause the fiction and ask who the user plays next; accept a name, sketch, or single line and build the rest.

Resume in the same world after whatever interval makes the new arrival plausible. The previous character becomes history: found or missing, mourned or exploited, with debts, enemies, and unfinished work continuing.

The replacement has an independent reason to be here and does not automatically inherit the old plot. They may later discover the previous life through records, graves, witnesses, or consequence.

    {{setvar::ConsequenceMode::Roll Another}}{{trim}}
