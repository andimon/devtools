# devtools

Purpose: keeping my devtools consistent across Ubuntu machines.

<table>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/zsh" width="48" height="48" alt="zsh"><br>zsh</td>
    <td align="center" width="120"><img src="https://github.com/ohmyzsh.png" width="48" height="48" alt="Oh My Zsh"><br>Oh My Zsh</td>
    <td align="center" width="120"><b><code>asdf</code></b></td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/erlang" width="48" height="48" alt="Erlang"><br>Erlang</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/elixir" width="48" height="48" alt="Elixir"><br>Elixir</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/python" width="48" height="48" alt="Python"><br>Python</td>
    <td align="center" width="120"><img src="https://raw.githubusercontent.com/microsoft/vscode/main/resources/linux/code.png" width="48" height="48" alt="VS Code"><br>VS Code</td>
    <td align="center" width="120"><img src="https://github.com/sublimehq.png" width="48" height="48" alt="Sublime Merge"><br>Sublime Merge</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/github/181717/white" width="48" height="48" alt="GitHub CLI"><br>GitHub CLI</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/latex" width="48" height="48" alt="LaTeX"><br>LaTeX</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/flatpak" width="48" height="48" alt="Flatpak"><br>Flatpak</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/bambulab" width="48" height="48" alt="Bambu Studio"><br>Bambu Studio</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/todoist" width="48" height="48" alt="Todoist"><br>Todoist</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/claude" width="48" height="48" alt="Claude Code"><br>Claude Code</td>
  </tr>
</table>

To set up tools:

```
curl -fsSL https://raw.githubusercontent.com/andimon/devtools/main/devtools | bash
```

The script will:

- Install the system packages needed to build Erlang and Python from source.
- Install zsh, or upgrade it if it is already installed, and make it your login shell (takes effect at your next login).
- Install [Oh My Zsh](https://ohmyz.sh), or update it if it is already there. On first install, Oh My Zsh moves your existing `~/.zshrc` to `~/.zshrc.pre-oh-my-zsh`.
- Install [asdf](https://asdf-vm.com), the version manager, or update it if a newer version is out.
- Add asdf to your `PATH` in `~/.bashrc` and `~/.zshrc` (only once).
- Install the latest Erlang, then the latest Elixir that works with it, then the latest Python.
- Set those versions as the default ones for your user.
- Install VS Code from the Microsoft apt repository, or upgrade it if it is already installed.
- Install Sublime Merge from the Sublime HQ apt repository, or upgrade it if it is already installed.
- Install the [GitHub CLI](https://cli.github.com) (`gh`) from the GitHub apt repository, or upgrade it if it is already installed.
- Install `pdflatex` and the LaTeX packages needed to build `docs/devtools.tex` (TeX Live from the Ubuntu repositories), or upgrade them if already installed.
- Install Flatpak and the Flathub store if missing, then install Bambu Studio and Todoist or update them.
- Install [Claude Code](https://claude.com/claude-code) with its official installer, or update it if it is already installed that way (a copy installed some other way is left alone).
- Skip anything that is already installed and up to date, so it is safe to run again.
- Print the versions that are now active when it finishes.
