# tmux Configuration Setup

## Overview

This tmux configuration is designed to be managed within your `~/.config` directory following the [XDG Base Directory Specification](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html).

---

## Installation Steps

1. **Clone this repository into your `~/.config` directory**

   ```
   cd ~/.config
   git clone <your-tmux-config-repo> tmux
   ```

2. Add the following lines to your shell configuration (`~/.bashrc`, `~/.zshrc`, etc.)
    ```
    export XDG_CONFIG_HOME="$HOME/.config"
    [ -n "$TMUX" ] || tmux set-environment -g XDG_CONFIG_HOME "$XDG_CONFIG_HOME"
    ```

3. Create the plugins directory
    ```
    mkdir -p ~/.config/tmux/plugins
    ```

4. Clone the tmux plugin manager (TPM)
    ```
    git clone https://github.com/tmux-plugins/tpm ~/.config/tmux/plugins/tpm
    ```

## Usage
1. Inside tmux run:
    ```
    tmux source-file ~/.config/tmux/tmux.conf
    ```

2. Install plugins via TPM
    ```
    Prefix + I
    ```

