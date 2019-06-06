# README dotfiles

```bash
sudo apt-get install fonts-powerline
sudo pip3 install powerline-shell
git clone --bare git@github.com:euphdk/dot.git $HOME/.dot
alias config='/usr/bin/git --git-dir=$HOME/.dot/ --work-tree=$HOME'
config checkout
config config --local status.showUntrackedFiles no
```

```bash
config add README.md
config commit -m "README"
config push
# or first time
config push --set-upstream origin master
```


<https://www.atlassian.com/git/tutorials/dotfiles>
