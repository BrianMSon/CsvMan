# CsvMan v1.0.0 Release Notes

**Date:** 2026-06-24
**Status:** Initial Release

---

## Welcome to CsvMan!

The first official release of **CsvMan**, a lightweight and fast editor for
**CSV** and **JSON** files on Windows, now with a full **side-by-side compare**
mode.

---

## Key Features

### File Handling
- Open one or many `.csv` / `.json` files (command line, **File → Open**, or drag-and-drop)
- **Open files** and **Recent files** side lists with right-click actions
- Recent files remembered between sessions
- Window position/size/state and **panel split ratios** restored on next launch
- Per-file dirty tracking with save prompts
- File-watching: warns when a file changes on disk

### CSV Editing
- Spreadsheet-style grid with proper quoting/escaping
- Add / remove / duplicate rows; rename / delete / reorder columns
- Undo / Redo for cell edits
- Multi-cell Cut / Copy / Paste as TSV (Excel-compatible)
- Modified cells highlighted

### JSON Editing
- MongoDB-style line-delimited JSON with extended values (`$date`, `$oid`, `$numberLong`, …)
- Nested objects/arrays flattened to dotted columns for editing, un-flattened on save

### Side-by-Side Compare (Diff)
- Left / right split to compare two files at once
- Automatic difference highlighting (changed cells, extra rows)
- Both panes fully editable, each with independent Undo/Redo and Save
- Positional row matching, header-name column matching
- Next / Previous difference navigation (`F8` / `Shift+F8`)
- Synchronized scrolling; same-file warning
- Open into either pane via lists, right-click menus, or drag-and-drop

### Navigation & Search
- Find with optional match-whole-word, highlighted across the grid
- Find next/previous (`F3` / `Shift+F3`), Replace / Replace All (`Ctrl+H`)
- Go to row (`Ctrl+G`), accelerated paging, Ctrl+Arrow value jumps

### Encoding & Delimiter
- Automatic detection on open; status-bar controls to change
- CP949 (Korean) and UTF-8 support

---

## System Requirements

| Requirement  | Specification        |
|--------------|----------------------|
| OS           | Windows 10 or later  |
| Framework    | .NET 8.0             |
| Architecture | x64                  |

---

## Installation

1. Download the release ZIP file
2. Extract to your preferred location
3. Run `CsvMan.exe`

No installation required — fully portable application.

---

## Third-Party Libraries

- **Newtonsoft.Json** 13.0.3 (MIT License)
- **System.Text.Encoding.CodePages** (legacy code-page support)

---

Thank you for using CsvMan!

_Copyright (c) 2026 HappySloth._
