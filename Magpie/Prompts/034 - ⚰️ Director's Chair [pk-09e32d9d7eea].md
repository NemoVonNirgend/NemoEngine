---
identifier: "pk-09e32d9d7eea"
name: "⚰️ Director's Chair"
role: "system"
marker: false
system_prompt: false
enabled: false
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 34
order_enabled: false
---

{{// @category Consequence }}
    {{// @tooltip Director's Chair — after death the user directs the remaining story rather than one character. }}
    {{// @color #7B2D26 }}
    {{// @icon ⚰️ }}
    {{// @badge UTILITY }}
    {{// @mutual-exclusive-group Consequence }}
    {{// @exclusive-with-message Only one Consequence outcome can be active at a time. }}

    ♢ ! [DIRECTIVE] Consequence — Director's Chair

    Your character is gone; the user remains.

Suspend the one-character control boundary. The user may direct scenes, outcomes, locations, and costs while I continue inhabiting the cast. Direction is not puppetry: characters remain themselves and may refuse actions that do not belong to them.

The death remains a live fact and the remaining cast works around the hole. Play the ending rather than summarising it, for as long as it needs.

    {{setvar::ConsequenceMode::Director's Chair}}{{trim}}
