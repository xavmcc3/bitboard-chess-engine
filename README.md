# bitboard-chess-engine
A simple implementation of a bitboard-based chess engine

## Building
Building with CMake using MYSYS2 on windows.

## Project Structure
`/apps` — Executable entry points (Handle CLI args, high-level orchestration, exit codes)
`/include/chessengine` — Public API headers for external users/apps
`/src` — Internal source code and private headers
`/tests` — Unit tests/integration tests
