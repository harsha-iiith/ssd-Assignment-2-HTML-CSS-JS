CS6.302 — Software System Development
Assignment 2 — HTML, CSS & JavaScript
Roll No: 2025204021

Overview
- This repository contains my solutions for Q1–Q7.
- All implementations are pure client-side HTML/CSS/JavaScript and run locally in a modern browser (Chrome/Firefox/Edge).
- No external backend is required. Open the listed HTML files directly.

Quick Start (Local)
- Q1: Hosted personal site (see links below).
- Q2: Open Q2/newssd.html
- Q3: Open Q3/jigsaw.html
- Q4: Open Q4/stoplight_game.html
- Q5: Open Q5/data_dictionary.html
- Q6: Open Q6/event_tracker.html
- Q7: Open Q7/bowling_game.html

Hosted Links
- Q1 (Personal Website): https://harsha-iiith.github.io/profile/  | Repo: https://github.com/harsha-iiith/profile
- Q2 (Transformed SSD page): https://harsha-iiith.github.io/newssd/  | Repo: https://github.com/harsha-iiith/newssd

Per-Question Notes & How to Run
Q1 — Personal Website (1 mark)
- Deployed on GitHub Pages (link above). Also referenced under Q1/README.txt.

Q2 — CSS/JS Transformed SSD Website (4 marks)
- Local: open Q2/newssd.html.
- Hosted version available (link above). Does not remove original content; only styling/UX improvements.

Q3 — Single-Player Jigsaw Puzzle Maker (5 marks)
- Local: open Q3/jigsaw.html.
- Usage (generic): choose/upload an image (if provided), pick a difficulty setting (e.g., 5/20/40/80/100 pieces), then solve by arranging pieces. Tested in desktop Chrome.
- Assumption: very large images may be downscaled for performance; interaction is mouse-based.

Q4 — Stoplight Game (Computer vs Human) with Comments (10 marks)
- Local: open Q4/stoplight_game.html.
- Usage (generic): pick strategies/inputs as prompted; computer provides random inputs; observe payoffs/outcomes. Code includes descriptive comments.
- Source referenced by problem statement: https://www.youtube.com/watch?v=0i7p9DNvtjk&t=142s

Q5 — Data Dictionary Tool (10 marks)
- Local: open Q5/data_dictionary.html.
- Summary: paste/load schema (JSON/XML/CREATE TABLE DDL) to generate an interactive data dictionary and relationship diagram. Export static HTML or use browser Print → Save as PDF.
- See Q5/README.txt for detailed features, usage guidance, supported formats, and limitations.

Q6 — Event Tracking (5 marks)
- Local: open Q6/event_tracker.html.
- Captures: page views, clicks, focus, and change events.
- Output: visible log panel in the page and console logs with Timestamp | EventType | EventObject. See Q6/README.txt for full details and examples.

Q7 — Bowling Alley Game with Three.js (15 marks)
- Local: open Q7/bowling_game.html (requires WebGL). Use controls for power, direction, spin; optional camera follow and sound.
- Features: 10-frame scoring with strike/spare rules, basic physics/collisions, and scoreboard. See Q7/README.txt for a comprehensive feature list, controls, and notes.

Assumptions
- Browser: modern desktop Chrome/Firefox/Edge; JavaScript enabled; no pop-up/script blockers interfering with local file access.
- File access: for image uploads (Q3) or local resources, run directly from file:// in a modern browser; if a browser blocks local imports, serve via a simple local HTTP server.
- Performance: large images (Q3) or complex schemas (Q5) may impact performance; use reasonable sizes.
- Randomness (Q4): computer’s choices are uniformly random unless otherwise noted.
- No server-side grading hooks; all input/output is visual or via console as required.
