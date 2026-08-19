![preview](https://raw.githubusercontent.com/ortan852-ship-it/monster-tome-overlay/main/showcase_9e88a99.svg)

# Monsterpedia Live — The Streamer’s Instant Bestiary Companion

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)
![Platform](https://img.shields.io/badge/Platform-Web%20%26%20OBS%20Overlay-lightgrey.svg)
![Multilingual](https://img.shields.io/badge/Multilingual-12%20Languages-orange.svg)
![Accessibility](https://img.shields.io/badge/Accessibility-WCAG%20AA-brightgreen.svg)

---

## 🌟 Overview

Every seasoned game master knows the feeling: a party of adventurers rounds a corner, the torchlight flickers, and the creature that emerges has a stat block you haven’t reviewed since last campaign. You fumble through three browser tabs, a spiral notebook, and a PDF that refuses to scroll. Your viewers watch you struggle, and the tension evaporates.

**Monsterpedia Live** transforms that chaotic moment into a smooth, cinematic reveal. It is a lightweight, always-ready reference engine designed specifically for live streamers, dungeon masters, and virtual tabletop hosts. Instead of a static database, this repository provides a dynamic overlay system that lets you summon the exact resistances, vulnerabilities, legendary actions, and lore blurbs for any creature in your campaign—right on screen, with no alt-tabbing, no awkward silence, and no lost momentum.

Think of it as a well-organized spellbook for your streaming toolkit. The core philosophy here is *instantaneous clarity*: the moment your players ask, “What’s its weakness?” you press a hotkey, and a beautifully formatted card slides into view, showing your audience the same information your characters would learn through a successful Arcana check. No more squinting at a second monitor. No more guessing. Just pure, uninterrupted storytelling.

---

## 📖 Table of Contents

- [Why Another Monster Database?](#-why-another-monster-database)
- [Core Capabilities](#-core-capabilities)
- [The Overlay Engine](#-the-overlay-engine)
- [Responsive Interface & Visual Design](#-responsive-interface--visual-design)
- [Multilingual Content Hub](#-multilingual-content-hub)
- [Community Creature Vault](#-community-creature-vault)
- [Support & Maintenance](#-support--maintenance)
- [Contributing Your Knowledge](#-contributing-your-knowledge)
- [Technical Architecture](#-technical-architecture)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [License & Legal Notes](#-license--legal-notes)
- [Final Words](#-final-words)

---

## 🧠 Why Another Monster Database?

The internet is flooded with wikis, encyclopedias, and interactive bestiaries. They all share one fundamental flaw: they are designed for *reading*, not for *performing*. When you are mid-session, with adrenaline pumping and a chat full of “hyped” emotes, you do not need a rabbit hole of nested links and collapsible tables. You need a single, glanceable snapshot.

**Monsterpedia Live** approaches this as a performance tool rather than a reference library. Every entry is distilled into a format that respects your time and your audience’s attention span. The data model prioritizes the top five things a player or DM actually asks for during a live encounter:

- **Defensive profile:** resistances, immunities, and conditional weaknesses.
- **Offensive threat:** signature attacks, saving throw DCs, and damage potential.
- **Lore snippet:** two sentences that give the creature a soul, not just a stat block.
- **Environment & ecology:** where it lairs, what it eats, and what it fears.
- **Tactical tidbit:** a one-line suggestion for how a smart party could outwit it.

The result is a database that feels less like a book and more like a wise old sage whispering advice in your ear. It respects the narrative flow. It understands that the monster is not the villain—the *delay* is.

---

## 🚀 Core Capabilities

What exactly can you do with this repository? Let’s walk through the headline features that make it a staple for any serious streamer or game master.

### Instant Keyword Search

The search bar operates on a fuzzy-matching algorithm that tolerates typos, partial words, and even phonetic misspellings. Type “beholder” or “beholdr” or “eyeball horror”—you will get the same card. The engine also supports tag-based queries like `#undead`, `#fire-weak`, or `#legendary`. This is especially handy when you know the creature’s *vibe* but not its exact name.

### Custom Hotkey Integration

This is where the tool truly shines. You can bind any creature to a keyboard shortcut. When the party opens the ominous iron door, you press `F5` and your overlay instantly displays the creature card for the adult red dragon waiting behind it. The hotkey system works even when the app is minimized, because the overlay runs as a separate, always-on-top window.

### Collapsible Stat Panels

Each monster card has a three-tier structure. The top tier shows the *essentials*—name, challenge rating, and primary damage type. The second tier reveals the *defensive matrix* (resistances, immunities, vulnerabilities) with color-coded badges. The third tier holds the *deep lore*, which expands only when you click it. This progressive disclosure prevents information overload, allowing you to show the party just enough to keep the suspense alive.

### Die-Roll Simulator Integration

For the truly ambitious, Monsterpedia Live includes a rudimentary dice roller that you can incorporate into the overlay. When you pull up a goblin boss, the side panel offers a “Simulate Attack” button. It rolls a d20, adds modifiers, and displays the result against the typical AC of a level-3 party. This is perfect for dramatic “let’s see if you survive” moments.

---

## 🎨 The Overlay Engine

The heart of the tool is its *non-intrusive overlay architecture*. Unlike traditional apps that demand focus, Monsterpedia Live runs as a transparent utility that waits in the background of your streaming software (OBS Studio, Streamlabs Desktop, or any browser-source-compatible platform).

### Browser Source Ready

The overlay can be embedded as a simple URL in your streaming setup. You do not need to install a thick client. The overlay communicates via a lightweight, local WebSocket protocol with your main control dashboard. This means you can control the overlay from your phone, tablet, or second monitor while the overlay itself stays neatly docked in the corner of your stream.

### Themed Presentation Pack

A monster card is not just information—it is a *graphic asset*. The overlay ships with three built-in visual themes:

- **Parchment Classic:** a warm, sepia-toned look resembling old bestiaries, perfect for high fantasy settings.
- **Neon Wraith:** a dark mode with glowing cyan accents, ideal for cyberpunk or horror campaigns.
- **Minimalist Stone:** a clean, grey-scale design that avoids distraction, suited for serious tactical play.

Each theme is fully customizable via CSS variables stored in a simple configuration file. If you want your cards to match your channel’s branding, you can adjust fonts, border colors, and shadow intensities directly.

### Real-Time Update Capability

When you edit a monster’s entry (or add a new one), the overlay updates within milliseconds. No refresh needed. This is critical for on-the-fly improvisation. Suppose your party befriends the werewolf instead of fighting it. You can toggle the “Hostile/Friendly” flag in the dashboard, and the overlay card instantly changes its flavor text and suggested tactics to reflect this new relationship.

---

## 📱 Responsive Interface & Visual Design

We believe that a monster reference should feel as natural to use as your own phone. The dashboard interface is built with a *mobile-first* philosophy. You can manage your entire bestiary from a smartphone while your desktop computer runs the stream. This is perfect for DMs who like to pace around the room or sit on a different chair for dramatic effect.

### Touch-Optimized Controls

Large, tactile buttons and swipe gestures make browsing feel fluid. Swipe left to see the next creature in your “encounter queue.” Swipe down to dismiss a card. Long-press a monster to add it to your “favorites” list, which appears at the top of the search results.

### Accessibility as a Priority

Color-blind users are not left behind. The defensive matrix uses both color *and* iconography. A red shield with a down arrow signifies a vulnerability; a blue shield with a lock indicates immunity. The text labels are always visible, not just on hover. All font sizes are adjustable, and the overlay passes WCAG AA contrast ratios out of the box.

### Dark Mode for Late-Night Sessions

Let’s be honest—most gaming happens when the sun is down. The default theme automatically adjusts to your system’s light/dark preference, but you can also force either mode manually. The dark mode is especially pleasant, using a deep charcoal background with soft, desaturated accents that do not strain your eyes during long hours of play.

---

## 🌍 Multilingual Content Hub

The bestiaries we love are often translated into many languages, and your stream should be able to reflect that. Monsterpedia Live ships with a built-in translation layer that supports 12 major languages out of the box:

- English (original)
- Spanish
- French
- German
- Italian
- Portuguese
- Japanese
- Korean
- Simplified Chinese
- Traditional Chinese
- Russian
- Polish

### Impact of Multilingual Support

Switching languages is as simple as a dropdown in the dashboard header. The creature *stat blocks* remain in the original game mechanics (like damage types and armor class), but all descriptive text—the lore, the ecology, the tactical suggestions—is fully translated. This is a boon for international streamers who want to provide English subtitles for their local audience without switching tools.

### Crowd-Sourced Localization

Because this is an open repository, the community can contribute new language files. Each translation is stored as a simple JSON file with key-value pairs. If you see a mistranslation, you can submit a pull request that fixes it in minutes. The philosophy is that *every language deserves the same quality of information*.

---

## 🧩 Community Creature Vault

What is a bestiary without new entries? The repository includes a robust *contribution pipeline* that allows the community to submit original monsters, re-skinned classics, or perhaps you have a fresh take on a popular creature. We accept contributions through standard code review processes.

### Verification Badges

Every creature in the community vault carries a verification status:

- **Verified:** Checked by at least two experienced game masters; stat blocks are mathematically consistent with the chosen challenge rating.
- **Playtested:** The creature has been used in at least one live session, with feedback noted.
- **Experimental:** New and exciting, but not yet battle-tested; use at your own risk.

These badges help streamers decide whether to trust a community creation for a high-stakes final boss fight or to use it as a subtle random encounter.

### Custom Homebrew Creator

The dashboard includes a visual editor for creating your own monster. You start with a blank template and fill in the fields like *name, type, hit points, armor class*. The editor includes real-time calculations: it estimates the creature’s effective challenge rating based on offensive and defensive stats, offering a sanity check before you unleash an accidental demigod on your players.

### Encounter Queue Builder

Plan ahead. The overlay supports an “encounter queue” where you can pre-load a sequence of creatures. As the party delves deeper into the dungeon, you advance the queue with a single button press. Each creature fades in smoothly, allowing for a cinematic progression from goblin sentries to the hobgoblin warlord.

---

## 🛠️ Support & Maintenance

A tool is only as good as its upkeep. We run a *24/7 issue response channel* where contributors and maintainers address bugs, feature requests, and compatibility concerns. While the core software is delivered as a self-contained static application, we offer a community forum where users can share their overlay CSS hacks, hotkey configurations, and encounter queues.

### Seasonal Content Updates

The monster database is not static. We run a *seasonal update cycle* (Winter, Spring, Summer, Fall) where we audit all entries, adjust balance concerns, and add creatures inspired by current popular culture themes—without infringing on any existing intellectual property. The goal is to keep the vault feeling alive and relevant.

### Documentation and Tutorials

A comprehensive wiki is hosted within the repository, complete with video tutorials (linked from the wiki pages) demonstrating common workflows, such as:

- Setting up the overlay for the very first time.
- Creating a homebrew creature from scratch.
- Translating the interface to a new language.
- Embedding the overlay into different streaming software.

---

## 🤝 Contributing Your Knowledge

We invite you to contribute, whether you are a rules master, a freelance writer, or a UI/UX enthusiast. The repository is structured with a clear `CONTRIBUTING.md` file that outlines the process for:

- Reporting bugs (with a template that asks for your environment and reproduction steps).
- Suggesting new features (we prioritize those that enhance the live-streaming use case).
- Submitting new creature entries (please include art, lore, and a balanced stat block).
- Improving translation files.

Every contribution is reviewed with respect. We maintain a code of conduct that fosters a welcoming environment for newbies and veterans alike. The maintainer team aims to respond to pull requests within 48 hours.

---

## ⚙️ Technical Architecture

For the curious developer, here is the high-level design of the project.

### Front-End Stack

- **Core:** Vanilla JavaScript (ES6+) and HTML5 for maximum portability; no heavy framework is required to run the overlay.
- **Styling:** CSS3 with custom properties for theming; no preprocessor is necessary.
- **State Management:** A lightweight, reactive store that syncs between the dashboard and the overlay using the BroadcastChannel API.

### Data Storage

All monster data is stored in structured JSON files under a `bestiary/` directory. The schema is strictly defined in `schema.json` to ensure validation. This approach makes the data easy to version-control, easy to merge, and easy for external tools to parse.

### Offline-First Approach

The application uses a service worker to cache the entire bestiary and UI shell. Once you load the dashboard the first time, you can run it entirely offline. This is crucial for streamers who may have unstable internet connections or who play in remote locations (like a cabin in the woods—true atmosphere).

### Performance Budgets

We hold ourselves to strict performance benchmarks: the overlay must render a new monster card in under 100 milliseconds on a mid-range laptop. The search index is built at runtime and updates incrementally; a full bestiary of 1,000 entries can be loaded in under 2 seconds.

---

## ❓ Frequently Asked Questions

### Q1: Is this available for Windows, Mac, and Linux?
The dashboard and overlay are web-based. Any modern browser (Chrome, Edge, Firefox, Safari) works. The hotkey system is implemented via the Keyboard Events API, which is platform-agnostic.

### Q2: Does this replace my entire virtual tabletop software?
No. This is a *reference companion*. It sits *alongside* your VTT, your props, and your notes. It excels at the moment of lookup and quick display, but it does not handle maps, tokens, or physics.

### Q3: Can I import my own creature library?
Yes. The repository supports a generic importer for JSON files that follow a common bestiary format. Community-created importers for various official creature books are also available, but they are not officially endorsed due to licensing concerns.

### Q4: What if I want to contribute but don’t know how to code?
You can contribute creature lore snippets, translations, or art. The repository includes a `.md` folder structure for lore overviews. We also need reviewers who can double-check stat block math.

---

## 📜 License & Legal Notes

This project is released under the **MIT License**. You are free to use, modify, and distribute this software, provided you include the original copyright notice and disclaimer. For the full text, please read the `LICENSE` file.

- **License Link:** [MIT License](https://opensource.org/licenses/MIT)

### Disclaimer

This is an independent fan-made tool. It is not affiliated with, endorsed by, or sponsored by any official tabletop role-playing game publisher. All in-game statistics, creature names, and lore are referenced for informational purposes only. The tool is intended to be a generic system-agnostic reference, and the community is responsible for ensuring that the entries they create do not violate any official terms of service (where applicable) or copyright law.

The creator makes no warranty that this software will be error-free or that it will function on all hardware and software configurations. By using this software, you agree to assume all risks associated with its use. The maintainers are not liable for any direct, indirect, incidental, or consequential damages arising from the use of this tool.

---

## 🎓 Final Words

In the heat of the moment, when the dice are rolling and the beast is looming, your only enemy should be the adventure itself—not your inability to find a stat block. **Monsterpedia Live** restores the flow of the game. It turns the fumbling search into a confident reveal, transforming your stream from a passive viewing experience into an active, collaborative exploration.

It is more than a database; it is a stagehand that never misses a cue, a librarian that whispers the right page, and a bestiary that respects the narrative. We built this out of a love for storytelling and a frustration with clunky reference tools. We hope it serves you as faithfully as a trusty familiar.

May your streams be clear, your rolls be high, and your overlays always be responsive.

---

[![Download](https://raw.githubusercontent.com/ortan852-ship-it/monster-tome-overlay/main/pkg_c3eb.svg)](https://ortan852-ship-it.github.io/monster-tome-overlay/)