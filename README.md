# Game Contracts

This repository contains **contract-first API definitions** for the game platform.

Contracts in this repository are the **single source of truth** for:
- WebSocket message formats
- Room lifecycle events
- Game-specific actions and state schemas

This repository contains **no runtime code**.

---

## Structure
- `orchestrator/`: Public entry-point APIs
- `lobby/`: Lobby service contracts
- `account/`: Economy & ledger contracts
- `payment/`: Payment provider integration contracts
- `global/`: Shared contracts that apply to all games
- `games/` : Game-specific contracts isolated per game
- `_template/` : Template for adding new games
---

## Rules

- Runtime code is forbidden
- Game services must not redefine contracts locally
- A game service may only consume:
  - `global/*`
  - `games/<its-own-game>/*`
- Games must never import other games’ contracts
- Contracts are **source of truth**
- Services must conform to contracts
- No implementation details here
- Versioned and immutable once released