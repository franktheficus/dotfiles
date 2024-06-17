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

### Multiple SSH keys for Git host [link](https://gist.github.com/alejandro-martin/aabe88cf15871121e076f66b65306610)

1. Create a SSH key with any name you choose.
2. Open and edit ~/.ssh/config file

```bash
# github acc 1
Host acc1.github.com
  HostName github.com
  PreferredAuthentication publickey
  IdentityFile ~/.ssh/id_acc1

# github acc2
Host acc2.github.com
  HostName github.com
  PreferredAuthentication publickey
  IdentityFile ~/.ssh/id_acc2

# gitlab acc
Host gitlab.com
  HostName gitlab.com
  PreferredAuthentication publickey
  IdentityFile ~/.ssh/id_gitlab
```

When using multiple accounts from the same server don't forget to use custom host when cloning.
`git clone git@acc1.github.com:USER/REPO.git`

3. Add global and local git configs to have correct author for commits.

```bash
git config --local user.name "Acc 1"
git config --local user.email "acc1@email.co"
```
