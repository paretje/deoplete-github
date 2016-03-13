# Deoplete Github

## Dependencies

I've tried not to replicate existing behaviour from already great plugins:

- [deoplete][]
- [fugitive][]
- [rhubarb][]

## Install

Install with your favourite vim plugin manager:

```vim
Plug 'SevereOverfl0w/deoplete-github'
```

Add it as a deoplete source:

```vim
let g:deoplete#sources = {}
let g:deoplete#sources.gitcommit=['github']
```

Deoplete also needs a little configuration:

```vim
let g:deoplete#keyword_patterns = {}
let g:deoplete#keyword_patterns.gitcommit = '.+'

call deoplete#util#set_pattern(
  \ g:deoplete#omni#input_patterns,
  \ 'gitcommit', [g:deoplete#keyword_patterns.gitcommit])

```

# Usage

In your git commit message, git "#" and you'll get issue numbers with their
titles beside them, and the issue body in the preview window.

[fugitive]: https://github.com/tpope/vim-fugitive
[rhubarb]: https://github.com/tpope/vim-rhubarb
[deoplete]: https://github.com/Shougo/deoplete.nvim
