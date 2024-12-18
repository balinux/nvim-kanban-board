# nvim-kanban-board

A simple Kanban board plugin for Neovim to manage tasks in a TODO.md file.

## Features

- Manage tasks in TODO, InProgress, and Done columns.
- Save and load tasks from a `TODO.md` file.
- Dynamic filepath support for local project or Neovim configuration.

## Installation

You cean install this plugin using any Neovim plugin manager. For example:

### With [Packer](https://github.com/wbthomason/packer.nvim)

```lua
use {
  'username/nvim-kanban-board',
  config = function()
    require('kanban')
  end
}
```

### With [Lazy.vim](https://github.com/folke/lazy.nvim)

```lua
require('lazy').setup {
  'username/nvim-kanban-board',
  config = function()
    require('kanban')
  end
}
```

## Usage

### Open the Kanban Board

```bash
:KanbanOpen
```

### Add an Item

```bash
:KanbanAdd <column> <item>
```

example

```bash
:KanbanAdd TODO Implement feature
```

### Move an Item

move an item between columns

```bash
 :KanbanMove <from_column> <to_column> <index>
```

example

```bash
:KanbanMove TODO InProgress 1
```

### Save

Save current kanban board

```bash
:KanbanSave
```

### load

Load the kanban board from TODO.md file

```bash
:KanbanLoad
```
