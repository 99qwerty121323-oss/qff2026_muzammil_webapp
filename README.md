# QFF PLUS 2026 — Live Python Quantum Oracle & Grover Web App

Interactive web dashboard powered by a pure Python 3 backend (`server.py`) that executes the Qiskit Fall Fest NUST 2026 Hackathon quantum oracle, Grover's algorithm, amplitude evolution, dynamic twin-prime scaling, and Monte Carlo shot-budget reliability analysis in real time.

## Features
- **Core 2×2 Binary Puzzle (Steps 1–4):**
  - Classical enumeration of all 16 grids (`0110`, `1001`) and 3-CNOT comparison pattern (`110`)
  - Qiskit little-endian bit-order checkpoint (`0001` → `1000`)
  - Exact 4-qubit gate-level oracle (`cx` → `x(3)` → `CCZ(1,2,3)` → uncompute) + 16-basis restoration check
  - Live Grover histogram, all-16-amplitude stage viewer, and `k = 0…4` over-rotation sweep
- **Dynamic Twin-Prime Extension (Main Extension Parts 1–4):**
  - Enter any `n_limit` (e.g. `100`, `1000`, `2000`, `8796`, `83457`) — qubits, ancillas, `k`, and shot budgets scale automatically
  - Automatic mode switching (`v-chain` for `NIDX ≤ 10`, 0-ancilla `diagonal` for larger `n_limit`)
  - Recovered twin-prime distribution, iteration sweep (`1,000` vs. `10,000` shots), and 200-trial Monte Carlo shot-budget accuracy chart

## Quick Start (Zero External Dependencies)
```bash
python3 server.py
```
Then open `http://127.0.0.1:8765` in your browser.
