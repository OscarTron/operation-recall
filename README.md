# Operation Recall

[![Live Demo](https://img.shields.io/badge/Live_Demo-GitHub_Pages-18a999?style=for-the-badge)](https://oscartron.github.io/operation-recall/)
[![License: MIT](https://img.shields.io/badge/License-MIT-18334f?style=for-the-badge)](LICENSE)
[![Built with JavaScript](https://img.shields.io/badge/Built_with-Vanilla_JavaScript-f4c95d?style=for-the-badge)](#technical-overview)

A responsive, session-based secret agent memory trainer for children. It combines short observation, recall, and reporting missions into repeatable training days without accounts, advertising, or paid services.

**[Try the live application](https://oscartron.github.io/operation-recall/)**

## Project Overview

This project began as a companion to Multiplication Practice: a focused tool to help children practice observing carefully, holding information in mind, and recalling it accurately. The secret agent theme keeps short practice sessions playful while the underlying skills stay simple and repeatable.

The product follows one central learning rule: **observe first, then recall from memory**.

## Portfolio Highlights

- Built a complete responsive application with HTML, CSS, and vanilla JavaScript
- Designed six distinct mission types around observation, sequence, and recall
- Implemented five adaptive difficulty levels with step-back after two struggles
- Added a session no-repeat guard that re-rolls recent trays, codes, cards, scenes, routes, and briefs
- Created ranks from Cadet to Master Spy, with stars, streaks, and a mission log
- Kept the experience kid-safe: no login, no chat, no ads, and no data sent elsewhere
- Developed a consistent mobile design system for controls, typography, spacing, and feedback

## Practice Rules

- A training day contains three missions.
- Every mission follows the same loop: observe, the information disappears, recall it, then review the debrief tip.
- There is no fail screen. If a child struggles twice, the level steps back.
- Sound is off by default.
- Every color clue is paired with a shape or label, never color alone.

## Missions

- **Tray Recall:** memorize objects, then say what is missing or pick what was shown.
- **Code Sequence:** repeat flashing color and shape pads in order, with six pads at every level.
- **Agent ID:** memorize an agent card, then answer questions about it.
- **What's Changed?:** spot changes in a scene after the lights go out.
- **Route Recall:** retrace a lit-up route in order.
- **Mission Brief:** read a short brief, then report back who, where, the code word, and the first step.

## Variety

The game is generative, not a fixed slide bank. Missions are re-drawn on every play and answer options are shuffled.

- Tray items: 36
- Scene items: 24
- Route stops: 18
- Mission Brief code words: 14, places: 12, objects: 12
- Code Sequence: 216 possible codes at Level 1, rising to 279,936 at Level 5

The no-repeat guard remembers the last 12 draws for each mission in the current session and re-rolls a collision.

## Features

- Six mission types with adaptive levels
- Stars, ranks, streaks, and a session mission log
- Editable agent codename
- Optional sound toggle, off by default
- Big tap targets and a responsive, keyboard-accessible interface
- Dark mode support through the device color scheme

## Technical Overview

| Area | Implementation |
| --- | --- |
| Front end | Semantic HTML, responsive CSS, vanilla JavaScript |
| State | Session-only; nothing is stored or sent elsewhere |
| Offline support | None; the page loads from GitHub Pages |
| Deployment | GitHub Pages |
| Dependencies | Google Fonts for display text; no runtime JavaScript dependencies |
| Privacy | No accounts, analytics, advertising, or remote data collection |

## Architecture

The application is a single self-contained `index.html` file. It keeps mission generation, play logic, scoring, and the mission log in one page so it can be published directly to GitHub Pages without a build system.

## Run locally

Clone the repository and start any static file server:

```bash
git clone https://github.com/OscarTron/operation-recall.git
cd operation-recall
python -m http.server 8000
```

Then open `http://localhost:8000`. The core interface also opens directly from `index.html`.

## Privacy

No player names, scores, or practice history are sent anywhere. Progress in this version lives only in the current page session, so it resets when the page is reloaded or revisited.

## Roadmap

- Persistent device-local progress, matching Multiplication Practice
- More scene items, stops, and brief vocabulary
- A parent-controlled session length setting

## License

Released under the MIT License.
