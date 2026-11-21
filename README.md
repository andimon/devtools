# devtools

Purpose: keeping my devtools consistent across Ubuntu machines.

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
- Install Flatpak and the Flathub store if missing, then install Bambu Studio or update it.
- Install [Claude Code](https://claude.com/claude-code) with its official installer, or update it if it is already installed that way (a copy installed some other way is left alone).
- Skip anything that is already installed and up to date, so it is safe to run again.
- Print the versions that are now active when it finishes.
