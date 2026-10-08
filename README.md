# PocketCade Game Packs

Public, data-only game package catalog for PocketCade.

This repository intentionally contains **no PocketCade application source code, executable Dart, or credentials**. PocketCade keeps trusted reusable game engines and renderers in the private app repository and downloads versioned JSON definitions from here.

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
