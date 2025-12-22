# Game Contracts

This repository defines the **canonical API and event contracts**
used by all game services in the platform.

Contracts in this repository are the **single source of truth** for:
- WebSocket message formats
- Room lifecycle events
- Game-specific actions and state schemas

This repository contains **no runtime code**.

---

## Structure

- `global/`
  Shared contracts that apply to all games

- `games/`
  Game-specific contracts isolated per game

- `_template/`
  Template for adding new games

---

## Rules

- Runtime code is forbidden
- Game services must not redefine contracts locally
- A game service may only consume:
  - `global/*`
  - `games/<its-own-game>/*`
- Games must never import other games’ contracts
