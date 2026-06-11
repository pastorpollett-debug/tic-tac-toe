# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-file browser Tic Tac Toe game (`tictactoe.html`) with no build step, no dependencies, and no package manager. Open the file directly in a browser to run it.

```
start tictactoe.html
```

## Architecture

Everything lives in `tictactoe.html` — HTML structure, CSS styles, and JavaScript game logic are all inline in one file.

**Game logic** (in the `<script>` tag):
- `board` — 9-element array tracking `'X'`, `'O'`, or `null` for each cell
- `WINS` — hardcoded array of the 8 winning index combinations
- `handleClick(i)` — main event handler; updates board state, checks for win/draw, switches turns
- `init()` — resets board and UI for a new game; scores persist across calls

**Scores** are tracked in a plain object `{ X, O, D }` and survive new games within the same browser session (not persisted to storage).

## Git / GitHub

- Remote: `https://github.com/pastorpollett-debug/tic-tac-toe`
- Default branch: `master`
- Push changes with a descriptive commit message after every meaningful edit
