# 📅 Bulk Reminder Importer (AppleScript)

A productivity-focused AppleScript that allows you to quickly import hundreds of reminders into the Apple Reminders app using a simple plain text format. Perfect for templated routines, project breakdowns, and daily workflows.

## 📑 Table of Contents
- [Features](#-features)
- [Input Syntax](#-input-syntax)
- [Input Methods](#-input-methods)
- [Examples](#-examples)
- [Output](#-output)
- [Setup](#-setup)
- [System Requirements](#-system-requirements)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)
- [Contributing](#-contributing)
- [Version](#-version)

## 🚀 Features

- One-line-per-task input with powerful inline syntax
- Adds reminders to a dedicated list (`Autoreminders`)
- Smart parsing: due dates, times, repeat patterns, tags, priority, notes, and URLs
- Skips malformed lines with detailed error logging
- Adds a batch tag to all imported reminders for traceability
- Preview interface with syntax guidance
- Log file saved to Desktop after each import

---

## ✍️ Input Syntax

Write one task per line. Each line can include optional modifiers using square bracket syntax.

Task name [due:YYYY-MM-DD] [time:HH:MM] [repeat:daily|weekly|monthly*N] [tags:tag1,tag2] [priority:low|medium|high] [note:some text] [url:https://…]

- `Task name` – **Required**
- `due:` – Optional due date (defaults to today)
- `time:` – Optional time (defaults to `09:00`)
- `repeat:` – Optional recurrence, supports count (`daily*5`)
- `tags:` – Optional tags (comma-separated); batch tag always added
- `priority:` – Accepts `low`, `medium`, or `high`
- `note:` – Adds a note to the task
- `url:` – Appends URL to the notes field

---

## 📥 Input Methods

When the script runs, you can choose between:

- **Paste from clipboard**
- **Select `.txt` file**
- **Drag-and-drop text file onto the app**

---

## 🧪 Examples

Call John
Buy groceries [due:2025-07-01] [time:14:00] [tags:errands,food] [priority:high]
Daily standup [repeat:daily*5] [note:Team sync] [url:https://meet.link]
Backup photos [repeat:monthly]

---

## 📂 Output

- Reminders are added to the **Autoreminders** list
- All imported reminders are tagged with a unique batch tag, e.g. `batch:2025-06-25_15-20-12`
- A detailed log is saved to your Desktop:
  - ✅ Successful tasks
  - ❌ Errors with line numbers and messages

---

## 🛠️ Setup

1. Open `reminder_importer.applescript` in **Script Editor**
2. Save it as a script or app
3. (Optional) Add to the Dock or assign a hotkey via Automator

---

## ⚙️ System Requirements

- macOS (tested on Monterey and later)
- Apple Reminders app

---

## 🧹 Troubleshooting

- If Reminders app permissions are denied, go to **System Preferences > Security & Privacy > Automation**
- Empty or malformed lines are logged but not added

---

## 📄 License

MIT License – do whatever you want, but give credit if you find this useful.

---

## 🤝 Contributing

Pull requests and suggestions welcome! Please open an issue first to discuss what you’d like to change.

---

## 🧭 Version

v1.0.0 – First stable release.
