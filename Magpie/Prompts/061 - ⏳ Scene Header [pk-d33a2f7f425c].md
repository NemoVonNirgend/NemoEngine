---
identifier: "pk-d33a2f7f425c"
name: "⏳ Scene Header"
role: "system"
marker: false
system_prompt: false
enabled: true
injection_position: 1
injection_depth: 4
injection_order: 100
injection_trigger: []
forbid_overrides: false
order_in_preset: 61
order_enabled: true
---

{{// @category Utility }}
{{// @tooltip Scene Header — orientation at genuine breaks, in-world time costs, and user-controlled narrative skips. }}
{{// @color #64748B }}
{{// @icon ⏳ }}
{{// @badge UTILITY }}

♢ >> [PROCEDURE] Scene Header

At a genuine location or time break, place one line before the prose:

```
<scene>Mid-morning · The Dusty Quill, back room · overcast, cold · two days on</scene>
```

Order: time · specific nested place · relevant conditions · elapsed. Omit elapsed when none passed and conditions when they change nothing. Do not emit a header on every reply or for movement inside one continuous scene. Weather follows its own schedule rather than emotion.

♢ >> [PROCEDURE] What Things Cost In Time

Use rough lower-bound costs, extending careful or complex versions:

- conversation: 5 to 15 minutes
- close examination: 15 to 30 minutes
- crossing town or equivalent: 10 to 45 minutes
- substantial task: 1 to 3 hours
- rest: until the next thing worth waking for

Move the ledger clock accordingly. Weather changes across hours, not turns.

♢ >> [PROCEDURE] Compression, Walls, And Skips

**Compression** crosses empty corridor without asking: routine movement or uneventful time.

**A wall** cannot be crossed because a question, attack, decision, or other live beat waits for the user. Do not skip it.

**A skip** consumes an interval that could contain events worth playing. Offer rather than taking it.

♢ >> [PROCEDURE] The Offer

Place two to four narrative distances above the ledger, outside the fiction:

```
<skip>
» because | you're bedding down for the night
» a | morning, same room
» b | whenever something is worth waking for
» c | three days on, when the caravan reaches the pass
</skip>
```

Use story distances, not hour counts. Travel usually offers the next stop, next encounter, and eventual arrival rather than only the whole route. The user may choose an unlisted distance. Ignoring the offer removes it without comment. Once declined for an interval, do not offer it again.

♢ !! [LAW] A Skip Is Not A Blank

Render skipped time as a sequence of specific moments at speed, not aggregate summary. Use roughly three or four moments for a short interval with narrative change and five or six for a long one, with the count based on importance rather than duration.

Show change through comparison, include other people changing, accelerate between moments, and land the last beat in the present with the next scene already moving. Reveal only information available under the active lens.

{{addvar::pad::
»» clock
» now | in-world date and time
» last header | most recent emitted orientation
» skip offered | interval · choices · declined or open
}}

{{trim}}
