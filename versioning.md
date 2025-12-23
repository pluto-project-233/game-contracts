# Contract Versioning Rules

## Global Contracts

- Intended to be stable
- Backward-compatible changes only
- Breaking changes are strongly discouraged

## Game Contracts

- Versioned independently per game
- Breaking changes affect only that game
- Version folders (v1, v2) may be introduced if needed

## General Rules

- Breaking changes must be documented
- Services must update before deployment

# Versioning Strategy

- Versioning is **path-based**
- Example: /v1/game/start
- Minor changes must be backward compatible
- Breaking changes require new version folder

Rules:
- v1 is immutable after release
- Multiple versions may coexist
- Orchestrator must support older versions if still in use

