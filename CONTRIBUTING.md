# Contributing to Omarflix

Thank you for your interest in contributing! This document provides guidelines and instructions for contributors.

## Getting Started

1. **No Build Process** — This is a single HTML file. No tools needed!
2. **Edit** `omarflix.html` in any text editor
3. **Test** — Open in your browser with `Ctrl+Shift+R` (hard refresh)
4. **Debug** — F12 to open browser console for errors

## Development Guidelines

### Code Style

- Use `'use strict';` at top of script
- Comment complex logic with `// ──` section headers
- Keep functions focused and small
- Use descriptive variable names
- Group related code in sections

### Before Making Changes

- Read through the existing code structure
- Check the `<script>` section outline:
  - Constants & CONFIG
  - DOM references
  - State variables
  - Storage functions
  - File detection & parsing
  - Playback control
  - UI rendering
  - Event listeners

### What to Work On

✅ **Good for contributions:**
- Bug fixes
- Performance improvements
- Accessibility enhancements
- Better error messages
- Documentation improvements
- Code comments and cleanup
- UI/UX tweaks
- New features (with discussion first)

❌ **Not suitable:**
- Minifying code (keep readable)
- Adding external dependencies
- Changing to multi-file structure
- Removing features
- Breaking changes without discussion

### Adding Features

1. **Discuss first** — Open an issue to discuss larger features
2. **Keep it small** — Prefer incremental additions
3. **Test thoroughly** — Works on desktop, mobile, various browsers
4. **Update docs** — Add comments and update README.md if needed
5. **Single file only** — Must stay as single HTML file

### Submitting Changes

1. **Fork** the repository
2. **Create a branch** — `git checkout -b feature/your-feature-name`
3. **Make changes** — Edit `omarflix.html`, update README.md if needed
4. **Test** — Verify on Chrome, Firefox, Safari if possible
5. **Commit** — Clear, descriptive commit messages
   ```
   git commit -m "Add subtitle support for SRT files"
   git commit -m "Fix: Next episode button appears when no next ep"
   git commit -m "Improve: Mobile responsiveness on landscape mode"
   ```
6. **Push** — `git push origin feature/your-feature-name`
7. **Pull Request** — Open PR with description of changes

## Bug Reports

Found a bug? Open an issue with:

```
**Description:** What's the issue?

**Steps to Reproduce:**
1. Open app
2. Click X
3. The problem occurs

**Expected Behavior:**
What should happen?

**Actual Behavior:**
What actually happens?

**Environment:**
- Browser: Chrome/Firefox/Safari + version
- OS: Windows/Mac/Linux
- Device: Desktop/Mobile
- Video format: MP4/MKV/etc

**Console Errors:**
(F12 → Console tab, paste any red errors)
```

## Feature Requests

Have an idea? Open an issue with:

```
**Feature:** What should Omarflix do?

**Use case:** Why would this be useful?

**Implementation Ideas:** (optional) How might this work?

**Similar Products:** How do other apps handle this?
```

## Code Review Process

- **Maintainer feedback** — May request changes or improvements
- **Be patient** — PR review may take a few days
- **Iterate** — Discuss any concerns and update as needed
- **Merge** — Once approved, your contribution is live!

## Areas Needing Help

- [ ] **Subtitle support** — SRT, ASS, VTT file parsing
- [ ] **Performance** — Optimize for 1000+ files
- [ ] **Accessibility** — ARIA labels, keyboard navigation
- [ ] **Mobile fixes** — iOS Safari edge cases
- [ ] **Scene detection** — Auto-generate chapters
- [ ] **Tests** — Unit test framework
- [ ] **Themes** — Light mode option
- [ ] **Internationalization** — Multi-language UI
- [ ] **Documentation** — API docs, code walkthroughs

## File Size Constraints

- **Max file size:** ~150KB (currently ~100KB)
- **No external scripts** — All code must be inline
- **No CSS frameworks** — Custom CSS only
- **Minimize dependencies** — Use only browser APIs

## Performance Optimization

When optimizing, remember:

```javascript
// ✅ Good — Direct, fast
const items = mediaFiles.filter(f => f.type === 'movie');

// ❌ Avoid — Loops, DOM thrashing
for (let i = 0; i < mediaFiles.length; i++) {
  if (mediaFiles[i].type === 'movie') element.innerHTML += ...;
}

// ✅ Debounce events
let searchTimeout;
searchInput.addEventListener('input', (e) => {
  clearTimeout(searchTimeout);
  searchTimeout = setTimeout(() => search(e.target.value), 300);
});
```

## Browser Compatibility

Test on:

- **Chrome** (latest two versions)
- **Firefox** (latest two versions)
- **Safari** (latest two versions)
- **Mobile** (iOS Safari, Chrome mobile)

Use no features newer than:
- DOM APIs: ES2015+
- CSS: CSS Grid/Flexbox (avoid bleeding edge)
- Video: HTML5 `<video>` standard APIs only

## Documentation

When updating features, also update:

- `README.md` — Add usage instructions
- Inline comments — Explain complex code
- HTML comments — Document new features
- CHANGELOG (if applicable)

## Questions?

- Check README.md for features and usage
- Look at existing code for examples
- Open an issue with questions
- GitHub Discussions for general chat

## Code of Conduct

- Be respectful to all contributors
- No harassment or discrimination
- Welcome diverse perspectives
- Assume good faith
- Report violations to maintainers

---

**Thank you for contributing to Omarflix!** 🎬

Your efforts help make this a better, more private media player for everyone.
