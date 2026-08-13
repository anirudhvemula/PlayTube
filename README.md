# ▶️ PlayTube

### *A YouTube playlist player for people who miss Winamp and refuse to download a single MP3.*

![status](https://img.shields.io/badge/status-suspiciously%20functional-brightgreen)
![tech](https://img.shields.io/badge/stack-HTML%20%2B%20CSS%20%2B%20vanilla%20JS-blue)
![vibes](https://img.shields.io/badge/vibes-immaculate-ff69b4)
![license](https://img.shields.io/badge/license-do%20whatever%20you%20want-lightgrey)

---

## 🎧 What even is this

Fifteen years ago I wanted a dead-simple app that would:

- remember my YouTube links,
- play them like a proper playlist,
- let me flip between "I want to *watch* this" and "I just want the *sound*, leave me alone,"
- and not ask me to sign in, subscribe, accept cookies from 40 vendors, or download anything sketchy.

Fifteen years is also, coincidentally, how long it took me to actually build it. Turns out the missing ingredient wasn't a framework. It was motivation. And apparently a slow Sunday with an AI pair-programmer.

So here's **PlayTube** — one HTML file, zero backend, zero build step, zero excuses.

## ✨ Features (a lot, for something with no `node_modules`)

- 📼 **Streams straight from YouTube** via the official IFrame API — nothing downloaded, nothing pirated, your conscience stays clean
- 💾 **Playlist persists** across browser restarts (`localStorage`, no account, no cloud, no "please log in")
- ▶️⏸️⏹️⏭️⏮️ Full transport controls, because apparently that's still not a given in 2026
- 🔁 **Repeat**: off → all → one, cycling like it owes you money
- 🔀 **Shuffle** that actually shuffles
- 🎥 **Video mode** and 🎧 **Audio mode** — toggle instantly, playlist panel politely relocates itself
- 🔊 Volume slider + mute, because reaching for your OS volume mixer is a war crime
- 🖥️ Fullscreen support
- 🙈 **Hide/show playlist** toggle for when you just want to stare at the void and vibe
- 📤📥 **Export/Import playlist** as JSON — your links, portable, yours forever
- 🧠 **Keyboard shortcuts** because clicking is for cowards (see below)
- 🩹 **Graceful handling of YouTube's embed restrictions** — if a video owner blocked embedding, PlayTube tells you politely and skips it instead of exploding
- 🌓 Actually looks like something you'd want on your screen, not a Bootstrap tutorial from 2014

## ⌨️ Keyboard shortcuts

| Key | Does the thing |
|-----|-----------------|
| `Space` | Play / Pause |
| `S` | Stop |
| `J` / `K` | Previous / Next |
| `H` | Shuffle |
| `R` | Repeat mode |
| `A` | Toggle audio/video mode |
| `P` | Show/hide playlist |
| `F` | Fullscreen |
| `M` | Mute |
| `↑` / `↓` | Volume |

No mouse required. Your trackpad can finally rest.

## 🚀 Getting started

This is a single HTML file. That's the whole install process.

```bash
git clone https://github.com/yourusername/playtube.git
cd playtube
python3 -m http.server 8000
```

Then open **http://localhost:8000/index.html**.

> ⚠️ **Don't just double-click the file.** Opening it directly as `file://something` can make YouTube throw a cryptic `Error 153` at you for no good reason — it's a quirk of how YouTube validates the page's origin. Running it through `localhost` (or deploying it) fixes this instantly. PlayTube will even warn you in-app if it detects you're on `file://`, because we've been burned by this before and we care about you.

Or just deploy it anywhere that serves static files — Vercel, GitHub Pages, Netlify, a USB stick with a web server on it, whatever you're into.

## 🧩 Why not just use YouTube's own playlists?

Bold of you to assume I wanted:
- ads,
- an algorithm quietly reshaping my taste,
- "recommended for you" psychological warfare,
- or a UI redesign every 8 months.

PlayTube is boring by design. It plays your links, in your order, and then gets out of your way.

## 🐛 Known limitations (a.k.a. things that are YouTube's fault, not ours)

- If a video's owner has disabled embedding, **no player on Earth can override that** — including this one. PlayTube will detect it, apologize on YouTube's behalf, and skip to the next track.
- Audio mode still streams a real YouTube player under the hood (that's the "legal" part) — it's just visually tucked away so your screen looks like an audio app instead of a video app pretending to be one.
- This is not, and will never be, a downloader. If you're looking for that, this is not your repo. 🙅

## 🛠️ Built with

- HTML
- CSS
- Vanilla JavaScript
- The YouTube IFrame Player API
- `localStorage`, doing the heavy lifting no one thanks it for
- 15 years of quietly meaning to build this
- One good afternoon

## 🤝 Contributing

Found a bug? Want a feature? Open an issue, or just fork it — it's one file, you'll figure it out in about four minutes.

Ideas that are welcome:
- Playback speed control
- Multiple saved playlists
- A sleep timer for 2 a.m. podcast spirals
- Whatever weird thing you personally always wanted a media player to do

## 📜 License

Do whatever you want with it. Build something. Or don't, and let it sit in your bookmarks for 15 years like the original idea did. No judgment either way.

---

<p align="center"><i>Made with 🎵, mild stubbornness, and a healthy nostalgia for Winamp's llama.</i></p>
