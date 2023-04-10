202304101823
Status: 

# Bindings setup nvim

Hi!  nothing here new thats [Primeagen dot files](https://github.com/ThePrimeagen/init.lua), I followed his [youtube video](https://www.youtube.com/watch?v=w7i4amO_zaE) for the setup.


The plugins used are these:
- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- [Harpoon](https://github.com/ThePrimeagen/harpoon)
- [Lsp Zeero](https://github.com/VonHeikemen/lsp-zero.nvim)
- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [Undotree](https://github.com/mbbill/undotree)
- [Fugitive](https://github.com/tpope/vim-fugitive)

> The "leader" in this case is the space " " as you can see in the scripts.


# Installation 

1. Setup [Packer](https://github.com/wbthomason/packer.nvim)
2. Clone this repo under ~/.config/nvim.
```bash
 cd ~/.config/nvim
 git clone https://github.com/LobsterRavioli/my-nvim-setup
```
3. Open the dependencies list for Packer.
```bash
 nvim lua/my_config/packer.lua
```
4. Open nvim "shell" pressing ":" and type "PackSync".
5. You should ready to go.

# Keybinding Cheetsheet
## Telescope
| Mode | Column  | Description                                                                                                                      |
|------|---------|----------------------------------------------------------------------------------------------------------------------------------|
| Normal    | `<leader>-pf` | Calls the Vim built-in function 'find_files' to open a fuzzy search window.                                                       |
| Normal    | `Ctrl-p`     | Calls the Vim built-in function 'git_files' to open files from Git projects.                                                      |
| Normal    | `<leader>-ps` | Prompts the user for a search string and calls the Vim built-in function 'grep_string' to search for that string in the current directory and its subdirectories. |
| Normal    | `<leader>-vh` | Calls the Vim built-in function 'help_tags' to open the help file and list all available help tags.                               |


## Harpoon 

| Mode | Column   | Description                                                                                                                                 |
|------|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Normal    | `<leader>a` | Calls the Vim built-in function 'mark.add_file' to add a mark to the current file.                                                            |
| Normal    | `Ctrl-e`      | Calls the Obsidian built-in function 'ui.toggle_quick_menu' to toggle the quick switcher menu.                                                |
| Normal    | `Ctrl-h`      | Calls the Obsidian built-in function 'ui.nav_file(1)' to navigate to the previous file in the current pane.                                   |
| Normal    | `Ctrl-t`      | Calls the Obsidian built-in function 'ui.nav_file(2)' to navigate to the next file in the current pane.                                       |
| Normal    | `Ctrl-n`      | Calls the Obsidian built-in function 'ui.nav_file(3)' to navigate to the previous file in the opposite pane (if split).                       |
| Normal    | `Ctrl-s`      | Calls the Obsidian built-in function 'ui.nav_file(4)' to navigate to the next file in the opposite pane (if split).                           |

## Lsp Zeero

| Mode | Column            | Description                                                                                                   |
| ---  |-------------------|---------------------------------------------------------------------------------------------------------------|
| Normal| `Ctrl-p`           | Maps the key combination `Control + p` to the 'cmp' function 'select_prev_item' with the 'cmp_select' behavior. |
| Normal | `Ctrl-n`           | Maps the key combination `Control + n` to the 'cmp' function 'select_next_item' with the 'cmp_select' behavior. |
| Normal | `Ctrl-y `          | Maps the key combination `Control + y` to the 'cmp' function 'confirm' with a table argument.                   |
| Normal | `Ctrl-Space`       | Maps the key combination `Control + Space` to the 'cmp' function 'complete'.                                  |
| Normal    | `gd`                | Calls the Vim LSP function 'buf.definition' to go to the definition of the symbol under the cursor.                    |
| Normal    | `K `                | Calls the Vim LSP function 'buf.hover' to show hover information for the symbol under the cursor.                       |
| Normal    | `leader-vws`        | Calls the Vim LSP function 'buf.workspace_symbol' to list symbols across the entire workspace.                          |
| Normal    | `leader-vd`         | Calls the Vim diagnostic function 'open_float' to open a floating window containing the current line's diagnostics.   |
| Normal    | `[d`                | Calls the Vim diagnostic function 'goto_next' to go to the next diagnostic in the current buffer.                       |
| Normal    | `]d`                | Calls the Vim diagnostic function 'goto_prev' to go to the previous diagnostic in the current buffer.                   |
| Normal    | `leader-vca `       | Calls the Vim LSP function 'buf.code_action' to list and apply available code actions for the current cursor position. |
| Normal    | `leader-vrr`        | Calls the Vim LSP function 'buf.references' to list all references to the symbol under the cursor.                       |
| Normal    | `leader-vrn`        | Calls the Vim LSP function 'buf.rename' to rename the symbol under the cursor.                                           |
| Insert    | `Ctrl-h`               | Calls the Vim LSP function 'buf.signature_help' to show signature help for the symbol under the cursor.                 |



## Vim Keymaps

### Basic Mappings

| Mode | Mapping | Description |
| --- | --- | --- |
| Normal | `<leader>pv` | Execute `:Ex` ( Vist della folder corrente) |
| Visual | `J` | Move the current selection down one line |
| Visual | `K` | Move the current selection up one line |
| Normal | `J` | Join the current line with the one below it |
| Normal | `<C-d>` | Scroll down |
| Normal | `<C-u>` | Scroll up |
| Normal | `n` | Move to the next search result and center the screen |
| Normal | `N` | Move to the previous search result and center the screen |
| Normal | `<leader>vwm` | Start a [vim-with-me](https://github.com/davidgranstrom/vim-with-me) session |
| Normal | `<leader>svwm` | Stop the current [vim-with-me](https://github.com/davidgranstrom/vim-with-me) session |

### Advanced Mappings

| Mode | Mapping | Description |
| --- | --- | --- |
| Visual | `<leader>p` | Cut the selected text and paste it below the current line |
| Normal/Visual | `<leader>y` | Copy the selected text to the clipboard |
| Normal | `<leader>Y` | Copy the current line to the clipboard |
| Normal/Visual | `<leader>d` | Cut the selected text |
| Insert | `<C-c>` | Exit insert mode |
| Normal | `Q` | Do nothing (noop) |
| Normal | `<C-f>` | Open a new Tmux window and run [tmux-sessionizer](https://github.com/jbnicolai/tmux-sessionizer) |
| Normal | `<leader>f` | Format the current buffer using LSP |
| Normal | `<C-k>` | Move to the next quickfix item and center the screen |
| Normal | `<C-j>` | Move to the previous quickfix item and center the screen |
| Normal | `<leader>k` | Move to the next location list item and center the screen |
| Normal | `<leader>j` | Move to the previous location list item and center the screen |
| Normal | `<leader>s` | Search and replace text in the current buffer |
| Normal | `<leader>x` | Make the current file executable |

### Packer Mappings

| Mode | Mapping | Description |
| --- | --- | --- |
| Normal | `<leader>vpp` | Edit the Packer config file |
| Normal | `<leader>mr` | Run a command from [CellularAutomaton](https://github.com/CellularAutomaton) |

### Miscellaneous Mappings

| Mode | Mapping | Description |
| --- | --- | --- |
| Normal | `<leader><leader>` | Reload the current file |
  
