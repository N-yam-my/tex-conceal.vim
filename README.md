# tex-conceal.vim

A vim plugin gives some sophistcated additions of the Conceal feature for LaTeX.

### Without conceal
<img src="https://github.com/KeitaNakamura/tex-conceal.vim/blob/master/normal.png" width="800">

### With conceal
<img src="https://github.com/KeitaNakamura/tex-conceal.vim/blob/master/conceal.png" width="800">

### With conceal and this plugin
<img src="https://github.com/KeitaNakamura/tex-conceal.vim/blob/master/conceal_plugin.png" width="800">

### Output
<img src="https://github.com/KeitaNakamura/tex-conceal.vim/blob/master/output.png" width="800">

## Installation

```vim
Plugin 'N-yam-my/tex-conceal.vim'                 " for Vundle
Plug   'N-yam-my/tex-conceal.vim', {'for': 'tex'} " for VimPlug
```

### For [vimtex](https://github.com/lervag/vimtex) user

[vimtex](https://github.com/lervag/vimtex) uses its own conceal feature from v2.
That breaks this plugin for now.
So when you install this plugin, you should set `g:vimtex_syntax_conceal` to 0 in order to disable that.

```vimrv
let g:vimtex_syntax_conceal
```

## Options

### Super/sub-scrips

To avoid having inscrutable utf-8 glyphs appear, set `g:tex_superscripts` and `g:tex_subscripts`:

```vim
let g:tex_superscripts= "[0-9a-zA-W.,:;+-<>/()=]"
let g:tex_subscripts= "[0-9aehijklmnoprstuvx,+-/().]"
```

See `:h tex-conceal` in more detail.

### Fraction

To conceal fraction (½⅓⅔¼⅕⅖⅗⅘⅙⅚⅛⅜⅝⅞)

```vim
let g:tex_conceal_frac=1
```

## Recommended settings

```vim
set conceallevel=2
let g:tex_conceal="abdgm"
```
