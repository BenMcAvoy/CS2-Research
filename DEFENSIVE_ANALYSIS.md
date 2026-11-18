# Defensive analysis: unauthorized client overlays

## Scope

This repository contains a Source 2 schema browser, entity and weapon overlays, rendering experiments, and a separate manual-mapping experiment. The overlay prototype illustrates how information read from a game client can be presented outside the game's normal interface. This document discusses defensive design; it does not claim that the repository implements or tests an anti-cheat.

## Threat model

Assume a client can be modified to inspect local entity data and display information that the normal interface does not show. The question for a game developer is which decisions and information should remain under server control.

## Defensive considerations

- Keep competitive outcomes authoritative on the server. Validate shots and state transitions against server-known positions, timing, and game rules.
- Limit replication of information that a client does not need. If sensitive state is sent to every client, a modified client may be able to expose it.
- Treat local integrity checks as one signal among several. Client-side checks alone cannot establish that the client is trustworthy.
- Evaluate detections against controlled test cases and record false-positive rates before using them to make enforcement decisions.

## Limits

The schema and overlay code is experimental and version-dependent. The repository does not measure detection coverage, evaluate Valve's anti-cheat, or provide a tested defense. The manual-mapping experiment is separate from the entity-inspection discussion above.
