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
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/nodedotjs" width="48" height="48" alt="Node.js"><br>Node.js</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/pnpm" width="48" height="48" alt="pnpm"><br>pnpm</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/typescript" width="48" height="48" alt="TypeScript"><br>TypeScript</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/cloudflareworkers" width="48" height="48" alt="Wrangler"><br>Wrangler</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://raw.githubusercontent.com/microsoft/vscode/main/resources/linux/code.png" width="48" height="48" alt="VS Code"><br>VS Code</td>
    <td align="center" width="120"><img src="https://github.com/sublimehq.png" width="48" height="48" alt="Sublime Merge"><br>Sublime Merge</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/github/181717/white" width="48" height="48" alt="GitHub CLI"><br>GitHub CLI</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/postman" width="48" height="48" alt="Postman"><br>Postman</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/docker" width="48" height="48" alt="Docker"><br>Docker</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/kubernetes" width="48" height="48" alt="kubectl"><br>kubectl</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/helm" width="48" height="48" alt="Helm"><br>Helm</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/terraform" width="48" height="48" alt="Terraform"><br>Terraform</td>
    <td align="center" width="120"><b><code>terragrunt</code></b></td>
  </tr>
  <tr>
    <td align="center" width="120"><b><code>AWS CLI</code></b></td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/latex" width="48" height="48" alt="LaTeX"><br>LaTeX</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/flatpak" width="48" height="48" alt="Flatpak"><br>Flatpak</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/bambulab" width="48" height="48" alt="Bambu Studio"><br>Bambu Studio</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/todoist" width="48" height="48" alt="Todoist"><br>Todoist</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/claude" width="48" height="48" alt="Claude Code"><br>Claude Code</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/claude" width="48" height="48" alt="Claude"><br>Claude</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/freecad" width="48" height="48" alt="FreeCAD"><br>FreeCAD</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/1password" width="48" height="48" alt="1Password"><br>1Password</td>
  </tr>
  <tr>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/obsidian" width="48" height="48" alt="Obsidian"><br>Obsidian</td>
    <td align="center" width="120"><img src="https://cdn.simpleicons.org/raspberrypi" width="48" height="48" alt="Raspberry Pi Imager"><br>Raspberry Pi Imager</td>
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
- Install the latest Erlang, then the latest Elixir that works with it, then the latest Python and Node.js.
- Set those versions as the default ones for your user.
- Install pnpm, TypeScript and Cloudflare's Wrangler as global npm packages of that Node.js, or update them.
- Install VS Code from the Microsoft apt repository, or upgrade it if it is already installed.
- Install Sublime Merge from the Sublime HQ apt repository, or upgrade it if it is already installed.
- Install the [GitHub CLI](https://cli.github.com) (`gh`) from the GitHub apt repository, or upgrade it if it is already installed.
- Install [1Password](https://1password.com) and its CLI (`op`) from the 1Password apt repository (amd64 only), or upgrade them if already installed.
- Install `pdflatex` and the LaTeX packages needed to build `docs/devtools.tex` (TeX Live from the Ubuntu repositories), or upgrade them if already installed.
- Install Flatpak and the Flathub store if missing, then install Bambu Studio, Todoist, FreeCAD and Obsidian or update them.
- Install [Postman](https://www.postman.com) from the Snap Store, or refresh it if it is already installed.
- Install [Raspberry Pi Imager](https://www.raspberrypi.com/software/) from Raspberry Pi's own `.deb` on GitHub, after checking its checksum, or upgrade it when a newer release is out.
- Install [Claude Code](https://claude.com/claude-code) with its official installer, or update it if it is already installed that way (a copy installed some other way is left alone).
- Install the [Claude desktop app](https://claude.ai/download) from Anthropic's apt repository, or upgrade it if it is already installed.
- Install Docker Engine with Buildx and Compose from Docker's apt repository, or upgrade them, and add you to the `docker` group (takes effect at your next login).
- Install `kubectl` from the Kubernetes apt repository for the current stable minor release, moving to the next minor when one is out.
- Install [Helm](https://helm.sh) from the Helm apt repository and Terraform from the HashiCorp apt repository, or upgrade them.
- Install the latest [Terragrunt](https://terragrunt.gruntwork.io) release binary from GitHub into `~/.local/bin`, after checking its checksum.
- Install the [AWS CLI](https://aws.amazon.com/cli/) v2 with AWS's own installer, or update it.
- Leave alone any of the tools above (Docker, kubectl, Helm, Terraform, Terragrunt, AWS CLI, npm packages) that are already installed some other way.
- Skip anything that is already installed and up to date, so it is safe to run again.
- Print the versions that are now active when it finishes.
