# (Personal) dotfiles

## Setup

```bash
if [ ! -d ~/git/jerolimov ]; then
    mkdir -p ~/git/jerolimov
    git clone https://github.com/jerolimov/dotfiles ~/git/jerolimov/dotfiles
fi
```

### Manually link files

```bash
cd ~/git/jerolimov/dotfiles
for file in .gitconfig*; do
    rm ~/$file
    ln -s ~/git/jerolimov/dotfiles/$file ~/$file
done
ls -l ~/.gitconfig*
```

<!--
### Fedora

```
sudo dnf install stow
```
-->
