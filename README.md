# `$ zit`

a commandline tool for knowledge management using the zettelkasten method.

## install

dependencies:
- [fd](https://crates.io/crates/fd-find): fd is a simple, fast and user-friendly alternative to [find](https://www.gnu.org/software/findutils/).
- [fzf](https://github.com/junegunn/fzf): fzf is a general-purpose command-line fuzzy finder.
- [mlp](https://github.com/ms-jpq/markdown-live-preview): mlp shows a live web preview of markdown docs
- [bat](https://github.com/sharkdp/bat): A cat(1) clone with wings.
- [bask](https://github.com/xwmx/bask): A runner and framework for command-centric Bash scripts.

```sh
# get bask
# install using curl
curl -L https://raw.github.com/xwmx/bask/master/bask \
  -o ~/bin/bask && chmod +x ~/bin/bask 
# clone repo
git clone https://github.com/tg-z/zit
# cd into repo
cd zit
# add script to path
ln -s zit ~/bin/zit
```

## usage

i use [vim-zettel](https://github.com/michal-h21/vim-zettel) in tandem with zit. it uses the [zettelkasten](https://zettelkasten.de/) method alongside [vimwiki](https://github.com/vimwiki/vimwiki).


