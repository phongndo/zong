# zong

A simple local multiplayer Pong clone written in Zig with raylib bindings.

The project is intentionally small, which makes it a good starter project for experimenting with Zig game loops, collision logic, and basic 2D rendering.

## Features

- Local two-player Pong gameplay
- Paddle movement for both players
- Ball bounce angles based on paddle contact
- Live score display
- Minimal single-file game loop

## Controls

- Player 1: `W` / `S`
- Player 2: `Up` / `Down`
- Quit: close the window

## Requirements

- Zig `0.15.2`
- A desktop environment that can open a raylib window

The `raylib-zig` dependency is defined in `build.zig.zon`, so you do not need to install raylib separately for this project. The dependency pin has been updated to a Zig `0.15.x` compatible revision and verified locally with Zig `0.15.2`.

## Run

```bash
zig build run
```

## Test

```bash
zig build test
```

## Project Layout

```text
.
├── build.zig
├── build.zig.zon
└── src
    └── main.zig
```

- `build.zig`: build graph, run step, and test step
- `build.zig.zon`: package metadata and dependencies
- `src/main.zig`: game state, input, physics, rendering

## Development

If you want the fastest local checks before pushing changes:

```bash
zig fmt --check build.zig src/main.zig
zig build test
```
