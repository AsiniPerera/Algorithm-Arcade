# Algorithm Arcade

A full-stack web app featuring five classic algorithm puzzle games. Each game is an interactive, playable demonstration of a well-known problem-solving technique — backtracking, recursion, game-tree search, and combinatorial optimization.

## The Games

| Game | Algorithmic theme |
|------|-------------------|
| **Eight Queens** | Backtracking — place 8 queens so none attack each other (includes sequential and threaded solvers) |
| **Knight's Tour** | Path finding / backtracking across a chessboard |
| **Tic-Tac-Toe** | Minimax with a heuristic evaluation for the computer opponent |
| **Tower of Hanoi** | Classic recursion |
| **Traveling Salesman** | Route optimization with an interactive map visualizer |

## Tech Stack

- **Frontend:** React 19, Vite, React Router, Chart.js
- **Backend:** Node.js, Express 5 (ES modules)
- **Database:** Supabase (stores player data and scores)
- **Testing:** Jest / Vitest with React Testing Library

## Project Structure

```
pdsa_project/
├── project_frontend/        # React + Vite client
│   └── src/games/           # one folder per game, each with its own tests
└── project_backend/         # Express API server
    └── routes/              # one route file per game
```

## Getting Started

### Prerequisites
- Node.js (18+ recommended)
- npm

### Backend

```bash
cd project_backend
npm install
npm start          # Express server on http://localhost:5000
```

### Frontend

```bash
cd project_frontend
npm install
npm run dev        # Vite dev server
```

## Running Tests

Each game ships with unit tests.

```bash
cd project_frontend
npm test           # Jest
npm run vite-test  # Vitest
```

## Notes

- The backend exposes game APIs under `/api/*` (e.g. `/api/eightQueensPuzzle`, `/api/knighttour`, `/api/towerofhanoi`).
- Supabase credentials are used by both the frontend and backend; for production, keep keys in environment variables (`.env`) rather than committing them to source.
