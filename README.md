# Bomboclat Discord Bot

Universal screen and mic recorder for Discord using Python.  
- Automatic **continuous screen recording** (720p, 4x speed, 3min → 45s, <8MB)
- Manual **mic recording** (`/startmic` / `/stopmic`)
- Discord slash commands for automation
- Runs as a background Windows application

## Features
- **Automatic Screen Recording:** 3min blocks, 4x speed, ultra-compact AVI video, no libraries required
- **Manual Mic Recording:** Start/stop with Discord commands, uploads as WAV
- **Comprehensive system/channel setup** for seamless Discord integration

## Requirements
- Python 3.8+
- pip install opencv-python sounddevice scipy numpy discord.py pyautogui pillow psutil

## Setup

1. Clone this repo.
2. Create a `bot_config.json` from the example and paste your Discord bot token.
3. Run:
4. (Optional) Build EXE with no console:
pyinstaller --onefile --noconsole --add-data "bot_config.json;." --name Bomboclat Bomboclat.py

## Example `bot_config.json`
{
"token": "YOUR_BOT_TOKEN_HERE",
"auto_startup": true
}
**Never commit your real Discord bot token publicly!**

---

### 5. `LICENSE` (MIT recommended)
