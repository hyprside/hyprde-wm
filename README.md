<div align = center>



<br><br>

**hyprde-wm** is a heavily modified fork of **Hyprland**, designed to be the
window management and compositing core of **HyprDE / Hyprside**.

## This is **not** a general-purpose Wayland compositor.
It is an **integrated system component**, tightly coupled with the Hyprside stack.

**This repository is intended for system developers, not end users.**


<br>

</div>

# What is hyprde-wm?

**hyprde-wm** is a fork of Hyprland adapted to act as:

- The compositor core for **HyprDE**
- A rendering client of [**Shift**](https://github.com/hyprside/shift), Hyprside’s graphical kernel and session manager
- A tightly integrated subsystem rather than a standalone WM

Unlike upstream Hyprland, this fork **does not aim to be modular, portable, or user-configurable via dotfiles**.

Instead, it prioritizes:

- Deterministic behavior
- Tight coupling with the shell
- Centralized configuration
- Predictable performance characteristics


# Key Differences from Hyprland

This fork intentionally diverges from upstream Hyprland in several ways:

### Architectural
- Designed to run **under Shift**, not directly on DRM/KMS
- Not designed to run standalone on arbitrary Linux setups

### Configuration
- No user-facing dotfile configuration
- Runtime behavior is controlled by the shell and system services
- Hyprlang dotfiles are completely deprecated and removed in favor of the **HyprRegistry**
### Scope
- No focus on plugin ecosystems
- No built-in plugin manager
- Features are added based on **Hyprside's requirements**, not general compositor use

### Stability Model
- Changes may break compatibility with upstream Hyprland
- API and behavior may change without notice
- No guarantee of upstream feature parity


# What stays from Hyprland

This fork still inherits much of what makes Hyprland great:

- Modern Wayland protocol support
- High-performance rendering pipeline
- Animation system and effects
- Tiling / floating / fullscreen window management
- Clean and readable C++ codebase

Hyprland serves as the **foundation**, not the final product.


# Intended Usage

This repository is meant to be used **only** as part of:

- **HyprDE**
- **Hyprside OS**

If you are looking for:
- A configurable Wayland compositor
- A desktop you can install on any distro

➡️ **You want upstream Hyprland, not this fork.**



# Credits & Acknowledgements


Special thanks to:

- **Hyprland** — original compositor and architecture. Making a wayland compositor from scratch is a real pain and Hyprland allowed me to headstart the development of the compositor.

All original Hyprland credits apply to inherited code.




# License

This project is licensed under the **same license as Hyprland**.
See the [LICENSE](LICENSE) file for details.
