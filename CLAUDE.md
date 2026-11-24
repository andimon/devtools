# Agent Instructions

- Only add packages from official publishers; verify the source/maintainer before installing.
- `docs/devtools.tex` documents only the generic machinery of the script (flow, argument handling, helpers, step patterns, asdf handling, CI structure), not individual tools. When you change any of that generic part, update `docs/devtools.tex` (and rebuild `docs/devtools.pdf` with `latexmk -pdf -outdir=docs docs/devtools.tex`) in the same change. Adding or removing a specific tool does not need a doc update.
