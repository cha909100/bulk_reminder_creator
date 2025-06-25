{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fmodern\fcharset0 Courier;}
{\colortbl;\red255\green255\blue255;\red135\green5\blue129;}
{\*\expandedcolortbl;;\cssrgb\c60784\c13725\c57647;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh16640\viewkind0
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f0\fs28 \cf2 # \uc0\u55357 \u56517  Bulk Reminder Importer (AppleScript)\
\
A productivity-focused AppleScript that allows you to quickly import hundreds of reminders into the Apple Reminders app using a simple plain text format. Perfect for templated routines, project breakdowns, and daily workflows.\
\
## \uc0\u55357 \u56529  Table of Contents\
- [Features](#-features)\
- [Input Syntax](#-input-syntax)\
- [Input Methods](#-input-methods)\
- [Examples](#-examples)\
- [Output](#-output)\
- [Setup](#-setup)\
- [System Requirements](#-system-requirements)\
- [Troubleshooting](#-troubleshooting)\
- [License](#-license)\
- [Contributing](#-contributing)\
- [Version](#-version)\
\
## \uc0\u55357 \u56960  Features\
\
- One-line-per-task input with powerful inline syntax\
- Adds reminders to a dedicated list (`Autoreminders`)\
- Smart parsing: due dates, times, repeat patterns, tags, priority, notes, and URLs\
- Skips malformed lines with detailed error logging\
- Adds a batch tag to all imported reminders for traceability\
- Preview interface with syntax guidance\
- Log file saved to Desktop after each import\
\
---\
\
## \uc0\u9997 \u65039  Input Syntax\
\
Write one task per line. Each line can include optional modifiers using square bracket syntax.\
\
Task name [due:YYYY-MM-DD] [time:HH:MM] [repeat:daily|weekly|monthly*N] [tags:tag1,tag2] [priority:low|medium|high] [note:some text] [url:https://\'85]\
\
- `Task name` \'96 **Required**\
- `due:` \'96 Optional due date (defaults to today)\
- `time:` \'96 Optional time (defaults to `09:00`)\
- `repeat:` \'96 Optional recurrence, supports count (`daily*5`)\
- `tags:` \'96 Optional tags (comma-separated); batch tag always added\
- `priority:` \'96 Accepts `low`, `medium`, or `high`\
- `note:` \'96 Adds a note to the task\
- `url:` \'96 Appends URL to the notes field\
\
---\
\
## \uc0\u55357 \u56549  Input Methods\
\
When the script runs, you can choose between:\
\
- **Paste from clipboard**\
- **Select `.txt` file**\
- **Drag-and-drop text file onto the app**\
\
---\
\
## \uc0\u55358 \u56810  Examples\
\
Call John\
Buy groceries [due:2025-07-01] [time:14:00] [tags:errands,food] [priority:high]\
Daily standup [repeat:daily*5] [note:Team sync] [url:https://meet.link]\
Backup photos [repeat:monthly]\
\
---\
\
## \uc0\u55357 \u56514  Output\
\
- Reminders are added to the **Autoreminders** list\
- All imported reminders are tagged with a unique batch tag, e.g. `batch:2025-06-25_15-20-12`\
- A detailed log is saved to your Desktop:\
  - \uc0\u9989  Successful tasks\
  - \uc0\u10060  Errors with line numbers and messages\
\
---\
\
## \uc0\u55357 \u57056 \u65039  Setup\
\
1. Open `reminder_importer.applescript` in **Script Editor**\
2. Save it as a script or app\
3. (Optional) Add to the Dock or assign a hotkey via Automator\
\
---\
\
## \uc0\u9881 \u65039  System Requirements\
\
- macOS (tested on Monterey and later)\
- Apple Reminders app\
\
---\
\
## \uc0\u55358 \u56825  Troubleshooting\
\
- If Reminders app permissions are denied, go to **System Preferences > Security & Privacy > Automation**\
- Empty or malformed lines are logged but not added\
\
---\
\
## \uc0\u55357 \u56516  License\
\
MIT License \'96 do whatever you want, but give credit if you find this useful.\
\
---\
\
## \uc0\u55358 \u56605  Contributing\
\
Pull requests and suggestions welcome! Please open an issue first to discuss what you\'92d like to change.\
\
---\
\
## \uc0\u55358 \u56813  Version\
\
v1.0.0 \'96 First stable release.\
}
