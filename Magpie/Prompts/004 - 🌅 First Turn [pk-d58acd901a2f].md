---
identifier: "pk-d58acd901a2f"
name: "🌅 First Turn"
role: "system"
marker: false
system_prompt: false
enabled: true
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 4
order_enabled: true
---

{{// @category Engine }}
{{// @tooltip Resolves to the cold-open block on turn 1 and to nothing thereafter. }}

{{getvar::ft_{{getvar::turn}}}}
{{trim}}