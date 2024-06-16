# Dotfiles

## Instalation
```bash
# Install gnu stow (macOS)
brew install stow
# or linux
dnf install stow
```

## Commands

```bash
# Stow specific config with simulation, remove -n flag to commit
stow -nvSt ~ folder_name

# Check that alias/link was made, e.g. nvim
ls -la | grep nvim

```

## Extras

Don't forget to install TPM [link](https://github.com/tmux-plugins/tpm)
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

 
