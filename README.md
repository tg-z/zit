# `zit.vim` plugin

this vim plugin is a personal rework of [vim-zettel](https://github.com/michal-h21/vim-zettel). it uses the [Zettelkasten](https://zettelkasten.de/) method along with vimwiki.

## install

### using [vim-plug](https://github.com/junegunn/vim-plug)

    call plug#begin()
    Plug 'vimwiki/vimwiki'
    Plug 'junegunn/fzf'
    Plug 'junegunn/fzf.vim'
    Plug 'tg-z/zit'
    call plug#end()

the [silver searcher](https://github.com/ggreer/the_silver_searcher), ag, is used for searching in the notes by default. 
the used command can be changed by setting the `g:zit_fzf_command` variable.

# usage
