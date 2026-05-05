
<div align="right">
  <details>
    <summary >🌐 Language</summary>
    <div>
      <div align="center">
        <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=en">English</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=zh-CN">简体中文</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=zh-TW">繁體中文</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=ja">日本語</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=ko">한국어</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=hi">हिन्दी</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=th">ไทย</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=fr">Français</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=de">Deutsch</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=es">Español</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=it">Italiano</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=ru">Русский</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=pt">Português</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=nl">Nederlands</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=pl">Polski</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=ar">العربية</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=fa">فارسی</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=tr">Türkçe</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=vi">Tiếng Việt</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=id">Bahasa Indonesia</a>
        | <a href="https://openaitx.github.io/view.html?user=NemoVonNirgend&project=NemoEngine&lang=as">অসমীয়া</
      </div>
    </div>
  </details>
</div>

# NemoEngine

An archive of my SillyTavern presets — Nemo Engine, Atelier, and NemoNet.

## Repository layout

```
Nemo Engine/
  Nemo Engine 9.3.2.json        Current preset
  Archive/                      All past versions (5.4 -> 9.3.1)
    NemoSet/                    Themed v5.x variants
  Prompts/                      Extracted prompts from current version (one .md per prompt)
  Archived Prompts/             Per-version prompt history (sparse: only changes per version)
    CHANGELOG.md                Per-version delta summary
    INDEX.md                    Per-prompt version history table

Atelier/
  Atelier 1.2.json
  Prompts/

NemoNet/
  Nemo Net 1.0.json
  Prompts/

Templates/
  Alternate Prompts/            Optional add-on prompts (Council of Avi, Image Gen, etc.)
  Scenario Template/            Scenario starter
```

The `Prompts/` folder for each preset has one markdown file per prompt — frontmatter holds metadata (`identifier`, `name`, `role`, injection settings), body holds the prompt content. This makes it easy to grep, diff, and track how individual prompts evolve.

`Archived Prompts/` uses **sparse storage**: a prompt only appears in a version's folder if it changed (or was added) compared to the previous version. The oldest archived version is the baseline (all prompts present). Walk the folders newest-to-oldest with `CHANGELOG.md` to trace evolution.

## Setup tips

- If you're using qvink there seems to be an issue with the way tokens are counted.
- Set up your reasoning / start reply with the following settings inside Advanced Formatting if you're using the thinking prompt (i.e. 🧠︱Thought: Council of Avi!) — [example image](https://www.reddit.com/media?url=https%3A%2F%2Fpreview.redd.it%2Fnemoengine-v5-4-preset-primarily-for-gemini-2-5-flash-pro-v0-8t2ss711xa2f1.png%3Fwidth%3D423%26format%3Dpng%26auto%3Dwebp%26s%3D6cddf9cab5e52ddf6fc6b65cd74252c1008d8c62)
- If your message is getting cut off halfway, try enabling show `{{user}}` and show `{{char}}` in chat under user settings — this can fix it.
- On the latest SillyTavern staging branch with post-processing, refusals are much more common. Strict mode works for most people; otherwise try rolling back.
- For an out-of-the-box experience, see the variants under `Nemo Engine/Archive/NemoSet/` — none of them include the optional NSFW stuff and they're a good starting point to mess around with.
