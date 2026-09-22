# PageMode

Scroll through Markdown notes page by page, step between notes with the mouse wheel, and file notes away quickly.

## Wheel navigation

PageMode treats every Markdown file in the vault as one continuous sequence, ordered like File explorer: folders first, then files, sorted by name with natural number ordering. Files inside the archive folder are skipped.

Wheeling over these areas of a note in the main workspace opens the next or previous note in the same tab:

- **File position bar** — a thin bar in the note's left margin. Its thumb shows where the current note sits in the sequence, and hovering it shows the position (`12 / 340`) and the note's path.
- **Inline title** and the area above it.
- **Tab header and view header** of the active tab.

Wheeling over an empty tab opens the first note (wheel down) or the last note (wheel up).

Wheel navigation works in both editing and reading view. It is ignored while `Ctrl`, `Cmd`, `Alt`, or `Shift` is held, and in side panels. The opened note is also selected in File explorer.

## Page-unit scrolling

When **Page-unit scrolling** is on, wheel and trackpad gestures inside a note scroll by one screen at a time, snapping to line boundaries so that no line is cut off at the top. At the top or bottom of a note, the next gesture moves to the previous or next note.

It is off by default; normal scrolling is used when it is off.

## Filing

- **Archive** moves a file or folder into the archive folder while keeping its path. For example, `Projects/Plan.md` becomes `archive/Projects/Plan.md`.
- **Unarchive** moves it back to its original path.
- **Move active file here** moves the note that is currently open into a folder.

Archive and Unarchive are available from the command palette (for the current file) and from the right-click menu in File explorer (for any file or folder). Move active file here is in a folder's right-click menu. Missing folders are created, and if the destination name is already taken, a number is appended (`Plan 1.md`). Links are updated by Obsidian as with a normal move.

## Commands

- **Open next Markdown file**
- **Open previous Markdown file**
- **Archive current file**
- **Unarchive current file**

## Settings

- **Page-unit scrolling** — scroll one page at a time and move between notes at the edges. Default: off.
- **Archive folder** — where archived items go. Default: `archive`.
- **Show archive folder** — show the archive folder in File explorer. Default: off (hidden). Archived files are excluded from wheel navigation either way.

PageMode requires Obsidian `1.6.6` or newer.
