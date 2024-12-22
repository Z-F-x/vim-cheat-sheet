# Vim Navigation Commands

- **Go to the end of file**: `Shift + G`
- **Go to top of file**: `Double g`
- **Move the cursor half a page down**: `Ctrl + D`
- **Move the cursor half a page up**: `Ctrl + U`


# Additional Vim Commands

## Navigation:
- `0`: Go to the beginning of the line.
- `^`: Go to the first non-blank character of the line.
- `$`: Go to the end of the line.
- `Ctrl + f`: Scroll forward by one page.
- `Ctrl + b`: Scroll backward by one page.
- `Ctrl + e`: Scroll the screen down one line without moving the cursor.
- `Ctrl + y`: Scroll the screen up one line without moving the cursor.

## Text Manipulation:
- `x`: Delete the character under the cursor.
- `s`: Substitute the character under the cursor (replace with text in Insert Mode).
- `D`: Delete from the cursor position to the end of the line.
- `C`: Delete from the cursor to the end of the line and enter Insert Mode.
- `S`: Replace the entire line with new text (enter Insert Mode).
- `>>`: Indent the current line.
- `<<`: Un-indent the current line.

## Marks and Jumps:
- `m[a-z]`: Set a mark at the cursor position.
- `'a`: Jump to the beginning of the line of mark 'a'.
- `` `a ``: Jump to the exact position of mark 'a'.
- `Ctrl + o`: Jump to the previous location.
- `Ctrl + i`: Jump to the next location.

## Searching:
- `*`: Search for the word under the cursor (forward).
- `#`: Search for the word under the cursor (backward).
- `n`: Move to the next match of the search.
- `N`: Move to the previous match of the search.
- `:noh`: Clear the search highlight.

## Buffers and Windows:
- `:e filename`: Open a file in the current window.
- `:split` or `:sp`: Split the window horizontally.
- `:vsplit` or `:vsp`: Split the window vertically.
- `Ctrl + w h/j/k/l`: Move between splits/windows.
- `:bnext`: Switch to the next buffer.
- `:bprev`: Switch to the previous buffer.
- `:bd`: Delete (close) the current buffer.
- `:ls`: List all buffers.

## Undo and Redo:
- `u`: Undo the last change.
- `Ctrl + r`: Redo the undone change.

---

# Time-Saving Shortcuts

## Quick Saving:
- `:w`: Save the file.
- `:w!`: Save a file without confirmation (overwriting any read-only file).
- `:wa`: Save all open files.
- `:sav filename`: Save the file with a new name.

## Exiting Vim:
- `ZZ`: Save and exit (same as `:wq`).
- `ZQ`: Quit without saving (same as `:q!`).
- `:qa`: Quit all files.

---

# Configuration and Customization Tips

## Line Numbers:
- `:set number`: Display line numbers.
- `:set relativenumber`: Display relative line numbers.
- `:set nu!`: Toggle line numbers.

## Searching and Replacing:
- `:s/old/new/g`: Replace all instances of "old" with "new" in the current line.
- `:%s/old/new/g`: Replace all instances of "old" with "new" in the entire file.
- `:s/old/new/gc`: Replace with confirmation (asks for each replacement).

## Syntax Highlighting:
- `:syntax enable`: Enable syntax highlighting.
- `:syntax off`: Disable syntax highlighting.

## Show Whitespace Characters:
- `:set list`: Show hidden characters like spaces and tabs.
- `:set nolist`: Hide those characters.

---

# Plugins and Extensions
If you're using plugins, you could briefly mention useful ones such as:
- **NERDTree** for file navigation.
- **fzf** for fuzzy searching.
- **coc.nvim** for intellisense and autocompletion.
- **vim-airline** for a better statusline.
- **vim-fugitive** for Git integration.
- **vim-surround** for managing surrounding characters like parentheses, quotes, etc.

---

# Advanced Tips

## Using Registers:
- `"a` (e.g., `"ayy`): Yank (copy) the current line to register `a`.
- `"aP`: Paste the content from register `a`.
- `:reg`: View the contents of all registers.

## Macros:
- `q[a-z]`: Start recording a macro to register `a-z`.
- `q`: Stop recording.
- `@[a-z]`: Replay a macro from register `a-z`.
- `@@`: Replay the last macro.

---

# Quick Reference for Modes

| Mode             | How to Enter            | Common Commands                    |
|------------------|-------------------------|-------------------------------------|
| **Normal Mode**   | `Esc`                   | - Move cursor: h, j, k, l          |
|                  |                         | - Delete: d, dw, dd, d$            |
|                  |                         | - Copy: y, yy, yw                  |
|                  |                         | - Paste: p                         |
| **Insert Mode**   | `i`, `I`, `a`, `A`, `o`, `O` | - Type text                        |
|                  |                         | - Move cursor: Ctrl + h (delete), Ctrl + w (delete word) |
| **Visual Mode**   | `v`, `V`, `Ctrl + v`     | - Select: v, V, Ctrl + v            |
|                  |                         | - Delete: d                         |
|                  |                         | - Yank: y                          |
|                  |                         | - Change: c                         |
| **Command-Line Mode** | `:`                  | - Save: `:w`                       |
|                  |                         | - Quit: `:q`, `:wq`, `:q!`          |
| **Replace Mode**  | `R`, `r`                 | - Replace: `R`                      |

---

# Show File Information
- `:set filetype`: Show the current file type.
- `:echo &filetype`: Echo the file type.


# Vim Modes and Commands Table

| **Mode**             | **Purpose**                                     | **How to Enter**                                                                 | **How to Exit**                                        | **Common Commands**                                                                                                  |
|----------------------|-------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Normal Mode**       | Default mode for navigation and editing         | Open Vim or press `Esc` from any other mode                                      | Press `Esc` from any other mode                       | - Move cursor: `h`, `j`, `k`, `l`<br> - Delete: `d`, `dw`, `dd`, `d$`<br> - Copy: `y`, `yy`, `yw`<br> - Paste: `p`     |
| **Insert Mode**       | For typing and inserting text                   | Press `i`, `I`, `a`, `A`, `o`, or `O` in Normal Mode                           | Press `Esc`                                           | - Type text<br> - Move cursor: `Ctrl + h` (delete), `Ctrl + w` (delete word)<br> - Tab for indentation                |
| **Visual Mode**       | For selecting text                              | Press `v` (Character-wise), `V` (Line-wise), or `Ctrl + v` (Block-wise) in Normal Mode | Press `Esc`                                           | - Select: `v`, `V`, `Ctrl + v`<br> - Delete: `d`<br> - Yank: `y`<br> - Change: `c`<br> - Paste: `p`                  |
| **Command-Line Mode** | For executing commands (e.g., save, quit)       | Press `:` in Normal Mode                                                         | Press `Esc`                                           | - Save: `:w`<br> - Quit: `:q`<br> - Search: `:/pattern`<br> - Replace: `:%s/old/new/g`                                |
| **Replace Mode**      | For replacing text under the cursor             | Press `R` in Normal Mode (or `r` followed by a character)                         | Press `Esc`                                           | - Replace characters: `R`<br> - Replace one character: `r` (followed by the character to replace with)                |
| **Select Mode**       | For selecting text for copy or cut              | Press `g`, then `v` (in some versions like GVim)                                  | Press `Esc`                                           | - Select: `v`, `V`, `Ctrl + v`<br> - Copy: `y`<br> - Cut: `d`<br> - Paste: `p`                                       |

## Details of Each Mode:

### 1. **Normal Mode** (Command Mode)
- **Purpose**: Used for navigating the file, manipulating text, and issuing commands.
- **How to Enter**: By default when you open Vim, or by pressing `Esc` from any other mode.
- **How to Exit**: Press `Esc` from any mode to return to Normal Mode.
- **Common Commands**:
  - Navigation: `h`, `j`, `k`, `l` (left, down, up, right), `w` (next word), `b` (previous word), `gg` (go to the start of the file), `G` (go to the end of the file).
  - Deleting: `d`, `dw` (delete word), `dd` (delete line), `d$` (delete to the end of the line).
  - Copying: `y`, `yy` (copy line), `yw` (copy word), `y$` (copy to the end of the line).
  - Pasting: `p` (paste after cursor), `P` (paste before cursor).
  - Undo/Redo: `u` (undo), `Ctrl-r` (redo).

### 2. **Insert Mode**
- **Purpose**: Used for typing new text into the file.
- **How to Enter**: Press `i` (insert at the cursor), `I` (insert at the beginning of the line), `a` (append after the cursor), `A` (append at the end of the line), `o` (open a new line below), or `O` (open a new line above).
- **How to Exit**: Press `Esc` to return to Normal Mode.
- **Common Commands**:
  - Typing: Just type text.
  - Navigation: `Ctrl+h` (delete previous character), `Ctrl+w` (delete previous word), `Tab` (indent), `Backspace` (delete).

### 3. **Visual Mode**
- **Purpose**: Used for selecting text to copy, delete, or modify.
- **How to Enter**: Press `v` (character-wise selection), `V` (line-wise selection), or `Ctrl+v` (block-wise selection) in Normal Mode.
- **How to Exit**: Press `Esc` to return to Normal Mode.
- **Common Commands**:
  - Select: `v` (select characters), `V` (select lines), `Ctrl+v` (select blocks).
  - Copy: `y` (yank/copy).
  - Delete: `d` (delete selected).
  - Change: `c` (delete selected and enter Insert Mode).
  - Paste: `p` (paste after selection).

### 4. **Command-Line Mode**
- **Purpose**: Used for executing Vim commands, such as saving, quitting, searching, etc.
- **How to Enter**: Press `:` in Normal Mode.
- **How to Exit**: Press `Esc` to return to Normal Mode.
- **Common Commands**:
  - Save: `:w` (write/save).
  - Quit: `:q` (quit), `:wq` (write and quit), `:q!` (force quit without saving).
  - Search: `:/pattern` (search for a pattern).
  - Replace: `:%s/old/new/g` (replace text).

### 5. **Replace Mode**
- **Purpose**: Used for replacing existing text under the cursor.
- **How to Enter**: Press `R` in Normal Mode to replace multiple characters, or `r` followed by a character to replace the current character.
- **How to Exit**: Press `Esc` to return to Normal Mode.
- **Common Commands**:
  - Replace: `R` (replace multiple characters), `r` followed by a character (replace just one character).

### 6. **Select Mode**
- **Purpose**: Similar to Visual Mode, but designed for selection and operations like copying or cutting.
- **How to Enter**: Press `g`, then `v` (in some versions like GVim).
- **How to Exit**: Press `Esc` to return to Normal Mode.
- **Common Commands**:
  - Select: `v`, `V`, `Ctrl+v` (same as Visual Mode).
  - Copy: `y` (yank/copy).
  - Cut: `d` (delete/cut).
  - Paste: `p` (paste).

