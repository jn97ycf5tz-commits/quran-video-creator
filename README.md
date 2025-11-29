# Quran Video Creator

<div align="center">

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

*Create stunning professional Quran videos with AI-powered backgrounds and perfect audio synchronization*

[Features](#features) • [Installation](#installation) • [Quick Start](#quick-start) • [Configuration](#configuration) • [Documentation](#documentation)

</div>

---

## Overview

Quran Video Creator is a powerful Python application that generates professional-quality Islamic videos featuring Quran verses with:
- **Perfect Audio Synchronization**: Translation text appears simultaneously with Arabic recitation
- **AI-Generated Backgrounds**: Stunning visuals using Stability AI or Pexels stock videos
- **Multi-Language Support**: 8+ languages including English, Arabic, German, Bosnian, Albanian, French, Spanish, and Turkish
- **Professional Typography**: Beautiful Arabic calligraphy with gold accents and shadows
- **Bismillah Title Cards**: Automatic detection and display before each verse
- **Intelligent Page Timing**: Content-aware duration based on verse complexity

## Features

### Core Capabilities
- ✅ **AI-Powered Background Generation**: Stability AI integration for custom backgrounds
- ✅ **Stock Video Integration**: Pexels API support for high-quality stock footage
- ✅ **Perfect Text Synchronization**: Zero-delay translation display with Arabic audio
- ✅ **Multi-Page Support**: Automatic verse splitting for optimal readability
- ✅ **Professional Branding**: Customizable logos, watermarks, and branding elements
- ✅ **Batch Processing**: Create entire Surah series automatically
- ✅ **Social Media Ready**: Optimized for Instagram, TikTok, YouTube Shorts

### Technical Excellence
- 🔧 **Auto-Dependency Installation**: Automatically checks and installs required packages
- 🔧 **Enhanced Arabic Support**: Proper RTL text rendering with arabic-reshaper and python-bidi
- 🔧 **Memory Management**: Efficient resource cleanup and garbage collection
- 🔧 **Comprehensive Logging**: Professional logging framework for debugging
- 🔧 **Input Validation**: Security-focused input sanitization
- 🔧 **Type Hints**: Modern Python type annotations

### Visual Presets
- 🌲 **Midnight Forest**: Mystical forest scenes with moonlight
- 🌌 **Cosmic Nebula**: Space and galaxy backgrounds
- 🌅 **Golden Sunset**: Beautiful sunset skies
- 🌊 **Ocean Depths**: Underwater serenity
- 🌌 **Northern Lights**: Aurora borealis displays
- 🏔️ **Mountain Sunrise**: Majestic mountain scenes
- 🕌 **Mosque Architecture**: Islamic architectural beauty
- 🏜️ **Desert Dunes**: Golden desert landscapes

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- FFmpeg (for video processing)

### FFmpeg Installation

**Windows:**
```bash
# Using Chocolatey
choco install ffmpeg

# Or download from: https://ffmpeg.org/download.html
```

**macOS:**
```bash
brew install ffmpeg
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt update
sudo apt install ffmpeg
```

### Quick Install

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/quran-video-creator.git
cd quran-video-creator
```

2. **Run the script** (it will auto-install dependencies):
```bash
python quran_video_creator.py
```

The script will automatically detect and install missing Python packages.

### Manual Installation

If you prefer to install dependencies manually:

```bash
pip install -r requirements.txt
```

## Quick Start

### Basic Usage

1. **Set up API keys** (optional but recommended for AI backgrounds):
   - Copy `.env.example` to `.env`
   - Add your API keys (see [Configuration](#configuration))

2. **Run the program:**
```bash
python quran_video_creator.py
```

3. **Follow the interactive prompts:**
   - Select language for translation
   - Choose translation source
   - Enter verse reference (e.g., `1:1` or `1:1-7`)
   - Select visual preset
   - Choose audio reciter

### Example: Creating a Single Verse Video

```
Language: English
Translation: Dr. Mustafa Khattab, the Clear Quran
Verse: 1:1
Visual: midnight_forest
Reciter: mishary
```

### Example: Creating a Series

```
Series mode: Yes
Starting verse: 1:1
Ending verse: 1:7
Output: Creates 7 individual videos in QuranVideos/Series/
```

## Configuration

### API Keys

The application supports three optional APIs for enhanced backgrounds:

1. **Stability AI** (AI-generated backgrounds)
   - Get key: https://platform.stability.ai/
   - Add to `.env`: `STABILITY_API_KEY=your_key_here`

2. **OpenAI** (Future GPT integration)
   - Get key: https://platform.openai.com/
   - Add to `.env`: `OPENAI_API_KEY=your_key_here`

3. **Pexels** (Stock video footage)
   - Get key: https://www.pexels.com/api/
   - Add to `.env`: `PEXELS_API_KEY=your_key_here`

### Environment Variables

Create a `.env` file in the project root:

```env
# API Keys (all optional)
STABILITY_API_KEY=your_stability_key_here
OPENAI_API_KEY=your_openai_key_here
PEXELS_API_KEY=your_pexels_key_here
```

### Configuration File

Edit `config.json` for preferences:

```json
{
  "api_keys": {
    "openai": "",
    "stability": "",
    "pexels": ""
  },
  "preferences": {
    "default_language": "en",
    "default_qari": "mishary"
  }
}
```

**Note**: Environment variables take precedence over `config.json` values for security.

## Supported Languages

| Language | Code | Translations Available |
|----------|------|------------------------|
| English | en | 5 (Dr. Mustafa Khattab, Saheeh International, Yusuf Ali, Pickthall, Taqi Usmani) |
| German | de | 1 (Frank Bubenheim & Nadeem Elyas) |
| Bosnian | bs | 1 (Muhamed Mehanović) |
| Albanian | sq | 1 (Efendi Nahi) |
| Arabic | ar | Original text |
| French | fr | 1 (King Fahad Quran Complex) |
| Spanish | es | 1 |
| Turkish | tr | 1 |

## Output Structure

```
QuranVideos/
├── Series/                 # Batch-created videos
│   ├── Surah_1_Verse_1.mp4
│   ├── Surah_1_Verse_2.mp4
│   └── ...
├── PostingTexts/          # Social media captions
│   ├── Surah_1_Verse_1.txt
│   └── ...
├── temp/                  # Temporary audio files
└── backgrounds/           # Downloaded/generated backgrounds
```

## Advanced Features

### Custom Visual Presets

Edit the `visual_presets` dictionary in the code to create custom background themes with specific:
- AI generation prompts
- Color gradients
- Text colors and effects
- Animation styles
- Pexels search queries

### Quality Settings

Adjust `quality_settings` in the code:
- Video bitrate: Default 8000k
- Audio bitrate: Default 192k
- FPS: Default 30
- Text scale factors
- Shadow and glow effects

### Page Display Settings

Configure `page_settings` for verse pagination:
- Max characters per page
- Translation delay (default 0.0 for perfect sync)
- Transition durations
- Page animation styles

## Troubleshooting

### Common Issues

**"MoviePy not available"**
- Solution: Run `pip install moviepy[optional]`

**"FFmpeg not found"**
- Solution: Install FFmpeg (see [Installation](#installation))

**"API key invalid"**
- Solution: Check your `.env` file or `config.json`
- API keys are optional - the app works without them using gradient backgrounds

**Arabic text not displaying correctly**
- Solution: Install Arabic support libraries:
  ```bash
  pip install arabic-reshaper python-bidi
  ```

**Memory errors with large batches**
- Solution: Process fewer videos at once
- Reduce video quality settings

### Logs

Check `quran_video_creator.log` for detailed error information.

## Development

### Project Structure

```
quran-video-creator/
├── quran_video_creator.py  # Main application
├── config.json             # Configuration file
├── .env.example           # Example environment variables
├── requirements.txt       # Python dependencies
├── README.md             # This file
├── LICENSE               # MIT License
├── CONTRIBUTING.md       # Contribution guidelines
└── docs/                 # Additional documentation
```

### Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Running Tests

The application includes built-in test functions. Enable testing mode in the code or run specific test methods.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

### APIs and Libraries
- [Quran.com API](https://quran.api-docs.io/) - Verse data and translations
- [MoviePy](https://zulko.github.io/moviepy/) - Video editing
- [Edge TTS](https://github.com/rany2/edge-tts) - Text-to-speech
- [Stability AI](https://stability.ai/) - AI background generation
- [Pexels](https://www.pexels.com/) - Stock video footage
- [Pillow](https://python-pillow.org/) - Image processing

### Fonts
- Arabic typography powered by system fonts
- Enhanced Arabic support via arabic-reshaper and python-bidi

## Roadmap

- [ ] Web interface for easier video creation
- [ ] More visual preset options
- [ ] Custom font uploads
- [ ] Video template system
- [ ] Cloud rendering support
- [ ] Mobile app version
- [ ] Real-time preview

## Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/quran-video-creator/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/quran-video-creator/discussions)

## Acknowledgments

Special thanks to:
- The Quran.com team for their excellent API
- All contributors and testers
- The open-source community

---

<div align="center">

**Made with ❤️ for the Muslim community**

*Share the beauty of the Quran through engaging video content*

</div>
