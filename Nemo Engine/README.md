# Nemo Engine v12.5.3

A modular Chat Completion preset for character roleplay and collaborative fiction.

## Latest download

| Preset | Download | Use |
| --- | --- | --- |
| **Nemo Engine v12.5.3** | [Download JSON](https://raw.githubusercontent.com/NemoVonNirgend/NemoEngine/main/Nemo%20Engine/Nemo_Engine_v12.5.3.json) | Latest complete preset, published November 11, 2026. |

Import the complete JSON as a **Chat Completion preset** in SillyTavern. Keep its bundled regex enabled. Do not import it as a character card. [NemoPresetExt](https://github.com/NemoVonNirgend/NemoPresetExt) supplies the configuration interface.

## Previous v12.3 downloads

| Preset | Download | Use |
| --- | --- | --- |
| **Message Dock v12.3** | [Download JSON](https://raw.githubusercontent.com/NemoVonNirgend/NemoEngine/main/Nemo%20Engine/Nemo_Engine_v12.3_Message_Dock.json) | Previous version, including the optional Vex dock and Scratchpad integration. |
| **Standard v12.3** | [Download JSON](https://raw.githubusercontent.com/NemoVonNirgend/NemoEngine/main/Nemo%20Engine/Nemo_Engine_v12.3.json) | Previous version with standard visual novel Vex presentation. |

Both v12.3 editions use the restored October 18 configuration, mapped to the v12.3 Lite modules. Retro Frame and Response Structure Compiler are enabled. Vex Commentary is off in that restored configuration; enable it to use the portrait dialogue interface. The visual assets and optional features remain included.

### v12.3 configuration notes

- Exactly two depth-0 output points: Assistant Sudo Prefill and User Message Ender.
- Databank and lore grouped immediately above chat history.
- Current thought/backtick and coloured-dialogue rendering fixes.
- Vex portrait catalog and optional dock/Scratchpad presentation.

## Documentation and previous-version notes

- [Restored configuration and Full-to-Lite mappings](./docs/CONFIG_RESTORE.md)
- [Final-message assembly and module maintenance](./docs/TAIL_ASSEMBLY.md)
- [Validation reports](./docs/validation/)
- [Vex assets](./assets/vex/README.md)
- [Visual novel renderer](./assets/vex/renderer/README.md)
- [Message Dock setup](./assets/vex/renderer/message-dock/README.md)
- [Historical v12.1 section guide](./docs/v12.1-guide.md) — useful background; its edition counts and defaults describe v12.1.

## Archive

[Older presets](./Archive/) and [prompt history](./Archived%20Prompts/) remain available. The duplicate v12.2 download filenames have moved to [Archive/Compatibility](./Archive/Compatibility/); use the v12.5.3 download above for the latest version.

Portrait asset locations are unchanged.
