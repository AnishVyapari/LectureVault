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
MIT License

Copyright (c) 2025 AnishVyapari

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

### 6. `requirements.txt`

discord.py
opencv-python
sounddevice
scipy
numpy
pyautogui
pillow
psutil
comtypes
pycaw
requests

text


---

## **GITHUB STRUCTURE EXAMPLE**


Bomboclat/
├── Bomboclat.py
├── bot_config.json.example # (add this instead of real token!)
├── .gitignore
├── README.md
├── LICENSE
├── requirements.txt


---

Use the above templates for a clean, professional look on GitHub.  
**Never upload a real bot token!** Rename your real `bot_config.json` to `bot_config.json.example` with a fake token for GitHub.
READ IMP IF YOU WANT TO DO SAME
