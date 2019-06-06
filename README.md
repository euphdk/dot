# README dotfiles

```bash
git clone --bare git@github.com:euphdk/dot.git $HOME/.dot
alias config='/usr/bin/git --git-dir=$HOME/.dot/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
```

<https://www.atlassian.com/git/tutorials/dotfiles>
