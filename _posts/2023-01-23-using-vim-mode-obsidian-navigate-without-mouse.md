---
date: 2023-01-23
layout: post
title: "Using VIM mode in Obsidian to navigate without mouse"
---

I felt the need to completely navigate text files with both hands on the keyboard. I came across the Vim way and saw Obsidian has native support for it! 🤯

It has a really steep learning curve. But, I am all in for experiments.

This is my attempt to simplify Vim for Obsidian. I've broken up the commands in phases and ignored (existing) commands I am unlikely to use for note taking/outlining.

- Phase 1: Moving the cursor
	- `h` / `l` - left and right
		- `e` / `ge` - jump to next/previous word
		- `0` / `$` - jump to start/end of line
	- `j` and `k` - up and down
- Phase 2: Editing text
	- `a` - start insert mode (append)
		- `I` / `A` - start insert mode start/end of line
		- `i` - start insert mode (inside)
	- `ctrl+[` / `Esc` - exit insert mode
	- `o` / `O` - Add blank line below/above
	- `d` - Delete
		- `dd` - Delete line
- Phase 3: Copying and Pasting
	- `c` - Delete, copy, and start insert mode
		- `cc` - Delete, copy line, and start insert mode
	- `y` - copy
		- `yy` - copy line
	- `p` - paste
	- `u` - undo
- Phase 4: Selecting text
	- `v` - start visual mode
- Phase 5: Advanced
	- `gg` - go to top of page
	- `G` - go to bottom of page
	- `J` - Join line below to the current one
	- `r [character]` - replace (for typos)
	- `zz` - center current line in screen
- Phase 6: Repeaters and modifiers
	- `{number}j` - Go down `{number}` lines
	- `{number}k` - Go up `{number}` lines
	- `{number}G` - Go to line `{number}
	- `dw` - delete word

Ps.: I use the [Outliner plugin](https://github.com/vslinko/obsidian-outliner) to move bullet lists around. `CMD+1` for moving the list item (and children) up, `CMD+2` to move them down, and `CMD+3` to toggle folding.
