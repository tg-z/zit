<h1 align="center"><code>$ zit</code></h1>

<p align="center">
<a href="https://github.com/tg-z/zit/issues"><img alt="github issues" src="https://img.shields.io/github/issues/tg-z/zit?color=ff69b4"></a>
<a href="https://github.com/tg-z/zit/stargazers"><img alt="github stars" src="https://img.shields.io/github/stars/tg-z/zit?color=ff69b4"></a>
<a href="https://github.com/tg-z/zit/graphs/contributors" alt="contributors">
<img src="https://img.shields.io/github/contributors/tg-z/zit?color=ff69b4"/></a>
</p>

<p align="center">a small tool for managing your zettelkasten. 📓 </p>

<p align="center">
  <a href="#features">features</a> •
  <a href="#install">install</a> •
  <a href="#usage">usage</a> •
  <a href="#extra">extra</a><br>
</p>

# features

### git integration
`zit` uses `git` to sync zettelkasten files and autocommit changes to remote repository if configured.

### live markdown preview
`zit` uses `mlp` to preview markdown files before committing them to a remote repository.

## dependencies
- [fd](https://crates.io/crates/fd-find): fd is a simple, fast and user-friendly alternative to [find](https://www.gnu.org/software/findutils/).
- [fzf](https://github.com/junegunn/fzf): fzf is a general-purpose command-line fuzzy finder.
- [mlp](https://github.com/ms-jpq/markdown-live-preview): mlp shows a live web preview of markdown docs.
- [bat](https://github.com/sharkdp/bat): A cat(1) clone with wings.
- [ag](https://geoff.greer.fm/ag/): A code-searching tool similar to ack, but faster.
- [glow](https://github.com/charmbracelet/glow): Render markdown on the CLI, with pizzazz! 💅
- [ripgrep](https://github.com/BurntSushi/ripgrep): ripgrep recursively searches directories for a regex pattern while respecting your gitignore.

## install

```sh
# clone repo
git clone https://github.com/tg-z/zit
# cd into repo
cd zit
# create ~/bin directory if you haven't already
mkdir -p ~/bin
# add script to path
ln -s zit ~/bin/zit
```

## usage
```sh
       __ __
.-----|__|  |_
|-- __|  |   _|
|_____|__|____|

zit - a small tool for managing your zettelkasten.

Usage:
  zit <cmd> <options> args
Options:
  -i 	Copy zettel id after running command.
  -f 	Copy zettel location/path after running command.
  -h 	Display this help information.
  -V 	Display version information and exit.
Help:
  zit help
Home:
  https://github.com/tg-z/zit
Available commands:
  commands
  find
  help
  id
  index
  list
  new
  open
  preview
  show
  sync
  tag
```
```sh
# print help text
zit help

# list files (pretty)
zit list

# print available commands
zit commands

# search for pattern in files and show context
zit show 'unix'

# commit and push changed files to remote git repo
zit sync

# print files with text that match pattern
zit find 'gnu'
```
## extra
i use [vim-zettel](https://github.com/michal-h21/vim-zettel) in tandem with zit. it uses the [zettelkasten method](https://zettelkasten.de/) alongside [vimwiki](https://github.com/vimwiki/vimwiki).
