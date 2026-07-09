

## Introduction

While learning Linux, I noticed that many people use the **VI editor** (or Vim) to create and edit files directly from the terminal.

At first, it felt confusing because I couldn't type anything after opening a file. Later, I understood that VI works in different modes, and once I learned them, using it became much easier.

## What is VI Editor?

VI is a text editor that comes with most Linux systems.

It is mainly used to create, edit, and save text files from the terminal.

Many developers and system administrators use it because it is fast and doesn't require a graphical interface.

## Opening a File

To open an existing file:

```bash
vi notes.txt
```

If the file doesn't exist, VI will create it when you save.

## Modes in VI

The most important thing to remember is that VI has different modes.

### Normal Mode

This is the default mode when you open a file.

In this mode, you can move around the file, copy, delete, search, and perform different actions.

You **cannot** type text in this mode.

### Insert Mode

This mode is used to write or edit text.

To enter Insert Mode, press:

```text
i
```

Now you can type normally.

To come back to Normal Mode, press:

```text
Esc
```

I found this to be the most important shortcut while learning VI.

## Saving a File

First press:

```text
Esc
```

Then type:

```text
:w
```

and press **Enter**.

This saves the file.

## Saving and Quitting

To save the file and exit:

```text
:wq
```

or simply:

```text
:x
```

## Quitting Without Saving

If I don't want to save the changes:

```text
:q!
```

This closes the editor without saving anything.

## Deleting Text

Delete one character:

```text
x
```

Delete the current line:

```text
dd
```

Delete multiple lines:

```text
5dd
```

This deletes five lines.

## Copy and Paste

Copy the current line:

```text
yy
```

Copy multiple lines:

```text
5yy
```

Paste below the current line:

```text
p
```

Paste above the current line:

```text
P
```

## Undo and Redo

Undo the last change:

```text
u
```

Redo the change:

```text
Ctrl + r
```

## Searching in a File

To search for a word:

```text
/word
```

Example:

```text
/Linux
```

Move to the next result:

```text
n
```

Move to the previous result:

```text
N
```

## Replacing a Word

Replace the first occurrence in the current line:

```text
:s/old/new/
```

Replace all occurrences in the file:

```text
:%s/old/new/g
```

## Moving Around the File

Go to the beginning of the file:

```text
gg
```

Go to the end of the file:

```text
G
```

Go to a specific line:

```text
:25
```

This moves to line number 25.

## Most Useful Shortcuts

| Shortcut   | Purpose               |
| ---------- | --------------------- |
| `i`        | Enter Insert Mode     |
| `Esc`      | Return to Normal Mode |
| `:w`       | Save                  |
| `:wq`      | Save and quit         |
| `:x`       | Save and exit         |
| `:q!`      | Quit without saving   |
| `x`        | Delete one character  |
| `dd`       | Delete current line   |
| `yy`       | Copy current line     |
| `p`        | Paste below           |
| `u`        | Undo                  |
| `Ctrl + r` | Redo                  |
| `/word`    | Search for a word     |
| `gg`       | Go to the beginning   |
| `G`        | Go to the end         |

## What I Learned

When I first opened the VI editor, I couldn't even figure out how to close it. After learning about Normal Mode and Insert Mode, everything started making sense.

I realized that I don't need to remember every shortcut. Just knowing how to open a file, enter Insert Mode, save, quit, copy, paste, and search is enough to get started. As I use VI more often, the shortcuts will become easier to remember.
