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
  zit <options> <cmd> args
Options:
  -i 	Copy zettel id to clipboard after running id.
  -f 	Copy zettel location/path after running command.
  -h 	Display this help information.
  -V 	Display version information.
Help:
  zit help
Home:
  https://github.com/tg-z/zit
Available commands:
  commands   Lists available subcommands.
  find       Find a file by name.
  help       Display help information.
  id         Outputs 14 character zettel id.
  index      Create a markdown index of files.
  list       With no argument, list all notes. Otherwise list notes containing any of the given patterns.
  new        Create a new note with the given title.
  open       Open a note in default editor.
  preview    Preview notes as HTML.
  show       Search file contents and show results in context.
  sync       Synchronize $ZETTEL_DIR with the git remote, if configured.
  tag        Search note tags.
```
__examples__:
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

# print zettel id from filename
zit id 20210101003310-workstation
20210101003310 # printed zettel id

# copy zettel id to clipboard
zit -i id 20210101003310-workstation
20210101003310 # this is copied to clipboard
```

## extra
i use [vim-zettel](https://github.com/michal-h21/vim-zettel) in tandem with zit. it uses the [zettelkasten method](https://zettelkasten.de/) alongside [vimwiki](https://github.com/vimwiki/vimwiki).
