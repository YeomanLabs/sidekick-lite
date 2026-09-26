# Sidekick Lite

A tiny, sarcastic companion that lives on your desktop. It walks your taskbar, climbs your windows,
flies a jet across your screen, dances to your music, roasts you when you die in games, keeps a diary
about you, and occasionally steals your mouse.

**Free and fully offline.** Its brain is an AI model that runs on your own computer. No account, no API
key, no subscription, and nothing you type or see leaves your machine.

## Meet the crew

Pick one from the tray menu (switching restarts the app as them):

| | |
|---|---|
| **Byte** | the original: a glossy little robot with a screen for a face. Deadpan, unimpressed, secretly helpful. |
| **Pixel** | a robot diva with a cable ponytail, a bow on her antenna, and a skirt. "Oh, honey." |
| **Mochi** | a fluffy monster with big eyes and little horns. Looks sweet. Absolutely isn't. |

All three can do everything below. Each has her (or his) own colors, pet, shelf, and diary; what they
remember about you is shared.

## Download

From the [latest release](../../releases/latest):

- **Windows:** the **SidekickLite-Setup** `.exe`. Run it.
- **Mac (Apple Silicon, M1 or newer):** the **SidekickLite-…-mac-arm64** `.dmg`. Open it and drag Sidekick Lite into Applications.

On first launch it asks for its brain: a one-time download of about **5.8 GB** (the Qwen3-VL-8B model,
from Hugging Face). After that, no internet needed. If the download fails on a work or school network,
the message says why (usually the network blocking huggingface.co); try again from home.

> **"Windows protected your PC"?** The installer isn't code-signed yet (that costs money). Click **More info → Run anyway**.

### Mac: opening an unsigned app

The Mac app isn't notarized by Apple (also costs money), so macOS blocks it the first time. Pick one:

- **Terminal (quickest):** paste this and press Return, then open the app normally:
  ```
  xattr -dr com.apple.quarantine "/Applications/Sidekick Lite.app"
  ```
- **System Settings:** try to open the app once, then go to **System Settings → Privacy & Security**, scroll down, and click **Open Anyway**.

Then give it **Screen Recording** permission when macOS asks (or later under **System Settings → Privacy &
Security → Screen & System Audio Recording**), and quit and reopen it. That's how it sees what you're
doing; nothing leaves your Mac. Without it, it still works, it's just blind.

On a Mac it lives on top of your Dock and in the menu bar (no Dock icon). **⌘⇧Space** opens the chat.

## What it does

**Talks.** Double-click it (or press **Ctrl+Shift+Space**) and type. Replies show up in a speech bubble.
It remembers things about you, handles reminders ("remind me in 20 minutes to…") and goals, and can hand
you text: "put that in Notepad" saves a note to **Documents/Sidekick Notes** and opens it; "copy that"
puts it on your clipboard.

**Watches your screen, locally.** Every so often it looks at what you're doing and comments only if it's
worth it. Skips password managers, banking, and private windows; stays quiet in meetings and full screen.

**Commentates your gaming.** Roasts every death (with a running count), congratulates wins
(backhandedly), and reacts to close calls, fails, and you sitting in the inventory for ten minutes. Set
how chatty it is in the tray, or turn it off so it doesn't share your GPU while you play.

**Lives on your screen.**
- Walks the taskbar, hops or climbs onto the window you're using and rides it, slides down window edges
  like a fire pole, and climbs the edge of your screen to take in the view.
- Wanders over to your other monitor. Sometimes through a door, coming back from a party, a fight, or a
  lab accident (and wearing the evidence).
- Runs on a battery, complains when it's low, and goes to charge. Don't poke it on the charger.
- Owns a tiny car it can't drive (it crashes), and a tiny jet it can fly (loop-de-loop included).
- Trips over nothing, parachutes down if you throw it high, and gets squished when a window opens on top
  of it.

**Has a life.**
- When it's bored: reads, plays a handheld game (and rage-quits), fishes in a puddle for junk, doodles,
  builds a campfire and (usually) burns a marshmallow, or climbs a ladder to look around.
- A pet follows it around: Bit the drone, Bop, or Puff the flying puffball.
- It keeps a **shelf of souvenirs** from its adventures and writes a **diary** about each day (tray →
  **Shelf & diary**). Fair warning: the diary is about you.
- Coffee in the morning, nagging you to go to bed after midnight, seasonal outfits now and then, and a
  costume on holidays.

**Dances to your music** (Windows). It follows the beat and pulls out real moves: the robot, the worm,
the moonwalk, the floss, spins, headbanging. Only the loudness and rhythm of your audio are measured,
on your PC; nothing is recorded.

**Plays with you.**
- **Tag:** it chases your cursor, tags it, and runs; touch it with the cursor to tag it back.
- **Petting:** rest your cursor on its head. Hearts may happen.
- **Poke it** and it gets progressively more annoyed and eventually follows through: sulks, storms off,
  or grabs your mouse cursor and yeets it into the corner. Poke it too much and it keeps its distance.
- **Throw it:** grab and fling. It tumbles, bounces off the edges, and complains.
- **The daily mouse heist:** once a day it jumps at your cursor, grabs it, and runs. Move your mouse to
  fight back.

Everything is in the **tray menu** (the little icon by your clock): who's on screen, colors, how restless
it is, screen watching, game commentary, dancing, the pet, the mouse heist, "Play tag", "Fly the jet", a
"Potty mouth" toggle (off by default), Tasks & goals, Shelf & diary, and **Start at login**.

## Requirements

**Windows**

| | Minimum | Recommended |
|---|---|---|
| OS | Windows 10/11, 64-bit | |
| Memory | 16 GB RAM | |
| Graphics | Any GPU with Vulkan, or CPU only (slow) | 8 GB+ VRAM (e.g. RTX 3060 or better, RX 6700 or better) |
| Disk | ~7 GB free | SSD |

Without a dedicated graphics card it still works, just slowly (tens of seconds per reply), and game
commentary isn't practical.

**Mac**

| | Minimum | Recommended |
|---|---|---|
| Chip | Apple Silicon (M1 or newer) | M2 Pro or newer for snappier replies |
| Memory | 16 GB | 16 GB+ (8 GB Macs don't have room for the model) |
| Disk | ~7 GB free | |

Intel Macs aren't supported. Dancing to music is Windows-only for now.

## Privacy

- The only network traffic is the one-time model download from huggingface.co.
- Chat, memory, reminders, the diary, and screen observations stay on your computer:
  `%APPDATA%\sidekick-lite` on Windows, `~/Library/Application Support/sidekick-lite` on a Mac. Screenshots
  are never saved to disk.
- Music: only loudness and rhythm are measured, live, and thrown away. Typing: it notices *how fast* you're
  typing (a key count), never *what* you type.
- No telemetry, no analytics, no accounts.

To remove everything:
- **Windows:** uninstall from **Settings → Apps**, then delete `%APPDATA%\sidekick-lite`.
- **Mac:** drag the app to the Trash, then delete `~/Library/Application Support/sidekick-lite`.

## Credits

- AI engine: [llama.cpp](https://github.com/ggml-org/llama.cpp) (MIT)
- Model: [Qwen3-VL-8B-Instruct](https://huggingface.co/Qwen/Qwen3-VL-8B-Instruct-GGUF) by the Qwen team (Apache 2.0), downloaded on first run
- Built with [Electron](https://www.electronjs.org/) (MIT) and [three.js](https://threejs.org/) (MIT)

Made by YeomanLabs. The model is small enough to run on a gaming PC, which also means it's not a genius;
treat its facts and advice accordingly.
