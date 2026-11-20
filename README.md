# devtools

Install-or-update script for a fresh Ubuntu machine.

- asdf (bootstrapped if missing): erlang, elixir, python
- VS Code via Microsoft's apt repo
- Flatpak apps from Flathub (Bambu Studio)

```
./devtools                # everything
./devtools python elixir  # only some asdf tools
./devtools --no-system --no-vscode --no-flatpak
```

Add asdf tools to `ASDF_TOOLS` and Flathub apps to `FLATPAK_APPS` at the top of the script.
