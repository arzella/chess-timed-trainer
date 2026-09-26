# Chess Timed Trainer

A single-page chess tactics trainer: timed thinking and review phases, full-line puzzle
checking, a local Stockfish engine, Lichess puzzle import, a personal puzzle rating,
per-theme strengths and weaknesses, and line replay.

Everything lives in `index.html`. There is no build step.

## Run locally

Open `index.html` in a browser. An internet connection is needed for chess.js,
the piece images and the Stockfish engine, which are loaded from public CDNs.

## Deploy

This repository is connected to Vercel. Every push to `main` publishes a new production
version. To update, replace `index.html` and commit.

## Third-party components

- [chess.js](https://github.com/jhlywa/chess.js) 0.10.3 (BSD-2-Clause), loaded from cdnjs.
- [Stockfish.js](https://github.com/nmrugg/stockfish.js) 19 lite (GPLv3), loaded from unpkg at runtime;
  fallback Stockfish 10 (GPLv3) from cdnjs.
- [fzstd](https://github.com/101arrowz/fzstd) 0.1.1 (MIT), inlined in `index.html`, used to read
  `lichess_db_puzzle.csv.zst`.
- Piece images from [Lichess](https://github.com/lichess-org/lila) (see their licenses per piece set).
- Puzzles: [Lichess puzzle database](https://database.lichess.org/#puzzles) (CC0) and the Lichess API.
