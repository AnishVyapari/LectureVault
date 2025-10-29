<!-- Glass Disk/Audio Themed Banner -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=14,17,20,23&height=200&section=header&text=LectureVault&fontSize=60&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Record.%20Store.%20Review.&descSize=20&descAlignY=55" alt="LectureVault Banner" width="100%"/>
</div>

<!-- Animated Audio Wave Loader -->
<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212749447-bfb7e725-6987-49d9-ae85-2015e3e7cc41.gif" width="400">
  <br>
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=9B59B6&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=100&lines=%F0%9F%8E%A4+Recording+Audio...;%F0%9F%8E%A5+Capturing+Screen...;%F0%9F%93%80+Glass+Disk+Processing..." alt="Audio Loader">
</div>

<div align="center">

# 🎥 LectureVault - Discord Screen & Audio Recorder

### Automated lecture recording with screen capture and microphone audio for Discord

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/) [![Discord.py](https://img.shields.io/badge/discord.py-2.0%2B-7289DA?logo=discord&logoColor=white)](https://discordpy.readthedocs.io/) [![OpenCV](https://img.shields.io/badge/OpenCV-Latest-5C3EE8?logo=opencv&logoColor=white)](https://opencv.org/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

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

---

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- Windows OS (for optimal performance)
- Discord Bot Token ([Get one here](https://discord.com/developers/applications))

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/AnishVyapari/LectureVault.git
   cd LectureVault
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure the bot**
   - Edit `bot_config.json` with your settings:
   ```json
   {
     "token": "YOUR_BOT_TOKEN",
     "channel_id": "YOUR_CHANNEL_ID",
     "screen_record_interval": 180
   }
   ```

4. **Run the bot**
   ```bash
   python Bomboclat.py
   ```

---

## 🎮 Usage

### Starting the Bot

1. Run `Bomboclat.py` to start the bot
2. The bot will automatically:
   - Connect to Discord
   - Begin screen recording in 3-minute intervals
   - Upload recordings to the configured channel

### Recording Controls

```bash
# Start microphone recording
/startmic

# Stop microphone recording
/stopmic

# Check bot status
/status
```

---

## 📋 Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `/startmic` | Start microphone recording | `/startmic` |
| `/stopmic` | Stop mic recording and upload | `/stopmic` |
| `/status` | Check recording status | `/status` |
| `/help` | Display help information | `/help` |

---

## ⚙️ Configuration

### bot_config.json

```json
{
  "token": "YOUR_DISCORD_BOT_TOKEN",
  "channel_id": "CHANNEL_ID_FOR_UPLOADS",
  "screen_record_interval": 180,
  "video_quality": "720p",
  "speed_multiplier": 4,
  "audio_sample_rate": 44100
}
```

### Settings Explained

- **token**: Your Discord bot token
- **channel_id**: Discord channel for uploads
- **screen_record_interval**: Recording duration in seconds (default: 180)
- **video_quality**: Resolution (720p, 1080p)
- **speed_multiplier**: Video speedup factor (default: 4x)
- **audio_sample_rate**: Audio quality in Hz

---

## 🛠️ Technical Details

### Architecture

```
LectureVault/
├── Bomboclat.py          # Main bot script
├── bot_config.json       # Configuration file
├── README.md             # Documentation
└── .github/
    └── workflows/        # CI/CD workflows
```

### Dependencies

- `discord.py` - Discord API wrapper
- `opencv-python` - Video processing
- `pyaudio` - Audio capture
- `numpy` - Data processing
- `pillow` - Image handling

### Recording Process

1. **Screen Capture**: Uses OpenCV to capture screen at 720p
2. **Audio Recording**: Captures microphone input via PyAudio
3. **Video Encoding**: Compresses with 4x speedup using Windows codecs
4. **Upload**: Sends to Discord via bot API

---

## 🔒 Privacy & Security

- All recordings are stored locally before upload
- Bot token should be kept secure
- Recordings are automatically deleted after upload
- No external services collect your data

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Discord.py community for excellent documentation
- OpenCV contributors for powerful video processing
- All contributors and users of LectureVault

---

## 📧 Contact

For questions, issues, or suggestions:

- Open an [Issue](https://github.com/AnishVyapari/LectureVault/issues)
- Submit a [Pull Request](https://github.com/AnishVyapari/LectureVault/pulls)
- Join our Discord community

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=14,17,20,23&height=100&section=footer" alt="Footer" width="100%"/>
  <br>
  <strong>Made with ❤️ for students and learners everywhere</strong>
</div>
