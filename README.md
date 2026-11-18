# CS2 Research

A C++ reverse-engineering sandbox for exploring Counter-Strike 2 and parts of the Source 2 client.

## What I explored

- A Dear ImGui schema browser for inspecting entity types and fields.
- Entity and weapon overlays that project selected in-game data onto the screen.
- Experiments with client rendering and material changes; some features are incomplete.
- A separate manual-mapping experiment in `ManualMapper/`.

The code is version-specific and experimental. It includes ESP-style client overlays that can reveal information not normally shown to players, so it is not appropriate for online or competitive matches.

## Project layout

- `CS2i/` contains the Source 2 inspection and overlay prototype.
- `ManualMapper/` is a separate Windows PE-loading experiment.
- `res/` contains project assets.

The Visual Studio solution and vcpkg manifests are included for Windows development. This repository is a record of reverse-engineering experiments, not a maintained or supported game tool.

## Defensive analysis

See [DEFENSIVE_ANALYSIS.md](DEFENSIVE_ANALYSIS.md) for a discussion of client-side information exposure and defensive design considerations. The note does not evaluate or claim to bypass any specific anti-cheat.
