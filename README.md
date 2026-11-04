# Pulse Click

A minimal, dark-themed autoclicker built with Python. Works for games, testing, and repetitive tasks.

![Pulse Click](https://github.com/akshar-g/PulseClick/blob/main/screenshot.png?raw=true)

## Features

- Neon, glassy UI with animated ripples that pulse on every click
- Speed slider (1-100 CPS) plus one-tap presets: Chill, Steady, Turbo, Max
- Humanize slider adds random timing variation (0-50%)
- Left / Middle / Right button, Single / Double click
- Click limit: infinite, 100, 500, or 1K
- Toggle or Hold mode
- Global, rebindable hotkey (default `F6`) that works while other apps are focused
- 3 second countdown on the Start button, pin-on-top, live click counter

## Install

```bash
git clone https://github.com/<your-username>/pulse-click.git
cd pulse-click
pip install -r requirements.txt
python main.py
```

Requires Python 3.9+. Tkinter ships with the standard Windows/macOS installers.

## Usage

1. Drag the speed slider (or tap a preset) and set humanize, limit, and click type.
2. Pick button, click type, and mode.
3. Place your cursor where you want to click and press the hotkey (or hit **Start**, which gives a 3 second head start).
4. Press the hotkey again to stop. In **Hold** mode, clicking runs only while the key is held.

Click the hotkey box to rebind it. `Esc` cancels rebinding.

## Build an .exe (Windows)

```bash
pip install pyinstaller
pyinstaller --onefile --noconsole --name PulseClick main.py
```

The result lands in `dist/`.

## Notes

- Speeds above ~60 CPS may be limited by OS timer resolution on Windows.
- On macOS, grant Accessibility and Input Monitoring permissions to your terminal or app.
- Some online games prohibit automation and anti-cheat may flag it. Check a game's rules before using this there.

## License

MIT
