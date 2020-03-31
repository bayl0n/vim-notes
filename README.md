# Vim Notes

Most of the notes are from [Talk on going mouseless with Vim, Tmux, and Hotkeys](https://www.youtube.com/watch?v=E-ZbrtoSuzw)

## Vim: modal editor

*4 Essential Modes*

| Mode | Sample triggering keystrokes|
|---| ----|
|Normal Mode | ```Esc``` |
| Insert Mode | i, a, c |
| Visual Mode | v, V, ```<Ctrl-v>``` |
| Command-line Mode | :, / |

 Think **operators, text objects,** and **motions**

## Operators

Operators are the *verbs* of vim

### Sample operators

| Keys | Description |
|---|---|
| c | change |
| d | delete |
| y | yank into register |
| ~ | swap case |
| gu | make lowercase |
| gU | make uppercase |
| ! | filter to external program |
| < | shift left |
| > | shift right |
| = | indent |

## Text Objects

Text objects are the *nouns* of vim

### Sample text objects

| Keys | Description |
|---|---|
| aw | a word |
| iw | inner word |
| aW | a WORD |
| iW | inner WORD |
| ap | a paragraph |
| ip | inner paragraph |
| ab | a bracket |
| ib | inner bracket |
| at | a tag block |
| it | inner tag block |

**NOTE:** W means any stream of non-whitespace characters whilst w are what vim represents using keywords (which depends on settings)

## Motion

How you navigate around Vim

### Sample motions

| Keys | Description |
|---|---|
| % | go to first matching parenthesis/bracket |
| [count]+ | down to first non-blank char of line |
| [count]$ | to end of line |
| [count]f/F {char} | to next occurence of {char} |
| [count]t/T {char} | to before next occurence of {char} |
| [count]h/j/k/l | left, down, up, or right |
| [count]]m | go to beginning of next method |
| [count]w/W | go a word/WORD to the right |
| [count]b/B | go a word/WORD to the left |
| [count]e/E | go to end of word/WORD right |

## Puttting it all together

```[count][operator][text object / motion]```

```6+``` = 6x go down to line start

```gUaW``` = capitalise a WORD

```3ce``` = 3

## Advanced Navigation

* [Various Motions](#various-motions)
* [Editing](#editing)
* [Searches](#searches)
* [Marks](#marks)
* [Tags](#tags)
* Jumplist + Changelist

### Various motions

**Always be scrolling!**

Also remember `H` `M` `L` -- High, Middle, Low

As well as `zt`, `zz`, `zb` -- Put current cursor to top, middle, or bottom of screen

### Editing

**Four basic commands**

| Keys | Definition |
| --- | --- |
| **:e**[dit] [++opt] [+cmd] {file} | Finds a file based on the current working directory |
| **:fin**[d][!] [++opt] [+cmd] {file} | File indexing |
| gf | Go to file |
| Ctrl-^ | Switch buffers |

### Searches

**Sample search patterns**

| Keys | Definition |
| ---- | ---------- |
| `/{patt} [/]<CR>` | search for {patt} |
| `/<CR>` | search for last used pattern |
| `?{patt}[?]<CR>` | search back for {patt} |
| `?<CR>` | search back for last used pattern |
| `[count]n` | repeat last search [count] times |
| `[count]N` | same as above, opposite directon |
| `*` | search forward for word under cursor |
| `#` | same as above, opposite direction |
| `gd` | go to local declaration |
| `:hls!` | toggle search highlighting |

