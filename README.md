# nixos-multi-machine-starter

This repository is intended to be a sane, batteries-included starter template
for running a LunarVim-powered NixOS development environment on both WSL and on
Hetzner Cloud.

This repository is the result of a live refactoring session where I
demonstrated how to merge two NixOS configurations for separate machines and
machine types into a single flake.

* [nixos-wsl-starter](https://github.com/lgug2z/nixos-wsl-starter)
* [nixos-hetzner-cloud-starter](https://github.com/lgug2z/nixos-hetzner-cloud-starter)

If you found this starter template useful, please consider
[sponsoring](https://github.com/sponsors/LGUG2Z) and [subscribing to my YouTube
channel](https://www.youtube.com/channel/UCeai3-do-9O4MNy9_xjO6mg?sub_confirmation=1).

## What Is Included

This starter is a lightly-opinionated take on a productive terminal-driven
development environment based on my own preferences. However, it is trivial to
customize to your liking both by removing and adding tools that you prefer.

* The default editor is initially `lvim`
* `win32yank` is used to ensure perfect bi-directional copying and pasting to
  and from Windows GUI applications and LunarVim running in WSL
* The default shell is `zsh`
* Native `docker` (ie. Linux, not Windows) is enabled by default
* The prompt is [Starship](https://starship.rs/)
* [`fzf`](https://github.com/junegunn/fzf),
  [`lsd`](https://github.com/lsd-rs/lsd),
  [`zoxide`](https://github.com/ajeetdsouza/zoxide), and
  [`broot`](https://github.com/Canop/broot) are integrated into `zsh` by
  default
    * These can all be disabled easily by setting `enable = false` in
      [home.nix](home.nix), or just removing the lines all together
* [`direnv`](https://github.com/direnv/direnv) is integrated into `zsh` by
  default
* `git` config is generated in [home.nix](home.nix) with options provided to
  enable private HTTPS clones with secret tokens
* `zsh` config is generated in [home.nix](home.nix) and includes git aliases,
  useful WSL aliases, and
  [sensible`$WORDCHARS`](https://lgug2z.com/articles/sensible-wordchars-for-most-developers/)

## Quickstart

[![Watch the walkthrough video](https://img.youtube.com/vi/LzRi9rPV2p4/hqdefault.jpg)](https://www.youtube.com/watch?v=LzRi9rPV2p4)

You should follow the quickstart steps from either
[nixos-wsl-starter](https://github.com/lgug2z/nixos-wsl-starter) or
[nixos-hetzner-cloud-starter](https://github.com/lgug2z/nixos-hetzner-cloud-starter)
depending on if you are targeting the WSL VM configuration or the Hetzner Cloud
VM configuration.
