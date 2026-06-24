# CsvMan

**CsvMan** is a lightweight and fast desktop editor for **CSV** and **JSON** files
on Windows. It focuses on the day-to-day chores of working with tabular data:
opening many files at once, finding and fixing values quickly, comparing two
files side by side, and saving the result back without surprises.

![Platform](https://img.shields.io/badge/platform-Windows-blue)
![.NET](https://img.shields.io/badge/.NET-8.0-512BD4)
![Language](https://img.shields.io/badge/language-C%23-239120)

## Key Features

### File Handling
- Open one or many `.csv` / `.json` files at once (command line, **File → Open**, or drag-and-drop)
- Side panel with **Open files** and **Recent files** lists; right-click for per-file actions
- Recent files are remembered between sessions
- Window position, size, maximized state, and **panel split ratios** are restored on the next launch
- Per-file dirty tracking: closing a modified document prompts you to save
- Live file-watching: warns when a file changes on disk outside the editor

### CSV Editing
- Spreadsheet-style grid with proper quoting/escaping (CSV stays CSV on save)
- Add, remove, and duplicate rows
- Rename, delete, and reorder columns (move left / right)
- **Undo / Redo** for cell edits (`Ctrl+Z` / `Ctrl+Y`)
- Cut / Copy / Paste a multi-cell selection as TSV — round-trips with Excel
- Modified cells are highlighted so you can see at a glance what changed

### JSON Editing
- Loads MongoDB-style JSON (one document per line, extended values such as
  `$date`, `$oid`, `$numberLong`, etc.)
- Nested objects and arrays are flattened into dotted column names
  (e.g. `address.city`, `tags.0`) for grid editing
- On save, the flat structure is un-flattened back into the original nested shape

### Side-by-Side Compare (Diff)
- Toggle a **left / right split** to compare two files at once
- Differences are highlighted automatically (changed cells and extra rows)
- Both panes are **fully editable**, each with its own Undo/Redo and Save
- Positional (row-by-row) matching with column matching by header name
- **Next / Previous difference** navigation (`F8` / `Shift+F8`)
- Synchronized vertical scrolling; a warning is shown when both panes hold the same file
- Open into either pane from the file lists, right-click menus, or drag-and-drop

### Navigation & Search
- **Find** box with optional *match whole word*; matches highlighted across the grid
- `Enter` / `Shift+Enter` (or `F3` / `Shift+F3`) jumps to next / previous match
- **Replace** and Replace All (`Ctrl+H`)
- Go to row (`Ctrl+G`), keyboard-friendly paging, and Ctrl+Arrow jump-to-next-different-value

### Encoding & Delimiter
- Automatic encoding/delimiter detection on open; status-bar controls to change them
- CP949 (Korean) and UTF-8 support

## Keyboard Shortcuts

| Action               | Shortcut              |
| -------------------- | --------------------- |
| Open                 | `Ctrl+O`              |
| Save / Save As       | `Ctrl+S` / `Save As…` |
| Close                | `Ctrl+W`              |
| Undo / Redo          | `Ctrl+Z` / `Ctrl+Y`   |
| Copy / Paste         | `Ctrl+C` / `Ctrl+V`   |
| Find / Replace       | `Ctrl+F` / `Ctrl+H`   |
| Find next / previous | `F3` / `Shift+F3`     |
| Next / prev diff     | `F8` / `Shift+F8`     |
| Go to row            | `Ctrl+G`              |
| Page down / up       | `PageDown` / `PageUp` |

## System Requirements

- **OS:** Windows 10 or later
- **Framework:** [.NET 8.0 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0)
- **Installation:** Simply download the release, unzip, and run `CsvMan.exe`

No installation required — fully portable application.

## Third-Party Libraries

- **Newtonsoft.Json** 13.0.3 — JSON parsing/serialization, including MongoDB extended-JSON wrappers (MIT License)
- **System.Text.Encoding.CodePages** — legacy code-page (e.g. CP949) support

## License

**CsvMan** is open-source software released under the **MIT License**.

See the [LICENSE](LICENSE) file for full details.

---

_Copyright (c) 2026 HappySloth._
