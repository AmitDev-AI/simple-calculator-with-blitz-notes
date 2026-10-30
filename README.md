# Scientific Calculator with Blitz Notes

A single-file scientific calculator with Blitz Notes — plain HTML, CSS, and vanilla JavaScript. No frameworks, no libraries, no build step, no network requests, and no `eval()`.

**Live demo:** https://amitdev-ai.github.io/simple-calculator-with-blitz-notes/

## Features

- Split-screen layout: scientific calculator on the left, Blitz Notes on the right
- Responsive — panels stack below 720px
- Automatic light/dark theme via `prefers-color-scheme`
- Animated gradient background with a subtle engineering grid
- **Scientific engine** (hand-written recursive-descent parser, no `eval()`):
  - `+ − × ÷ ^`, parentheses, and implicit multiplication (`2π`, `3(4+5)`)
  - `sin`, `cos`, `tan` with a DEG/RAD toggle that is remembered
  - `ln`, `log`, `√`, `x²`, `xʸ`, factorial `x!`
  - constants `π` and `e`, plus `Ans` and `EXP` (×10^)
  - live result preview while typing, with friendly error messages
- Float-safe results (`0.1 + 0.2` shows `0.3`) and a 12-significant-digit display
- Divide-by-zero recovery: the next key starts a fresh calculation
- Paper tape of recent calculations — click a chip to reuse the result
- Click the live result to copy it
- **Real-world example chips:** tip, savings growth, and a loan monthly-payment formula
- Blitz Notes autosave to `localStorage` (debounced ~400 ms, plus save on page unload)
- Export notes as `.txt`, or clear them after confirmation

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `0`–`9`, `.` | Enter a number |
| `+` `-` `*` `/` | Operators |
| `^` `(` `)` `%` `!` | Power, brackets, percent, factorial |
| `Enter` or `=` | Evaluate |
| `Backspace` | Delete last character |
| `Esc` or `Delete` | Clear |
| `p` | Insert π |

Shortcuts are ignored while the Blitz Notes textarea has focus.

## Real-world examples

| Chip | Formula | What it solves |
| --- | --- | --- |
| Tip 18% | `84.5×(1+18%)` | Total bill with an 18% tip |
| Savings | `1000×(1.06)^10` | Compound growth of 1,000 at 6% for 10 years |
| Loan | `20000×(.05/12)/(1-(1+.05/12)^(-60))` | Monthly payment on 20,000 at 5% over 5 years |

Load a chip, then edit the numbers in the expression.

## Run locally

Download `amitcalc.html` and double-click it — it opens directly in Edge or Chrome. Notes are stored in your browser under the key `calculator-notes:notes:v1`, so they persist across refreshes.

## Repo layout

| File | Purpose |
| --- | --- |
| `amitcalc.html` | The app |
| `index.html` | Identical copy served by GitHub Pages at the site root |

If you edit the app, copy the changes to `index.html` and push so the live site updates.
