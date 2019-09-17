# README dotfiles

```bash
# Prepare for powerline-shell
sudo apt-get install fonts-powerline
sudo pip3 install powerline-shell

# Clone the repository
git clone --bare git@github.com:euphdk/dot.git $HOME/.dot

# Temp create alias - will also be in .bash_aliases
alias config='/usr/bin/git --git-dir=$HOME/.dot/ --work-tree=$HOME'

# Move existing files out of place
mkdir -p .config-backup && \
config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | \
xargs -I{} mv {} .config-backup/{}

# Checkout and don't show untracked files when running config status
config checkout
config config --local status.showUntrackedFiles no

# Install vscode extensions
fix-vscode-extensions.sh
```

```bash
config add README.md
config commit -m "README"
config push
# or first time
config push --set-upstream origin master
```


<https://www.atlassian.com/git/tutorials/dotfiles>
