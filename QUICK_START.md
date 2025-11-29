# Quick Start Guide

Get up and running with Quran Video Creator in 5 minutes!

## Prerequisites Check

Before starting, ensure you have:

1. **Python 3.8+** installed
   ```bash
   python --version
   ```

2. **FFmpeg** installed
   ```bash
   ffmpeg -version
   ```

   If not installed:
   - **Windows**: `choco install ffmpeg` (or download from ffmpeg.org)
   - **macOS**: `brew install ffmpeg`
   - **Linux**: `sudo apt install ffmpeg`

## Installation (2 minutes)

### Option 1: Auto-Install (Recommended)

Just run the script - it will install everything automatically!

```bash
# Clone or download the repository
cd quran-video-creator

# Run the script
python quran_video_creator.py
```

The program will:
- Check for missing dependencies
- Offer to install them automatically
- Guide you through the setup

### Option 2: Manual Install

```bash
# Install all dependencies at once
pip install -r requirements.txt
```

## First Video (3 minutes)

1. **Run the program:**
   ```bash
   python quran_video_creator.py
   ```

2. **Follow the interactive prompts:**

   ```
   Select language: 1 (English)
   Select translation: 1 (Dr. Mustafa Khattab)
   Enter verse: 1:1
   Select visual: 1 (midnight_forest)
   Select reciter: 1 (Mishary)
   Create series: n
   ```

3. **Wait for processing** (1-2 minutes)

4. **Find your video:**
   ```
   QuranVideos/Surah_1_Verse_1.mp4
   ```

**That's it!** You've created your first Quran video!

## What's Next?

### Add API Keys (Optional)

For AI-generated backgrounds:

1. **Copy the example file:**
   ```bash
   cp .env.example .env
   ```

2. **Edit `.env` and add your keys:**
   ```env
   STABILITY_API_KEY=your_key_here
   PEXELS_API_KEY=your_key_here
   ```

3. **Get API keys:**
   - Stability AI: https://platform.stability.ai/
   - Pexels: https://www.pexels.com/api/

**Note:** The app works perfectly without API keys using gradient backgrounds!

### Create a Series

Perfect for daily social media posts:

```bash
python quran_video_creator.py
```

When prompted:
```
Verse Reference: 1:1-7
Create Series: y
```

Result: 7 individual videos in `QuranVideos/Series/`

### Customize Settings

Edit `config.json` to change defaults:

```json
{
  "preferences": {
    "default_language": "en",
    "default_qari": "mishary"
  }
}
```

## Common Issues

### "FFmpeg not found"
- **Solution:** Install FFmpeg (see Prerequisites above)
- **Verify:** Run `ffmpeg -version` in terminal

### "MoviePy not available"
- **Solution:** Run `pip install moviepy[optional]`
- Or let the auto-installer handle it

### "Arabic text displays incorrectly"
- **Solution:** Install Arabic support:
  ```bash
  pip install arabic-reshaper python-bidi
  ```

### API key not working
- **Solution:** Double-check your `.env` file
- Ensure no extra spaces around keys
- Remember: API keys are optional!

## Tips for Success

1. **Start Simple**
   - Create single verses first
   - Experiment with different visual presets
   - Try different languages

2. **Batch Create**
   - Use series mode for efficiency
   - Perfect for weekly content planning
   - One command creates multiple videos

3. **Social Media**
   - Videos are optimized for Instagram/TikTok
   - Use the generated caption files in `PostingTexts/`
   - Post consistently for best engagement

4. **Quality Settings**
   - Default settings work great for most uses
   - Edit the script for custom bitrates/resolution
   - Check the README for advanced options

## Example Workflows

### Daily Instagram Posts
```bash
# Create 7 videos at once
Verse: 67:1-7 (Surah Al-Mulk)
Series: Yes

# Post one video each day
# Use caption files from PostingTexts/
```

### Ramadan Series
```bash
# Day 1: 2:183-184 (Fasting prescribed)
# Day 2: 2:185 (Month of Ramadan)
# Day 3: 2:186 (I am near)
# ... continue through Ramadan
```

### Jummah Reminders
```bash
# Every Friday: One verse from Surah Al-Jumu'ah
Preset: mosque_architecture
Verses: 62:9-11
```

## Getting Help

- **Documentation:** Read [README.md](README.md) for full details
- **Examples:** Check [docs/EXAMPLES.md](docs/EXAMPLES.md) for more use cases
- **Issues:** Report bugs on GitHub
- **Questions:** Open a GitHub Discussion

## Next Steps

1. Read the full [README.md](README.md) for all features
2. Check out [EXAMPLES.md](docs/EXAMPLES.md) for creative ideas
3. Review [CONTRIBUTING.md](CONTRIBUTING.md) to contribute
4. Share your videos and spread the beauty of the Quran!

---

**JazakAllahu Khayran** for using Quran Video Creator!

May Allah accept this work and make it beneficial for the Ummah.
