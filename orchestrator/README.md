# Game Orchestrator API Contracts

The orchestrator acts as a **coordination layer**, not a business logic owner.

Consumers:
- Client (Web / Flutter)
- Payment provider (Webhook)

Non-consumers:
- Lobby Service
- Game Service
- Account Service

Characteristics:
- Stateless
- Command-driven
- Idempotent
- Firebase Auth based
