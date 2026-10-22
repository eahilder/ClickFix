# ClickFix Calculator Test

A single-file HTML page for testing detections around a clipboard-to-Windows-Run workflow. The command launches Windows Calculator through PowerShell's `-EncodedCommand`; its decoded content is `Start-Process calc.exe`.

## Run locally

From the repository directory:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. The page attempts to copy the command on load and reports the result. If the browser blocks it, use **Copy command** or copy the visible text manually. Press **Win + R**, paste the command, and press **Enter** to launch Calculator.

## Requirements

- Windows and Windows PowerShell to run the Calculator command.
- Python 3 to serve the page with the command above.
- Browser clipboard access; automatic copying depends on browser permissions.

No build step, dependencies, or external assets are required.
