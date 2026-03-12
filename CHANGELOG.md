# Changelog

All notable changes to Omarflix are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [1.0.0] - 2026-03-12

### Added

**Core Features**
- Single HTML file video player for local media
- Support for MP4, MKV, WebM, AVI, MOV, M4V formats
- TV show detection and episode organization
- Movie vs. Show automatic classification
- Built-in web video player with standard controls

**Playback**
- Resume from last position for all videos
- Automatic next episode for TV shows
- Skip intro button (jumps 85 seconds for shows)
- Watch progress tracking (saved real-time every 5 seconds)
- Keyboard shortcuts (Space, F, arrows, S for skip, M for mute)
- Mobile touch gestures (swipe, double-tap, pinch-zoom compatible)

**Library Management**
- Add media folders (local, OneDrive, network drives)
- Auto-organize by movie/show with episode parsing
- Search videos by title or filename
- Filter by type (Movies, TV Shows, In Progress)
- Sort by title, recently watched, or progress percentage
- Quick continue-watching button in library

**TV Show Features**
- Episode browser modal for easy navigation
- Season and episode organization
- "Next Episode" button at 80% through video
- Auto-play next episode when finished
- Episode progress tracking with visual indicators
- Watched episode markers (green checkmarks)

**Watch History**
- Automatic progress saving to localStorage
- Resume positions stored for every video
- Completion tracking (watched, in-progress, not started)
- Last watched timestamp
- Progress percentage display

**Cross-Device Support**
- Manual sync export as JSON file
- Sync configuration storage
- Multi-device watch history merging
- Cloud folder support (Google Drive, OneDrive, Dropbox)
- 30-second auto-sync interval when enabled

**UI/UX**
- Netflix-inspired dark theme (red accents)
- Responsive design (desktop, tablet, mobile)
- Hamburger menu for mobile navigation
- Poster artwork from TheMovieDB API (cached locally)
- Smooth animations and transitions
- Modal dialogs for episodes and settings
- Touch-friendly mobile interface

**PWA & Offline**
- Service Worker registration for offline support
- Asset caching for better performance
- Install as app on iOS and Android
- Works offline after initial load
- Cache-first strategy for resources

**Accessibility & Performance**
- Semantic HTML structure
- Keyboard navigation support
- Dark mode theme for reduced eye strain
- Efficient localStorage usage
- Fast folder scanning with async operations
- Poster caching for quick load times

**Data Management**
- All data stored locally in browser `localStorage`
- Settings backup/export functionality
- Clear history with one button
- Selective folder removal
- No cloud uploads without user action

### Technical

- Pure JavaScript, no external dependencies
- ~100KB single HTML file
- ES2015+ JavaScript features
- CSS Grid and Flexbox layout
- HTML5 `<video>` element
- FileSystem Access API with File Input fallback
- localStorage for data persistence
- Service Worker for offline support
- TheMovieDB API integration for posters

### Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+ (iOS 15.4+ for directory picker)
- Opera 76+
- Any modern browser with HTML5 video support

### Documentation

- Comprehensive README.md with setup guides
- Code comments and documentation
- Contributing guide with development setup
- License (MIT)
- This changelog

---

## Future Roadmap

### Planned Features

- [ ] Subtitle support (SRT, ASS, VTT)
- [ ] Scene/chapter detection
- [ ] Watchlist and favorites
- [ ] Custom collections/playlists
- [ ] Light theme support
- [ ] Keyboard customization
- [ ] Theme customization (accent colors)
- [ ] Multi-language UI
- [ ] Bookmarks for resume points
- [ ] Video transcoding/conversion
- [ ] Sync conflict resolution
- [ ] Advanced search filters
- [ ] User profiles per device
- [ ] Bulk import/export

### Under Consideration

- Desktop Electron app (for simpler distribution)
- Mobile native apps (iOS/Android)
- Server backend for advanced syncing
- Collaborative watchlists
- Social features (what friends are watching)
- Recommendations based on watch history

---

## Known Limitations

- Single browser instance only (no cross-tab sync)
- localStorage size may limit very large libraries (varies by browser)
- Some older codecs may not be supported (browser limitation)
- iOS directory picker limited on older Safari versions
- Requires browser filesystem access permissions

---

## Deprecations

None yet.

---

## Security

### In This Release

- ✅ No remote code execution vulnerabilities
- ✅ No SQL injection (no database)
- ✅ No XSS vulnerabilities (proper sanitization)
- ✅ No data exfiltration (all local)
- ✅ No tracking or telemetry

### Security Considerations

- Data stored in browser can be accessed by other websites on same domain if not HTTPS
- Use HTTPS if hosting on web server
- Clear browser history to delete watch data
- Incognito mode won't persist watch history between sessions

---

## Attribution

Built with:
- HTML5 `<video>` API
- Browser localStorage
- TheMovieDB API (poster artwork)
- Font: Outfit from Google Fonts

---

## Contributing

See CONTRIBUTING.md for guidelines on contributing to Omarflix.

All contributors welcome! Areas needing help:
- Subtitle support
- Performance optimization
- Accessibility improvements
- Bug fixes
- Documentation

---

**Omarflix v1.0** — Your private cinema awaits! 🎬
