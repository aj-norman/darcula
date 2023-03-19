## Darcula

![darcula](./img/full_screen.png)

:smiling_imp: A [Vim](https://www.vim.org/)/[Neovim](https://neovim.io/) color scheme reproduction of the official [JetBrains](https://www.jetbrains.com/) IDE Darcula theme. Forked from doums/darcula.

### install
Using `wbthomason/packer.nvim`, Copy the following snippet to your configuation files (i.e. `plugins.lua`)

```lua
use({
  'aj-norman/darcula',
  config = function ()
      vim.cmd('colorscheme darcula')
  end
})
```

Adding the function will set NVIM to use the darcula colourscheme by default

**tree-sitter** support

[treesitter](https://github.com/nvim-treesitter/nvim-treesitter)

### support
- Truecolor
- 256 color
- [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- nvim [LSP](https://neovim.io/doc/user/lsp.html)

### VimScript API

#### darcula#palette
the colors palette of Darcula

#### darcula#Hi
helper function to create/modify highlight group

#### example:
```
call darcula#Hi('rustLifetime', darcula#palette.macroName, darcula#palette.bg, 'italic')
call darcula#Hi('Comment', [ '#eeeeee', 255 ], darcula#palette.null, 'italic')
call darcula#Hi('BlackFg', [ '#000000', 16 ])
```

### helper groups
Darcula provides some helper groups.\
You can use them with `hi link`.

[GitGutter](https://github.com/airblade/vim-gitgutter)
```
hi! link GitGutterAdd GitAddStripe
hi! link GitGutterChange GitChangeStripe
hi! link GitGutterDelete GitDeleteStripe
let g:gitgutter_sign_removed = '▶'
```

[Coc](https://github.com/neoclide/coc.nvim)
```
hi! link CocErrorSign ErrorSign
hi! link CocWarningSign WarningSign
hi! link CocInfoSign InfoSign
hi! link CocHintSign HintSign
hi! link CocErrorFloat Pmenu
hi! link CocWarningFloat Pmenu
hi! link CocInfoFloat Pmenu
hi! link CocHintFloat Pmenu
hi! link CocHighlightText IdentifierUnderCaret
hi! link CocHighlightRead IdentifierUnderCaret
hi! link CocHighlightWrite IdentifierUnderCaretWrite
hi! link CocErrorHighlight CodeError
hi! link CocWarningHighlight CodeWarning
hi! link CocInfoHighlight CodeInfo
hi! link CocHintHighlight CodeHint
```

[ALE](https://github.com/dense-analysis/ale)
```
hi! link ALEError Error
hi! link ALEWarning CodeWarning
hi! link ALEInfo CodeInfo
hi! link ALEErrorSign ErrorSign
hi! link ALEWarningSign WarningSign
hi! link ALEInfoSign InfoSign
```

### credits
[JetBrains](https://www.jetbrains.com/) for the original and awsome Darcula color scheme!

### license
Mozilla Public License 2.0
