my<div align="center">

# 🎥 LectureVault - Discord Screen & Audio Recorder

### Automated lecture recording with screen capture and microphone audio for Discord

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Discord.py](https://img.shields.io/badge/discord.py-2.0%2B-7289DA?logo=discord&logoColor=white)](https://discordpy.readthedocs.io/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Latest-5C3EE8?logo=opencv&logoColor=white)](https://opencv.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Commands](#-commands) • [Configuration](#%EF%B8%8F-configuration) • [License](#-license)

</div>

---

## 🌟 Overview

**LectureVault** is a powerful Discord bot that automatically records your screen and captures microphone audio during lectures, meetings, or study sessions. Built with Python and optimized for performance, it saves recordings as compact, sped-up videos for easy review.

### Why LectureVault?

- 🎬 **Automatic Screen Recording** - Continuous 720p screen capture in 3-minute blocks
- 🎙️ **Manual Mic Recording** - On-demand audio recording with slash commands
- ⚡ **4x Speed Playback** - 3-minute recordings compressed to 45 seconds (< 8MB)
- 🔧 **Discord Integration** - Seamless slash commands for full control
- 💻 **Background Operation** - Runs silently as a Windows application
- 📦 **No Dependencies** - Uses built-in Windows libraries for video encoding

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎥 **Automatic Screen Recording** | Records screen in 3-minute blocks at 720p resolution with 4x speedup |
| 🎤 **Manual Mic Recording** | Start/stop microphone recording with `/startmic` and `/stopmic` commands |
| 📤 **Auto Upload** | Automatically uploads recordings to Discord channels |
| ⚙️ **System Integration** | Comprehensive system setup for seamless Discord integration |
| 🔒 **Secure Configuration** | Token-based authentication with config file |
| 🚀 **Lightweight** | Ultra-compact AVI format, optimized file sizes (< 8MB per 3-min block) |

---

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- Discord Bot Token ([Create one here](https://discord.com/developers/applications))
- Windows OS (for screen recording functionality)

### Step 1: Clone the Repository

```bash
git clone https://github.com/AnishVyapari/RAITRECORDER.git
cd RAITRECORDER
```

### Step 2: Install Dependencies

```bash
pip install opencv-python sounddevice scipy numpy discord.py pyautogui pillow psutil
```

### Step 3: Configure the Bot

Create a `bot_config.json` file in the root directory:

```json
{
  "token": "YOUR_BOT_TOKEN_HERE",
  "auto_startup": true
}
```

⚠️ **Security Warning**: Never commit your real Discord bot token to public repositories!

### Step 4: Run the Bot

```bash
python recorder_bot.py
```

---

## 🎮 Usage

### Automatic Screen Recording

The bot automatically starts recording your screen when launched:
- Records in 3-minute intervals
- Applies 4x speed compression
- Saves as ultra-compact AVI files (< 8MB)
- Auto-uploads to configured Discord channel

### Manual Microphone Recording

Control mic recording with slash commands:

```
/startmic  - Begin microphone recording
/stopmic   - Stop recording and upload WAV file
```

---

## 🎯 Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/startmic` | Start microphone recording | All users |
| `/stopmic` | Stop mic recording and upload | All users |

---

## ⚙️ Configuration

### `bot_config.json` Options

```json
{
  "token": "YOUR_BOT_TOKEN_HERE",       // Discord bot token
  "auto_startup": true                    // Auto-start recording on launch
}
```

### Building an Executable (Optional)

Create a standalone `.exe` file for easier distribution:

```bash
pyinstaller --onefile --noconsole --add-data "bot_config.json;." --name LectureVault recorder_bot.py
```

The executable will be created in the `dist/` folder.

---

## 📁 Project Structure

```
LectureVault/
├── recorder_bot.py              # Main bot application
├── bot_config.json              # Configuration file (DO NOT COMMIT!)
├── bot_config.json.example      # Example config (safe to commit)
├── .gitignore                   # Excludes sensitive files
├── requirements.txt             # Python dependencies
├── README.md                    # This file
└── LICENSE                      # MIT License
```

---

## 🛠️ Troubleshooting

### Common Issues

**Bot not responding to commands:**
- Ensure the bot has proper permissions in your Discord server
- Verify the bot token is correct in `bot_config.json`
- Check that slash commands are synced (may take up to 1 hour)

**Recording not working:**
- Confirm you're running on Windows (required for screen recording)
- Check that all dependencies are installed: `pip install -r requirements.txt`
- Verify sufficient disk space for recordings

**Upload failures:**
- Ensure file sizes are under Discord's limit (8MB for free servers, 50MB for Nitro)
- Check bot has `ATTACH_FILES` permission in the target channel

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 Fork the repository
2. 🔧 Create a feature branch: `git checkout -b feature/AmazingFeature`
3. 💾 Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. 📤 Push to the branch: `git push origin feature/AmazingFeature`
5. 🔍 Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** - see below for details:

```
MIT License

Copyright (c) 2025 Anish Vyapari

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
```

---

## 🌐 Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-AnishVyapari-181717?logo=github&logoColor=white)](https://github.com/AnishVyapari)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-7289DA?logo=discord&logoColor=white)](https://discord.gg/your-server)

**Made with ❤️ by Anish Vyapari**

[⬆ Back to top](#-lecturevault---discord-screen--audio-recorder)

</div>op
