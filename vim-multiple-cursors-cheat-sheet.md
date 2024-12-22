# Vim Multiple Cursors Cheat Sheet

## Setup

1. Install the `vim-multiple-cursors` plugin using your plugin manager (e.g., `vim-plug`, `Vundle`).

## Basic Usage

- **Place the cursor** on the word you want to select.
- **Press `Ctrl + n`** to select that word.  
  (This will add a cursor to the next instance of that word in the document.)
- **Repeat `Ctrl + n`** to select more instances of the word.
- **Press `Ctrl + p`** to remove the previous cursor (de-select the last added instance).
- **Edit all selected instances** simultaneously. Any edits will be applied to all selected occurrences.

## Custom Keybindings

You can change the default keybindings for multiple cursors. Add the following to your `.vimrc`:

```vim
let g:multi_cursor_start_word_key = '<C-d>'  " Custom key to start selecting
let g:multi_cursor_select_next_key = '<C-n>'  " Custom key to select the next occurrence
let g:multi_cursor_quit_key = '<C-x>'  " Custom key to quit selection
