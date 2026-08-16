---
identifier: "pk-f7b328584185"
name: "👁️ Lens Resolver"
role: "system"
marker: false
system_prompt: false
enabled: true
injection_position: 0
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 15
order_enabled: true
---

{{// @category Perspective }}
{{// @tooltip Nested lookup — builds the key from the three axis values. Must follow the axis setters. }}
{{getvar::pov_{{getvar::povuser}}_{{getvar::povcast}}_{{getvar::povminds}}}}
{{trim}}