# General DS&A Prep — 30/60/90-Day Professional Plan

A self-contained browser app for professional-level DS&A interview preparation. All settings are stored in `localStorage` — no account, no backend, no build step required.

---

## Overview

| Setting | Default | Options |
|---------|---------|---------|
| Plan length | 30 days | 30, 60, or 90 days |
| Start date | Today | Any date (resets day numbering) |
| Your name | — | Shown in greeting + header |

Open `general-prep.html` in any browser. Use the **Settings** tab to configure your plan.

---

## Plan Lengths

### 30-Day Foundation Sprint (~133 hours)
Best for a focused push before a near-term interview. Covers all core patterns and the most common interview problems.

| Week | Focus | Topics |
|------|-------|--------|
| 1 | Arrays & Hashing | Two pointers, sliding window, sorting, hash maps, strings |
| 2 | Data Structures | Linked lists, stacks, queues, binary trees (DFS + BFS + BST) |
| 3 | Graphs & Search | BFS, DFS, topological sort, Union-Find, binary search, heaps |
| 4 | DP & Advanced | DP (1D + 2D), backtracking, tries, greedy, advanced DP |
| 5 (Days 29–30) | Final Prep | Mock marathon, pattern review, rest |

### 60-Day Advanced Track (~265 hours)
Everything in the 30-day plan plus advanced algorithms and a hard-problem marathon.

| Week | Focus | Topics |
|------|-------|--------|
| 5–6 | Advanced Graphs | Dijkstra, Bellman-Ford, Floyd-Warshall, MST (Kruskal/Prim), SCC |
| 6–7 | Hard DP | Interval DP, bitmask DP, tree DP, string DP (edit distance, regex) |
| 7 | Advanced Structures | Segment trees, Fenwick trees, KMP, bit manipulation |
| 8 | Hard Problem Marathon | Hard arrays, stacks, trees, graphs, DP, strings — timed |

### 90-Day Full Mastery (~395 hours)
Complete 60-day track plus system design, distributed systems, and interview excellence training. For career transitions or senior-level roles.

| Week | Focus | Topics |
|------|-------|--------|
| 9 | Design Patterns | LRU/LFU cache, iterators, math algorithms, probability |
| 10 | Algorithm Mastery | Network flow, geometry, randomized algorithms, amortized analysis |
| 11 | System Design | Scalability, CAP theorem, distributed systems, database design, API design, OOD |
| 12 | Interview Excellence | Behavioral (STAR), communication, whiteboard coding, pressure training, mock marathon |

---

## Tabs

| Tab | Contents |
|-----|----------|
| **Home** | Countdown, today's schedule with clickable links, quick actions, motivational quotes |
| **N-Day Plan** | Full day grid grouped by week with phase labels. Week filter to jump to any week. |
| **Patterns** | 7 annotated pattern templates (Two Pointers → DP) |
| **Flashcards** | 82 flashcards with 3D flip animation. Filters: All / Arrays / Trees / Graphs / DP / Advanced / Strings / Complexity / Design / Misc |
| **Problems** | 15 problems (10 medium + 5 hard) with brute + optimal annotated code. Filter by difficulty, pattern, or day. |
| **Mock Timer** | 45-minute countdown with protocol reminders and problem selection |
| **Tips** | Time management, communication, traps, pattern triggers |
| **Ritual** | 8-step interview ritual + pattern→algorithm table + 7 core templates |
| **Reference** | Python idioms, gotchas, 7 detailed annotated templates |
| **Data Structures** | 9 structures (Array → Trie) with complexity tables, annotated code, LeetCode links |
| **Algorithms** | 9 algorithms (Binary Search → Union-Find) with annotated code and LeetCode links |
| **Focus** | 20 focus and retention techniques (Active Recall, Spaced Repetition, Feynman, etc.) + spaced repetition schedule + weekly review checklist |
| **Settings** | Plan length (30/60/90), name, start date, current plan stats |

---

## Flashcard Categories

82 cards across 10 categories:

| Category | Count | Covers |
|----------|-------|--------|
| Arrays | 14 | Two pointers, sliding window, binary search (3 forms), prefix sums, Kadane's, kth element |
| Trees | 10 | Traversals, BST, LCA, validation, heaps, segment trees, Fenwick trees |
| Graphs | 14 | BFS/DFS, topological sort, Dijkstra, Bellman-Ford, Floyd-Warshall, MST, Union-Find, SCC |
| DP | 11 | Recognition, recurrences (Fibonacci, knapsack, LCS, edit distance, LIS), interval DP, bitmask DP, tree DP |
| Advanced | 7 | Dijkstra, Bellman-Ford, Floyd-Warshall, MST, Union-Find, segment trees, Fenwick trees |
| Strings | 6 | KMP, Rabin-Karp, Manacher's, anagram detection, Python string complexities |
| Complexity | 8 | Amortized O(1), Master Theorem, heapsort, quicksort, Python list + heapq ops, DFS/BFS |
| Design | 6 | CAP theorem, consistent hashing, SQL vs NoSQL, LRU cache, sharding, load balancers |
| Misc | 12 | Linked lists, backtracking, pattern ID, Python tools, trie, quickselect, Boyer-Moore, reservoir sampling |

---

## Hard Problems

Five hard LeetCode problems with full brute force + optimal annotated code:

| # | Problem | Pattern |
|---|---------|---------|
| 11 | Trapping Rain Water | Two pointers |
| 12 | Edit Distance | 2D DP |
| 13 | Sliding Window Maximum | Monotonic deque |
| 14 | Serialize & Deserialize Binary Tree | BFS / tree design |
| 15 | N-Queens | Backtracking with diagonal sets |

---

## Floating Buttons

| Button | Color | Action |
|--------|-------|--------|
| Ask Claude | Anthropic orange | Copies context-aware prompt to clipboard → opens claude.ai/new |
| Ask Gemini | Google blue | Copies prompt → opens gemini.google.com/app |
| Ask ChatGPT | OpenAI green | Copies prompt → opens chatgpt.com |

Each button builds a prompt containing your plan context + the topic of the current tab.

---

## Persistent Widgets

- **Pomodoro clock** (bottom-left) — 25/5 minute work/break cycles, auto-switches, session counter, minimizable
- **Side timer** (right edge, vertically centered) — general countdown, adjustable in 15-minute increments (15m–120m)

---

## Local Storage Keys

| Key | Value |
|-----|-------|
| `dsaplan_start` | ISO date string — plan start date |
| `dsaplan_length` | `30`, `60`, or `90` |
| `dsaplan_name` | Your name string |

Clear with `localStorage.clear()` in the browser console to reset everything.

---

## Tech

- React 18 (CDN, no npm)
- Babel Standalone (in-browser JSX)
- Fira Code + Inter (Google Fonts)
- No build step — open the file or serve as static
