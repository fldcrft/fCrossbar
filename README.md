# fCrossbar (Alpha Release)

**fCrossbar** is a full-featured, ultra-lightweight Windower add-on designed to improve quality of life for both experienced and new Final Fantasy XI players through a modern hotbar and controller crossbar, while maintaining an extremely small memory footprint.

It's a lot, but I'd strongly recommend reading through the feature list to really understand how much work and thought has gone into this project. It may look overwhelming at first, but once you go through it, you'll see that the actual experience is designed to be simple and intuitive.

If you enjoy the project and want to support continued development, please consider donating.

<sub>Copyright © 2026 fieldcraft. All Rights Reserved.</sub>

<details>
<summary><sub>License and usage terms</sub></summary>

The source code for **fCrossbar** is made publicly available for viewing and **personal use only**.

**You may not** redistribute, republish, modify, create derivative works from, rebrand, sublicense, sell, or commercially exploit this software or any substantial portion of its source code without prior written permission from the copyright holder.

Permission is granted to download and use unmodified copies of **fCrossbar** for personal, non-commercial use.

This software is provided **“as is,” without warranty of any kind.**

</details>

> **Documentation and additional project information are still in development.**

## Core Architecture Features

- Ultra-lightweight, minimal codebase with memory usage below **600 KB** under normal testing conditions.
- Setup mode typically uses approximately **800–950 KB** of memory while active.
- Release builds are expected to use slightly less memory due to code cleanup and packaging.
- Steam Deck / Steam-friendly design.
- Fully mappable action bars for **Abilities, Magic, Weapon Skills, Trusts, Items, Mounts, and more**.
- Dynamic main-job and subjob action filtering.
- Character-specific **Job / Subjob profile support**.
- Cooldown, resource, and action-state feedback.
- Designed around low runtime overhead, minimal polling, stable performance, and avoiding unnecessary background work.

### 0.1 Controller UI

Controller crossbar layouts are supported for **PlayStation, Xbox, Steam, and Nintendo-style controllers**.

These are primarily visual button-label variants rather than completely separate UI systems for each controller. The actual controller mapping layer is handled through Steam, and I plan to release controller layouts as requested and provide support where needed.

The goal is to let the controller feel natural without forcing fCrossbar to maintain multiple redundant input systems.

### 0.2 Keyboard / Mouse UI

The hotbar is fully usable through mouse clicks or keyboard hotkeys.

Native Final Fantasy XI keybinds naturally limit some available keys, but additional bindings can be extended manually through the settings if you know what you're doing and want more control.

### 0.3 Logical Hotbar Design

**Informative, but minimal.**

For this iteration of the project, I deliberately chose not to use custom skill artwork or heavily graphical buttons. I want the player's focus to remain on the game itself rather than turning the interface into a collection of decorative glyphs.

The typography, state changes, borders, timers, and informational cues are designed to give you what you need without becoming visually noisy.

- **Dynamic Weapon Skill swapping** — when you switch weapons, assigned Weapon Skill slots can automatically update to the Weapon Skills available for the equipped weapon.
- **Cooldown timers** with an hourglass-style visual animation.
- Where applicable, abilities automatically choose logical targets. For example, self-only buffs such as Berserk will automatically target `<me>`.
- Full target support for magic and applicable actions, including targets such as `<stpc>`, `<st>`, `<pet>`, and more.
- Built-in **skillchain system**.
- Range checks when engaging enemies or supporting allies.
- Support for pet-job abilities and pet commands.
- Fully resizable and repositionable hotbar.
- Dynamic resource and action-state feedback.

### 0.4 Skillchain Support

fCrossbar includes a built-in Final Fantasy XI skillchain system supporting **all 16 skillchain properties**.

This is one of the parts of the project I've put the most thought into, and I think the community will enjoy how much useful information it can provide without automating gameplay.

Weapon Skills can dynamically change their visual state depending on what is happening in combat, allowing you to quickly see which options are relevant to the current skillchain.

This is **not automation**. You still need to understand the timing and make the decision yourself.

I may add optional timing bars later if there is enough interest from users.

### 0.5 Custom Macros

fCrossbar supports custom macros with up to **12 lines**.

This allows for things such as:

- Gear swapping
- Buff sequencing
- Spell sequencing
- Magic burst rotations
- Multi-step commands

The 12-line limit is a conscious design decision.

I want fCrossbar to provide powerful tools for players without turning into an automation framework. I do not intend to build or distribute systems that play the game for you.

### 0.6 Additional Details

- **Mounts behave as logical toggles with cooldown support.** Add a mount to your bar, press it to mount, and press the same button again to dismount. Cooldown information is displayed directly on the action, making mount behavior feel more in line with modern MMOs.
- Abilities, magic, items, trusts, and other player resources are discovered when fCrossbar loads and during relevant configuration states rather than being continuously scanned.
- I am exploring combat-log or event-based detection so newly learned spells, abilities, or Weapon Skills can appear dynamically while leveling without requiring a full reload.
- A **color-vision-accessible UI mode** is planned as the interface reaches a more finalized visual state.
- Optional sound cues for specific events and action states are being considered, with the sound design created by yours truly.
- Additional accessibility, layout, and quality-of-life features will continue to be added as the project matures.

<br>
<br>

## About fieldcraft

I've spent years playing MMOs like Final Fantasy XIV and World of Warcraft, and I've often found myself wanting certain modern interface conveniences when returning to older games.

Coming back to Vana'diel made me want to apply my product-design experience to one of the first MMOs I ever played and build something useful for the community, especially for players returning after many years away.

I'm a **Lead / Senior Product Designer** in software with more than **20 years of experience in visual design and HCI**, and I've also been producing electronic music for more than **10 years**.

A lot of the decisions behind fCrossbar come directly from that background: keeping things visually clear, reducing unnecessary interaction, giving players useful information at the right time, and making the interface feel modern without losing what makes Final Fantasy XI feel like Final Fantasy XI.

And if you're into electronic music, you can also find my work under **fieldcraft** on streaming platforms.
