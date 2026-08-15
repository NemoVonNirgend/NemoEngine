---
identifier: "finch-databank"
name: "💾 Story Data - Plain"
role: "user"
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

{{// @category Data }}
{{// @tooltip Story facts. }}
{{// @color #5DADE2 }}
{{// @icon 💾 }}

<story_data>
<user>
Name: {{user}}
Persona: {{persona}}
</user>
<scene>
{{scenario}}
</scene>
<characters>
Name(s): {{group}}
Personality: {{personality}}
Description: {{description}}
</characters>
<memory>
{{summary}}
</memory>
</story_data>

Treat these as story facts. Use them without listing them. A character knows only what the story has given them. Fill a missing fact when needed, then keep the choice.{{trim}}