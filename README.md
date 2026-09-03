# Tournament-Creator

Tournament-Creator is a lightweight browser-based app for running a **King of the Hill** style pool tournament. It supports player setup, table assignment, live match tracking, queue rotation, standings, and quick utility pages.

Can open official Github Hosted site at https://mahoneygd.github.io/Tournament-Creator/

## Features

- Start a tournament from a list of player names
- Configure number of active tables
- Configure max consecutive win streak before rotation
- Track live matches and report winners
- Auto-manage player queue and table reuse
- Maintain standings (wins, points, games played)
- Add players mid-tournament
- Undo the last action
- Persist tournament data in `localStorage`
- Utility pages:
  - Name/pair randomizer
  - Extended standings view with opponents faced and average opponent rank

## Project Structure

- `/docs/index.html` – Main tournament UI
- `/docs/app.js` – Tournament logic and state handling
- `/docs/utils/randomize.html` – Name/pair randomizer tool
- `/docs/utils/standings.html` – Extended standings page
- `/assets/9Ball_rack.PNG` – App favicon/image asset

## Getting Started

This project is static HTML/CSS/JS and does not require a build step.

### Option 1: Open directly

Open `/home/runner/work/Tournament-Creator/Tournament-Creator/docs/index.html` in your browser.

### Option 2: Run a local static server (recommended)

From the repository root (`/home/runner/work/Tournament-Creator/Tournament-Creator`), run one of:

- Python 3:
  - `python3 -m http.server 8000`
- Node (if you have `serve` installed):
  - `npx serve docs`

Then open:

- `http://localhost:8000/docs/` (Python)
- or the URL shown by `serve`

## How to Use

1. Enter player names (one per line).
2. Set number of tables and max win streak.
3. Click **Start Tournament**.
4. Report each match winner from the active match cards.
5. Use **Undo** to revert the last action if needed.
6. Use **Exec Only Button** for expanded standings details.
7. Use **Randomizer** for quick shuffled names/pairs.

## Data Persistence

Tournament state is saved in browser `localStorage` under the key `tournamentData`.

- Refreshing the page restores saved state.
- Clicking **Reset** clears in-memory state and removes saved local storage data.

## Notes

- This project is currently front-end only.
- No authentication, backend, or multi-user sync is included.
