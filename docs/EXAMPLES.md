# Quran Video Creator - Usage Examples

This document provides practical examples for using Quran Video Creator in various scenarios.

## Table of Contents

- [Basic Examples](#basic-examples)
- [Advanced Examples](#advanced-examples)
- [Batch Processing](#batch-processing)
- [Custom Styling](#custom-styling)
- [Troubleshooting Examples](#troubleshooting-examples)

## Basic Examples

### Example 1: Create a Single Verse Video

The simplest use case - creating a video for one verse.

**Scenario:** You want to create a video for the first verse of Al-Fatiha in English.

**Steps:**
1. Run the program: `python quran_video_creator.py`
2. When prompted:
   ```
   Language: 1 (English)
   Translation: 1 (Dr. Mustafa Khattab, the Clear Quran)
   Verse Reference: 1:1
   Visual Preset: 1 (midnight_forest)
   Reciter: 1 (Mishary Rashid Al-Afasy)
   Create Series: n
   ```

**Output:**
- Video file: `QuranVideos/Surah_1_Verse_1.mp4`
- Caption file: `QuranVideos/PostingTexts/Surah_1_Verse_1.txt`

---

### Example 2: Albanian Translation

Creating content for Albanian-speaking audiences.

**Scenario:** Create a video with Albanian translation (Efendi Nahi).

**Steps:**
```
Language: 4 (Albanian)
Translation: 1 (Efendi Nahi)
Verse Reference: 2:255 (Ayat al-Kursi)
Visual Preset: 5 (northern_lights)
Reciter: 1 (Mishary)
```

**Output:**
Beautiful video with Albanian subtitle for the famous Throne Verse.

---

### Example 3: Multiple Verses (Range)

**Scenario:** Create a video covering multiple verses together.

**Steps:**
```
Language: 1 (English)
Translation: 2 (Saheeh International)
Verse Reference: 55:1-13
Visual Preset: 2 (cosmic_nebula)
Reciter: 2 (Abdul Basit)
```

**Result:**
One video containing verses 1-13 of Surah Ar-Rahman, with pages automatically created for optimal readability.

---

## Advanced Examples

### Example 4: Series Creation

Creating multiple individual videos for a complete Surah.

**Scenario:** Create separate videos for each verse of Surah Al-Fatiha (1:1-7).

**Steps:**
```
Language: 1 (English)
Translation: 1 (Dr. Mustafa Khattab)
Verse Reference: 1:1-7
Visual Preset: 6 (mountain_sunrise)
Reciter: 1 (Mishary)
Create Series: y
```

**Output:**
```
QuranVideos/Series/
├── Surah_1_Verse_1.mp4
├── Surah_1_Verse_2.mp4
├── Surah_1_Verse_3.mp4
├── Surah_1_Verse_4.mp4
├── Surah_1_Verse_5.mp4
├── Surah_1_Verse_6.mp4
└── Surah_1_Verse_7.mp4

PostingTexts/
├── Surah_1_Verse_1.txt
├── Surah_1_Verse_2.txt
└── ...
```

Perfect for daily Instagram/TikTok posts!

---

### Example 5: Custom Visual Themes

**Scenario:** Using different visual presets for different moods.

**Night/Contemplation Verses:**
```
Visual Preset: midnight_forest or northern_lights
Best for: Verses about reflection, night prayer, contemplation
Example: Surah Al-Muzammil (73:1-10)
```

**Creation/Universe Verses:**
```
Visual Preset: cosmic_nebula or ocean_depths
Best for: Verses about Allah's creation, universe
Example: Surah Ar-Rahman (55:1-13)
```

**Hope/Mercy Verses:**
```
Visual Preset: golden_sunset or mountain_sunrise
Best for: Verses about Allah's mercy, hope
Example: Surah Az-Zumar (39:53)
```

**Islamic Architecture:**
```
Visual Preset: mosque_architecture
Best for: Verses about prayer, worship
Example: Surah An-Noor (24:36-38)
```

---

### Example 6: Multi-Language Content Strategy

**Scenario:** Creating content for different communities.

**Monday - English Content:**
```
Language: English
Translation: Dr. Mustafa Khattab (modern, clear)
Verse: 2:286 (Allah does not burden a soul...)
```

**Tuesday - German Content:**
```
Language: German
Translation: Frank Bubenheim & Nadeem Elyas
Verse: Same verse in German
```

**Wednesday - Bosnian Content:**
```
Language: Bosnian
Translation: Muhamed Mehanović
Verse: Same verse in Bosnian
```

This creates a consistent message across different language communities.

---

## Batch Processing

### Example 7: Weekly Content Calendar

**Scenario:** Prepare a week's worth of content in advance.

**Day 1-7:**
Create series for Surah Al-Mulk (67:1-7)
```
Verse Reference: 67:1-7
Create Series: y
```

Result: 7 videos ready for daily posting!

---

### Example 8: Complete Short Surahs

**Scenario:** Create complete Surah videos for memorization content.

**Recommended Short Surahs:**
- Surah Al-Fatiha: `1:1-7`
- Surah Al-Ikhlas: `112:1-4`
- Surah Al-Falaq: `113:1-5`
- Surah An-Nas: `114:1-6`
- Surah Al-Kawthar: `108:1-3`
- Surah Al-Asr: `103:1-3`

Create series for each, then organize into playlists!

---

## Custom Styling

### Example 9: Ramadan Special Series

**Theme:** Golden sunset for iftar reminders

```
Language: Your choice
Visual Preset: golden_sunset
Verses: Select merciful, hopeful verses
Examples:
- 2:185 (Ramadan month)
- 2:186 (I am near)
- 97:1-5 (Laylat al-Qadr)
```

**Output Style:** Warm, inviting visuals perfect for Ramadan content.

---

### Example 10: Jummah Reminder Series

**Theme:** Mosque architecture for Friday

```
Language: Your choice
Visual Preset: mosque_architecture
Verses: Surah Al-Jumu'ah (62:9-11)
Create Series: y
```

Perfect for Friday reminders on social media!

---

## Troubleshooting Examples

### Example 11: Testing API Keys

**Scenario:** Verify your API keys are working.

**Test with Stability AI:**
```
1. Add STABILITY_API_KEY to .env
2. Create video with cosmic_nebula preset
3. Check backgrounds/ folder for generated image
```

**Test with Pexels:**
```
1. Add PEXELS_API_KEY to .env
2. Create video (any preset has Pexels fallback)
3. Check logs for "Downloaded from Pexels" message
```

---

### Example 12: Working Without API Keys

**Scenario:** You don't have API keys but want to create videos.

**Solution:** The app creates beautiful gradient backgrounds automatically!

```
# Simply leave .env file empty or don't create it
# Run program normally
```

The app will use:
- Gradient backgrounds matching the preset theme
- All other features work perfectly
- Professional-looking results

---

## Social Media Optimization

### Instagram Reels / TikTok

**Best Practices:**
- Use series mode for daily content
- Choose visually striking presets (cosmic_nebula, northern_lights)
- Keep verse count low (1-3 verses max)
- Focus on impactful, relatable verses

**Example Strategy:**
```
Week 1: Patience verses (golden_sunset)
Week 2: Gratitude verses (mountain_sunrise)
Week 3: Hope verses (northern_lights)
Week 4: Reflection verses (midnight_forest)
```

### YouTube Shorts

**Recommendations:**
- Slightly longer content (2-5 verses)
- Use descriptive posting texts as video descriptions
- Create themed playlists (Juz, Surah, Topic)

---

## Tips and Tricks

### Tip 1: Choosing the Right Reciter

**Mishary Rashid Al-Afasy:**
- Clear pronunciation
- Moderate pace
- Great for beginners

**Abdul Basit:**
- Classical, beautiful recitation
- Slightly slower
- Great for reflection

**Saad Al-Ghamdi:**
- Modern, popular style
- Good pace
- Widely recognized

### Tip 2: Translation Selection

**Dr. Mustafa Khattab (English):**
- Modern, accessible language
- Great for young audiences
- Clear and relatable

**Saheeh International:**
- Literal, precise
- Good for study
- Traditional style

### Tip 3: Visual Preset Matching

**Match visuals to verse themes:**
- Night/Stars verses → cosmic_nebula
- Nature verses → midnight_forest, mountain_sunrise
- Ocean/water verses → ocean_depths
- General/any → golden_sunset (universally appealing)

---

## Need Help?

- Check the main [README.md](../README.md) for installation help
- Review [CONTRIBUTING.md](../CONTRIBUTING.md) for bug reports
- Open an issue on GitHub for specific problems

---

**May Allah make it easy for you to create beautiful Quranic content!**
