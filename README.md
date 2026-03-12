# Omarflix 🎬

> Your private cinema — watch local videos in your browser. No accounts, no uploads, completely private.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Single File](https://img.shields.io/badge/Single-File-blue)
![No Backend](https://img.shields.io/badge/No-Backend-green)
![100% Private](https://img.shields.io/badge/100%25-Private-red)

A lightweight, single-file browser-based media player for your local video library. Point it to a folder, start streaming — that's it. All watch history and progress saved locally on your device. No accounts, no uploads, no cloud, no tracking.

## Features

- 🎬 **Netflix-inspired UI** — Beautiful dark theme with smooth animations
- 🎯 **Smart organization** — Auto-detects TV shows vs movies, parses seasons/episodes
- 📺 **TV show support** — Episode browser, skip intro, next episode auto-play
- ⏯️ **Intelligent playback** — Resume from last position, remember where you left off
- 📁 **Flexible storage** — Add from OneDrive, network drives, local folders
- 💾 **Automatic saves** — Progress saved real-time every 5 seconds
- 🔄 **Fast restore** — Library persists automatically, no re-uploading
- 📱 **Responsive design** — Works perfectly on desktop, tablet, and mobile
- 🔒 **100% private** — All data stays on your device, no tracking
- 📦 **Zero dependencies** — Single HTML file, no installation needed
- 🌐 **Offline ready** — Service worker for caching, works without internet
- ⌨️ **Keyboard shortcuts** — Full playback control from keyboard

## Table of Contents

- [Quick Start](#-quick-start)
- [Supported Formats](#-supported-formats)
- [Features](#features)
- [Setup Guides](#-setup-guides)
  - [Desktop](#desktop)
  - [Mobile](#mobile)
- [Usage](#-usage)
- [Player Controls](#-player-controls)
- [Troubleshooting](#-troubleshooting)
- [Tech Details](#-tech-details)
- [Privacy](#-privacy)
- [Contributing](#-contributing)
- [License](#license)

---

## 🚀 Quick Start

**[Download `omarflix.html`](./omarflix.html)** →  Open in browser →  Add media folder →  Start watching!

### 30 Seconds to Video

1. Save `omarflix.html` to your computer
2. Double-click to open in your browser
3. Click **"Add Media Folder"**
4. Select a folder with video files
5. Click any title to start streaming

That's it. Watch history saves automatically.

## 📦 Supported Formats

| Format | Codec Support | Notes |
|--------|---------------|-------|
| **MP4** | H.264 + AAC | Best compatibility ✅ |
| **MKV** | H.264/H.265 + AAC/FLAC/Opus | Full support ✅ |
| **WebM** | VP8/VP9 + Vorbis/Opus | Good support ✅ |
| **AVI** | MPEG-4/MPEG-2 | Works on most browsers ✅ |
| **MOV** | H.264 + AAC | QuickTime format ✅ |
| **M4V** | H.264 + AAC | iTunes format ✅ |

*Browser support depends on built-in codecs. For unsupported formats, convert using FFmpeg or Handbrake.*

## 🖥️ Setup Guides

### Desktop

#### Organization (Optional)

Recommended folder structure:
```
Media/
├── Movies/
│   ├── Dune Part Two (2024).mp4
│   └── Interstellar (2014).mkv
└── TV Shows/
    ├── Breaking Bad/
    │   └── S01/
    │       ├── Breaking Bad S01E01.mkv
    │       └── Breaking Bad S01E02.mkv
    └── The Office/
        ├── The Office S01E01.mkv
        └── The Office S01E02.mkv
```

#### Episode Naming

Flexible naming — all these work:
- `Show Name S01E05.mkv`
- `Show Name - S01E05 - Title.mkv`
- `Show Name_s01e05.mkv`
- `Show Name 1x05.mkv`

#### Got it, what's next?

1. Open `omarflix.html` in your browser
2. Click **"Add Folder"** (or **"Add Media Folder"** on landing)
3. Select your video folder
4. Grant permission when browser asks
5. Library loads automatically

**That's it.** Your watch history saves to your browser — no configuration needed.

### Mobile

#### Install as App (Recommended)

**iPhone/iPad:**
1. Open `omarflix.html` in Safari
2. Tap **Share** (↗️)  
3. Select **"Add to Home Screen"**
4. Call it "Omarflix" and tap **Add**
5. Tap the new icon to launch

**Android:**
1. Open `omarflix.html` in Chrome
2. Tap **Menu** (⋮)
3. Tap **"Install app"** (or "Add to Home screen")
4. Confirm
5. Tap the new icon to launch

#### Features on Mobile

- **Hamburger menu** (☰) → Navigation & settings
- **Swipe left** → Forward 10 seconds
- **Swipe right** → Rewind 10 seconds
- **Double tap** → Play/Pause
- **Responsive columns** → Auto-adapts to screen size

## 📺 Usage

### Adding Videos

**From local folder:**
- Click **"Add Folder"** (desktop) or **"Add Media Folder"** (mobile)
- Select folder with videos
- Library loads instantly

**From network/cloud:**
- OneDrive, Google Drive, Dropbox files appear as if local
- First load may be slower (depends on network)

**Persistent library:**
- Your media list saves automatically
- Close and reopen the app — library is still there
- No need to re-add folders each time

### Watching

**Movies:**
- Click the poster
- Start watching
- Progress saved automatically
- Resume next time (click "Resume")

**TV Shows:**
- Click the show poster
- Click an episode to start
- Auto-plays next episode when finished
- Use episode browser to jump around

### Search & Filter

- **Search**: Find by title, show name, or filename
- **Filter**: Movies, TV Shows, or In Progress
- **Sort**: Title, recently watched, progress percentage
- Works instantly without reloading

## ⌨️ Player Controls

### Keyboard Shortcuts (Desktop)

| Key | Action |
|-----|--------|
| `Space` / `K` | Play/Pause |
| `←`/`→` | Rewind/Forward 5 sec |
| `S` | Skip Intro (85 sec) |
| `F` | Fullscreen |
| `M` | Mute/Unmute |
| `+`/`-` | Volume up/down |
| `Esc` | Exit fullscreen/player |

### Mobile Gestures

| Action | Gesture |
|--------|---------|
| Play/Pause | Double tap |
| Forward | Swipe left |
| Rewind | Swipe right |
| Menu | Tap ☰ |
| Details | Swipe up |

### Player Buttons

| Button | Action |
|--------|--------|
| ⬅️ | Return to library |
| ▶️ / Resume | Start or resume video |
| ⏮️ Restart | Play from beginning |
| ⏭️ Skip Intro | Jump forward 85 seconds |
| ⏭ Next Ep | Jump to next episode (TV only) |
| 📺 Episodes | Browse all episodes (TV only) |
| ⛶ | Fullscreen toggle |

## 🆘 Troubleshooting

| Issue | Solution |
|-------|----------|
| **No video files found** | Check folder has supported formats (mp4, mkv, avi, webm, m4v). Try a folder with fewer files first. |
| **Audio only, no video** | Your browser doesn't support the codec. Convert to MP4 (H.264) using FFmpeg or Handbrake. |
| **Progress not saving** | Check browser allows `localStorage`. Don't use incognito/private mode. Clear cache. |
| **Video plays slowly** | Too many files? Split into multiple folders. Check available RAM. Refresh page. |
| **Posters not appearing** | Takes 30 seconds on first load. Refresh after 1 minute. Check show/movie names match TMDB database. |
| **Library loads slowly** | Limit folder to <1000 files. Check system has 2GB+ RAM. Try async folder scan. |
| **Can't add folders (Safari)** | iOS has limited directory picker support. Use file-by-file selection instead. |
| **Library doesn't restore** | Check browser allows `localStorage`. Enable in settings → privacy. |

**Still stuck?** Check browser console (`F12`) for errors. File an issue with:
- Browser & version
- OS
- Video format
- Error message (screenshot)
- Steps to reproduce

---

## 🛠️ Tech Details

### Architecture

- **Single HTML file** (~100KB) with embedded CSS and JavaScript
- No build process, no dependencies, no Node modules
- Runs entirely in the browser using modern web APIs
- Service Worker for offline support and asset caching

### Key Technologies

| Component | Technology |
|-----------|-----------|
| **UI** | HTML5 + CSS3 (custom theme) |
| **Playback** | Native HTML5 `<video>` element |
| **Storage** | Browser `localStorage` + IndexedDB |
| **File Access** | FileSystem Access API (modern) + File Input (legacy) |
| **Offline** | Service Worker + Cache API |
| **Data Sync** | JSON exports to cloud storage |
| **Posters** | TheMovieDB API (cached locally) |

### Browser Support

| Browser | Version | Notes |
|---------|---------|-------|
| **Chrome/Edge** | 90+ | ✅ Full support, recommended |
| **Firefox** | 88+ | ✅ Works great |
| **Safari** | 14+ | ✅ iOS 15.4+ for directory picker |
| **Opera** | 76+ | ✅ Chromium-based |
| **Samsung Internet** | 14+ | ✅ Android support |

### Performance

- **File size:** ~100KB single HTML file
- **Startup time:** <100ms
- **Memory usage:** ~50-100MB with 500+ files loaded
- **Storage:** ~5-10MB with watch history + posters

### Security

- ✅ No remote code execution
- ✅ No server uploads (data stays local)
- ✅ No tracking or analytics
- ✅ No third-party scripts
- ✅ Content Security Policy friendly
- ✅ Works in restricted browser contexts

---

## 🔒 Privacy

### What Data Is Collected?

**Nothing** — unless you explicitly enable it.

### Data Storage

All data stored locally on your device:

| Data | Location | Sync? |
|------|----------|-------|
| Video library | `localStorage` | Manual only |
| Watch history | `localStorage` | Manual only |
| Watch progress | `localStorage` | Manual only |
| Poster cache | `localStorage` | Manual only |
| Volume setting | `localStorage` | Manual only |

### Third-Party Services

- **TheMovieDB API** (optional): Fetches poster artwork on first load, then cached locally
- **No Google Analytics, Sentry, tracking pixels, or other telemetry**

### Clearing Data

Click **"Clear History"** button to:
- ✅ Delete watch history
- ✅ Delete media library
- ✅ Clear all progress
- ✅ Reset settings

**This cannot be undone** — clear cache if you're deleting accidental.

---

## 🤝 Contributing

Found a bug? Want a feature? Contributions welcome!

### How to Contribute

1. **Report bugs** — Open an issue with browser console errors
2. **Suggest features** — Open an issue with use case
3. **Submit code** — Fork, edit `omarflix.html`, submit PR
4. **Improve docs** — Edit README.md or add comments

### Development Setup

No setup needed! Just:
1. Edit `omarflix.html` in any text editor
2. Open in browser with `Ctrl+Shift+R` (hard refresh)
3. Check browser console (`F12`) for errors

### Code Structure

```
omarflix.html
├── <head>
│   ├── Meta tags
│   ├── Manifest
│   └── <style> (CSS)
├── <body>
│   ├── Navigation
│   ├── Landing page
│   ├── App interface
│   ├── Player modal
│   └── <script> (JavaScript)
│       ├── Constants & Config
│       ├── Storage functions
│       ├── File detection
│       ├── Playback control
│       ├── UI rendering
│       └── Event listeners
└── Service Worker (inline)
```

### Areas for Contribution

- [ ] Subtitle support (SRT, ASS, VTT)
- [ ] Scene detection
- [ ] Keyboard customization
- [ ] Theme support (light/dark mode)
- [ ] Watchlist / Favorites
- [ ] Collections / Playlists
- [ ] Performance optimization
- [ ] Accessibility improvements
- [ ] Mobile app packaging

### Development Philosophy

- Keep it single-file
- No external dependencies
- Max ~150KB file size
- Support modern & legacy browsers
- Works fully offline
- Zero tracking

---

## 📝 License

MIT License — See [LICENSE](LICENSE) for details.

**In short:** Use, modify, and distribute freely. No restrictions, no warranties.

---

## 🙏 Acknowledgments

- Video codec support provided by browser vendors (Firefox, Chrome, Safari, Edge)
- Poster artwork from [TheMovieDB](https://www.themoviedb.org/) API
- Inspired by Netflix, Plex, and other media players
- Thanks to everyone who tested and provided feedback

---

**Made with ❤️ for your private cinema**

*Watch locally. Control everything. No tracking. No accounts. Just your videos.*

📧 Got questions? Open an issue on GitHub.

---

**Updated:** March 12, 2026

