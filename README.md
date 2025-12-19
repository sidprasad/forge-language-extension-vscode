# Forge VSCode Extension


VS Code support for [Forge](https://forge-fm.org/).

## Highlights

- Run Forge files with robust process management (Racket discovery, version checks, graceful stop).
- LSP essentials: go to definition, hover, and document symbols.
- **Intelligent code completion**: 60+ Forge keywords and 9 smart snippets for common patterns.
- Syntax highlighting and language configuration for `.frg`.

## Quick start

1. Install Racket and Forge: `raco pkg install forge`
2. Install the extension from the 
3. Open a `.frg` file and run `Forge: Run` (or click the Run button).

## Code Completion

Smart, non-intrusive completions for Forge. Trigger with **Ctrl+Space** (Windows/Linux) or **Cmd+Space** (Mac), or let it appear naturally as you type.

**Features:**
- **60+ Keywords**: All Forge keywords (`sig`, `pred`, `fun`, `run`, `check`, `all`, `some`, `always`, etc.)
- **9 Smart Snippets**: Common code patterns with tab-stop placeholders:
  - `sig (snippet)` → Full signature declaration template
  - `pred (snippet)` → Predicate with parameters
  - `run (snippet)` → Run command with scope
  - `test expect (snippet)` → Complete test block
  - Quantifiers: `all (snippet)`, `some (snippet)`
  - And more...
- **Context-aware**: Skips completions inside comments and strings
- **Helpful documentation**: Each item includes description and usage info

## Commands

- `Forge: Run`
- `Forge: Stop`
- `Forge: Continue Forge Run`
- `Forge: Enable Logging`
- `Forge: Disable Logging`
- `Forge: Forge Docs`

## Settings

| Setting | Type | Default | Description |
| --- | --- | --- | --- |
| `forge.racketPath` | string | `""` | Path to Racket executable. Leave empty to auto-detect. |
| `forge.minVersion` | string | `"3.3.0"` | Minimum Forge version required. |
| `forgeLanguageServer.maxNumberOfProblems` | number | `100` | Max diagnostics produced by the server. |
| `forgeLanguageServer.trace.server` | string | `"messages"` | LSP trace verbosity. |
