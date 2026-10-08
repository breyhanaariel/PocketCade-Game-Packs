# PocketCade Game Packs

Public, data-only game package catalog for PocketCade.

This repository intentionally contains **no PocketCade application source code, executable Dart, or credentials**. PocketCade keeps trusted reusable game engines and renderers in the private app repository and downloads versioned JSON definitions from here.

## Development release policy

The current game definitions are milestone/test content and intentionally use pre-1.0 game versions such as `0.7.0-dev.1`. The package `schemaVersion` describes the JSON contract and is independent of the game's release version. Final production games will receive game version `1.0.0` only after PocketCade and the game content are complete and release-validated.

## Schema v2

Each canonical game definition now supplies:

- game identity, version, distribution, and trusted engine family
- mechanically meaningful rules such as target score, lives, timing, board/engine parameters, and game-specific content
- presentation roles such as player, collectible, hazard, and instructions
- progression metadata for Stars and achievements

The app validates package identity, version, engine family, required rules, presentation, and progression before promotion to the installed game. A failed update preserves the previous known-good install.

## Library

- 30 canonical game definitions
- 5 bundled/reference games
- 25 downloadable games
- SHA-256 integrity hashes in `catalog.json`
- installed downloadable games remain playable offline
- packages configure trusted PocketCade capabilities; they cannot ship arbitrary executable code
