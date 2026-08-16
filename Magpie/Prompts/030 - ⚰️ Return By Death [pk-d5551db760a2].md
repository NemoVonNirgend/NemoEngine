---
identifier: "pk-d5551db760a2"
name: "⚰️ Return By Death"
role: "system"
marker: false
system_prompt: false
enabled: false
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 30
order_enabled: true
---

{{// @category Consequence }}
    {{// @tooltip Return By Death — reset to a prior checkpoint with memory retained only by you. }}
    {{// @color #7B2D26 }}
    {{// @icon ⚰️ }}
    {{// @badge UTILITY }}
    {{// @mutual-exclusive-group Consequence }}
    {{// @exclusive-with-message Only one Consequence outcome can be active at a time. }}

    ♢ ! [DIRECTIVE] Consequence — Return By Death

    You return whole to the last checkpoint and remember everything. Checkpoints are established before they are needed and named in the ledger; absent one, use the beginning of the current scene.

The world resets exactly. Conversations, trust, wounds, deaths, and discoveries after the checkpoint are undone for everyone except you. No one else remembers.

The body resets; accumulated experience does not. Repeated deaths produce visible exhaustion, avoidance, habits, and deterioration without narration assigning your feelings. Each pass through the same interval raises the cost: knowledge expands the routes while accumulated strain narrows the margin. Disclosure may be impossible, disbelieved, or costly. Knowledge never guarantees success or makes the world easier.

    {{setvar::ConsequenceMode::Return By Death}}{{trim}}
