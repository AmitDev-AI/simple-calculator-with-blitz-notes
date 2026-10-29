# Calculator + Notes

A single-file calculator and notepad app built with plain HTML, CSS, and vanilla JavaScript. No frameworks, no libraries, no build step, no network requests.

**Live demo:** https://amitdev-ai.github.io/My-Calc/

## Features

- Split-screen layout: calculator on the left, notes on the right
- Responsive — panels stack below 720px
- Automatic light/dark theme via `prefers-color-scheme`
- Calculator with expression line, chained operations, percent, sign toggle, and a 15-digit input cap
- Float-safe results (`0.1 + 0.2` shows `0.3`)
- Friendly divide-by-zero message that recovers on the next key press
- Full keyboard support
- Notes autosave to `localStorage` (debounced ~400 ms, plus save on page unload)
- **Extras:** accent palette switcher, paper tape of recent calculations, click-to-copy result, export notes as `.txt`

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `0`–`9`, `.` | Enter a number |
| `+` `-` `*` `/` | Operators |
| `Enter` or `=` | Evaluate |
| `Backspace` | Delete last digit |
| `Esc` or `Delete` | Clear |
| `%` | Percent |

Shortcuts are ignored while the notes textarea has focus.

## Run locally

Download `calculator-notes.html` and double-click it — it opens directly in Edge or Chrome. Notes are stored in your browser under the key `calculator-notes:notes:v1`, so they persist across refreshes.

## Repo layout

| File | Purpose |
| --- | --- |
| `calculator-notes.html` | The app |
| `index.html` | Identical copy served by GitHub Pages at the site root |

If you edit the app, copy the changes to `index.html` and push so the live site updates.
