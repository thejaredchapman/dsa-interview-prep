# DS&A Interview Prep

Two self-contained browser apps for data structures and algorithms interview preparation. No build step — open any `.html` file directly or deploy as a static site.

## Files

| File | Description |
|------|-------------|
| `index.html` | Pinterest-specific 9-day sprint (Jun 3–12) |
| `general-prep.html` | Company-agnostic 30/60/90-day professional plan |

---

## `index.html` — Pinterest DS&A Sprint

A focused 9-day study guide targeting a specific Pinterest engineering interview.

**Tabs:** Home · 9-Day Plan · Patterns · Flashcards · Problems · Mock Timer · Tips · Ritual · Reference · Data Structures · Algorithms

**Features:**
- Live countdown timer to interview date
- 9-day card grid with today highlighted and per-day hover colors
- 7 annotated pattern templates (Two Pointers → DP)
- 20 flashcards with CSS 3D flip animation
- 10 problems with brute/optimal annotated code + LeetCode links
- 45-minute mock timer with protocol
- Interview ritual checklist (8 steps)
- Reference tab (Python idioms, gotchas, 7 detailed templates)
- Data Structures tab (9 structures with complexity tables + code)
- Algorithms tab (9 algorithms including 4-approach Kth Element)
- Pomodoro clock (bottom-left), side timer (right edge, 15-min increments)
- Ask Claude / Ask Gemini / Ask ChatGPT floating buttons

---

## `general-prep.html` — 30/60/90-Day Professional Plan

A company-agnostic interview prep system with configurable plan length, stored locally.

See [general-prep.md](./general-prep.md) for full documentation.

---

## Tech Stack

- React 18 (via CDN)
- Babel Standalone (in-browser JSX transpilation)
- Fira Code + Inter (Google Fonts)
- No npm, no build step, no dependencies

## Usage

```bash
# Open locally
open index.html
open general-prep.html

# Or serve locally (for mobile testing)
python3 -m http.server 8080
# then open http://localhost:8080 on any device
```
