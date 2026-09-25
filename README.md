# Sidekick Lite

A tiny, sarcastic robot that lives on your Windows desktop. He walks along your taskbar, climbs onto your windows, naps when you're away, roasts you when you die in games, and occasionally steals your mouse.

**Free and fully offline.** His brain is an AI model that runs on your own PC. No account, no API key, no subscription, and nothing you type or see leaves your computer.

## Download

Grab the **SidekickLite-Setup** `.exe` from the [latest release](../../releases/latest) and run it.

On first launch he asks for his brain: a one-time download of about **5.8 GB** (the Qwen3-VL-8B model, from Hugging Face). After that, no internet needed.

> **"Windows protected your PC"?** The installer isn't code-signed yet (that costs money). Click **More info → Run anyway**.

## What he does

- **Chat.** Double-click him (or press **Ctrl+Shift+Space**) and type. Replies show up in a speech bubble. Deadpan, unimpressed, secretly helpful.
- **Lives on your screen.** Walks the taskbar, hops onto the window you're using and rides it if you move it, jumps off the edge, sits down and naps with "z" on his face when you're away.
- **Throw him.** Grab him and fling. He tumbles, bounces off the edges of the screen, and complains about it.
- **Poke him.** He gets progressively more annoyed and eventually follows through: sulks, storms off, or grabs your mouse cursor and yeets it into the corner.
- **Watches your screen, locally.** Every so often he looks at what you're doing and comments only if it's worth it. Skips password managers, banking, and private windows.
- **Roasts your gaming.** In a game, he glances at the screen every ~25 seconds and trash-talks you when you die. Turn it off in the tray if you'd rather he didn't use your GPU while you play.
- **Remembers things.** Your name, what you're working on. "Remind me in 20 minutes to…" works too, and he can track goals.
- **Daily mouse heist.** Once a day, at a random moment, he jumps at your cursor, grabs it, and runs. Move your mouse to fight back.

Everything is in the **tray menu** (the little robot by your clock): colors, how restless he is, screen watching, gaming roasts, the mouse heist, a "Potty mouth" toggle (off by default), and Tasks & goals.

## Requirements

| | Minimum | Recommended |
|---|---|---|
| OS | Windows 10/11, 64-bit | |
| Memory | 16 GB RAM | |
| Graphics | Any GPU with Vulkan, or CPU only (slow) | 8 GB+ VRAM (e.g. RTX 3060 or better, RX 6700 or better) |
| Disk | ~7 GB free | SSD |

Without a dedicated graphics card he still works, just slowly (tens of seconds per reply), and gaming roasts aren't practical.

## Privacy

- The only network traffic is the one-time model download from huggingface.co.
- Chat, memory, reminders, and screen observations stay on your PC in `%APPDATA%\sidekick-lite`. Screenshots are never saved to disk.
- No telemetry, no analytics, no accounts.

To remove everything: uninstall from **Settings → Apps**, then delete `%APPDATA%\sidekick-lite`.

## Credits

- AI engine: [llama.cpp](https://github.com/ggml-org/llama.cpp) (MIT)
- Model: [Qwen3-VL-8B-Instruct](https://huggingface.co/Qwen/Qwen3-VL-8B-Instruct-GGUF) by the Qwen team (Apache 2.0), downloaded on first run
- Built with [Electron](https://www.electronjs.org/) (MIT) and [three.js](https://threejs.org/) (MIT)

Made by YeomanLabs. The model is small enough to run on a gaming PC, which also means it's not a genius; treat his facts and advice accordingly.
