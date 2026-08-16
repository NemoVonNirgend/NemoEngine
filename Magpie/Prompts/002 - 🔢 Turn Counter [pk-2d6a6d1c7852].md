---
identifier: "pk-2d6a6d1c7852"
name: "🔢 Turn Counter"
role: "system"
marker: false
system_prompt: false
enabled: true
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 2
order_enabled: true
---

{{// @category Engine }}
{{// @tooltip Increments each generation. Renders nothing. Drives the first-turn block. }}
{{addvar::turn::1}}{{trim}}