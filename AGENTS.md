# Repository Guidelines

## Project Structure & Module Organization

- `src/extension.ts`: main VS Code extension (commands, webview, config plumbing).
- `out/`: compiled JavaScript (`tsc` output) shipped by the extension; update via build, not by hand.
- `init.R`: bootstrap script injected into R sessions by the extension.
- `plot_server.R`: R-side WebSocket server + plot capture/resize logic.
- `assets/`: extension assets (e.g., `assets/icon.png`).
- `node_modules/`: vendored npm dependencies (tracked in git in this repo).

## Build, Test, and Development Commands

- `mamba run -n base npm run compile`: compile TypeScript into `out/` (also used for publishing).
- `mamba run -n base npm run watch`: recompile on changes while developing.
- VS Code dev loop: open the repo in VS Code → press `F5` to launch an “Extension Development Host”.
- Package a VSIX: `mamba run -n base npx -y @vscode/vsce package`.

## Coding Style & Naming Conventions

- TypeScript: 4-space indentation, semicolons, single quotes; keep changes localized to `src/` and regenerate `out/`.
- R: prefer `<-`, `snake_case`, and minimal global side effects (use `.GlobalEnv` only where the extension relies on it).

## Testing Guidelines

- No automated test suite currently. Validate by running the extension (F5) and generating base R and `ggplot2` plots in a VS Code R terminal.
- If you change UI/webview behavior, include a screenshot/GIF in the PR when practical.

## Commit & Pull Request Guidelines

- Commit history uses short, descriptive messages; a Conventional Commit prefix appears in places (e.g., `docs:`) and is welcome when it fits.
- PRs should include: summary of changes, manual test steps, and whether `out/` and/or `node_modules/` were modified.

## Runtime & Configuration Notes

- The extension injects `source(Sys.getenv('VSC_R_PLOT_INIT'))` into R terminals and uses `VSCODE_R_PLOT_CONFIG` for session state.
- `plot_server.R` installs required CRAN packages if missing; for offline/locked-down setups, preinstall `httpuv`, `jsonlite`, and `base64enc`.
- The default R environment on this server is `r451` (e.g., `mamba run -n r451 R` / `mamba run -n r451 Rscript script.R`).
