## Install Neovim
```bash
sudo pacman -S neovim
nvim --version
```

## Install ripgrep
```bash
sudo pacman -S ripgrep

#Verify installation
rg --version
```

This is a dependency for telescope which is a plugin in neovim for searching files.

## Check git installation
```zsh
git --version
```


## Setting up folder structure
Create a directory in `.config` called nvim. This will be where all configurations will be saved.

```zsh
touch init.lua
mkdir lua
touch lua/keymaps.lua
touch lua/options.lua
```

This should result in the following folder strcutre:

├── init.lua
└── lua
    ├── keymaps.lua
    └── options.lua

## Initial Config
set leader
set relative line numbers

## Install plugin manager lazyvim


## Install theme
{ "catppuccin/nvim", name = "catppuccin", priority = 1000 }


## Install telescope

```
-- plugins/telescope.lua:
{
    'nvim-telescope/telescope.nvim', tag = '0.1.8',
      dependencies = { 'nvim-lua/plenary.nvim' }
    }
```

Next set key bindings for telescope



## Install Nvim tree

```lua
local keymap = vim.keymap -- for conciseness

    keymap.set("n", "<leader>ee", "<cmd>NvimTreeToggle<CR>", { desc = "Toggle file explorer" }) -- toggle file explorer
    keymap.set("n", "<leader>ef", "<cmd>NvimTreeFindFileToggle<CR>", { desc = "Toggle file explorer on current file" }) -- toggle file explorer on current file
    keymap.set("n", "<leader>ec", "<cmd>NvimTreeCollapse<CR>", { desc = "Collapse file explorer" }) -- collapse file explorer
    keymap.set("n", "<leader>er", "<cmd>NvimTreeRefresh<CR>", { desc = "Refresh file explorer" }) -- refresh file explorer

```