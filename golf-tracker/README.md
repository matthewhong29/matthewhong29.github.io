# Golf Shot Tracker

A one-page, phone-friendly app for logging golf shots club by club and comparing them to a baseline.

**Live:** https://matthewhong29.github.io/golf-tracker/ (on iPhone: Share → Add to Home Screen)

## What it does
- **Log**: pick a club, enter carry (plus total, left/right miss, and shot shape if you want). Launch monitor numbers (club/ball speed, launch, spin) are optional.
- **Stats**: average carry per club against the baseline, shot-to-shot consistency (±), the usual miss direction, smash factor, a gapping chart, and a dispersion plot for each club.
- **History**: every shot, filterable by club.
- **Settings**: player name and handicap, editable baseline numbers, which clubs are in the bag, CSV export, and JSON backup/restore.

## Baseline numbers
The defaults are rough averages for a mid-handicap (~15) male amateur in his 50s–60s:

| Club | Carry | Club mph | Ball mph | Launch° | Spin |
|---|---|---|---|---|---|
| Driver | 205 | 92 | 131 | 12.5 | 3300 |
| 3W | 185 | 87 | 123 | 11.5 | 3900 |
| 5W | 172 | 84 | 117 | 12.5 | 4400 |
| Hybrid | 165 | 81 | 113 | 13 | 4600 |
| 5i | 155 | 78 | 107 | 14 | 5000 |
| 6i | 145 | 76 | 103 | 15.5 | 5500 |
| 7i | 135 | 74 | 99 | 17 | 6200 |
| 8i | 125 | 72 | 94 | 19 | 7000 |
| 9i | 115 | 70 | 89 | 21 | 7800 |
| PW | 105 | 68 | 84 | 24 | 8500 |
| GW | 90 | 66 | 77 | 27 | 9000 |
| SW | 75 | 64 | 70 | 30 | 9500 |

When you have his real numbers (from a fitting, a launch monitor, or just his normal carries), enter them on the Settings tab. To change the defaults for everyone, edit `DEFAULT_BASELINE` in `index.html`.

## Data
Shots are saved in the browser's localStorage on that one device, with no server or account. Use **Backup (JSON)** now and then and **Restore backup** to move the data to another phone.

## Moving to its own repo
The app is a single file with no dependencies. Copy `index.html` into a new repo and turn on GitHub Pages. The only outside reference is the favicon (`../favicon.svg`).
