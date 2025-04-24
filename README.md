# (Personal) dotfiles

## Includes

* `.gitconfig`
  * Some nice configurations tipps based on this [blog posts](https://blog.gitbutler.com/git-tips-and-tricks/) by Scott Chacon, [@schacon](https://github.com/schacon)
  * Better diff with [delta](https://github.com/dandavison/delta) by Dan Davison, [@dandavison](https://github.com/dandavison)

## Setup

### Dependencies

#### Fedora/CentOS/RHEL

```bash
sudo dnf install git-delta
```

### Clone

```bash
if [ ! -d ~/git/cj ]; then
    mkdir -p ~/git/cj
    git clone https://github.com/cj/dotfiles ~/git/cj/dotfiles
fi
```

### Link

```bash
cd ~/git/cj/dotfiles
for file in .gitconfig*; do
    rm ~/$file
    ln -s ~/git/cj/dotfiles/$file ~/$file
done
ls -l ~/.gitconfig*
```
