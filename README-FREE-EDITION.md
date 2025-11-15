# ClearSpeak V3 - Free Edition

**Professional Multilingual Text-to-Speech Platform**

Version 3.17.0 | Released January 2025 | Free for Personal and Commercial Use

---

## Overview

ClearSpeak V3 is a professional desktop application designed for creating high-quality voice prompts and announcements for PABX systems, IVR platforms, and professional audio projects. It's completely **FREE** with no license activation required.

### Key Features

- **Professional TTS Integration**
  - Google Cloud Text-to-Speech (50+ languages, 200+ voices)
  - ElevenLabs AI voices
  - Batch processing with CSV import
  
- **AI-Powered Text Enhancement**
  - Gemini AI text correction and improvement
  - Professional text normalization
  - Multi-language support

- **Professional Audio Tools**
  - Silence detection and removal
  - Normalization and compression
  - Format conversion (WAV, MP3, OGG)
  - Metadata editing

- **Workflow Automation**
  - CSV batch import
  - Project management
  - Export to multiple formats

---

## System Requirements

### macOS
- **Apple Silicon**: macOS 11.0 (Big Sur) or later
- **Intel**: macOS 10.15 (Catalina) or later
- 500 MB free disk space
- Internet connection (for TTS services)

### Windows
- Windows 10 or Windows 11 (64-bit)
- 500 MB free disk space
- Internet connection (for TTS services)

---

## Installation

### macOS Installer (.dmg)

1. Download the appropriate .dmg file for your Mac
   - Apple Silicon (M1/M2/M3/M4): `ClearSpeak-V3-3.17.0-MAC_AppleSilicon_Installer.dmg`
   - Intel: `ClearSpeak-V3-3.17.0-MAC_Intel_Installer.dmg`

2. Open the .dmg file

3. Drag ClearSpeak V3 to your Applications folder

4. **Important**: First-time launch
   - Right-click the app in Applications
   - Select "Open"
   - Click "Open" when macOS security warning appears
   - Subsequent launches work normally

### macOS Portable (.zip)

1. Download the appropriate .zip file for your Mac
2. Extract the .zip file
3. Right-click the app and select "Open"
4. Click "Open" when security warning appears

### Windows (.zip)

1. Download `ClearSpeak-V3-3.17.0-Windows10_11_Portable.zip`

2. Extract the ZIP to any location (e.g., `C:\ClearSpeak`)

3. Run `clearspeak-v3.exe`

4. **If Windows SmartScreen appears**:
   - Click "More info"
   - Click "Run anyway"
   - (This is normal for unsigned applications)

---

## Getting Started

### First Launch

1. **No License Required** - ClearSpeak V3 is completely free
2. The app will load directly to the main interface
3. Configure your API credentials for TTS services

### Setting Up TTS Services

#### Google Cloud TTS (Recommended)

1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Create a new project or select existing
3. Enable "Cloud Text-to-Speech API"
4. Create a Service Account key (JSON)
5. In ClearSpeak: Settings → Google Cloud → Upload JSON key

#### ElevenLabs (Optional)

1. Sign up at [ElevenLabs.io](https://elevenlabs.io)
2. Get your API key from dashboard
3. In ClearSpeak: Settings → ElevenLabs → Enter API key

#### Gemini AI (Optional)

1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create API key
3. In ClearSpeak: Settings → Gemini AI → Enter API key

### Creating Your First Project

1. Click "New Project"
2. Enter project details (name, language, voice)
3. Add text to translate or import CSV
4. Click "Generate" to create audio files
5. Use post-processing tools to finalize audio

---

## Features Guide

### Batch Processing

Import CSV files with columns:
- `filename` - Output filename (without extension)
- `text` - Text to convert to speech
- `language` - Language code (e.g., "en-US", "es-ES")
- `voice` - Voice name (optional)

Example CSV:
```csv
filename,text,language,voice
greeting,Welcome to our service,en-US,en-US-Neural2-J
menu,Press one for sales,en-US,en-US-Neural2-J
goodbye,Thank you for calling,en-US,en-US-Neural2-J
```

### Post-Processing

Available tools:
- **Silence Detection**: Automatically remove leading/trailing silence
- **Normalize Audio**: Consistent volume levels
- **Compression**: Reduce dynamic range
- **Format Conversion**: Convert between WAV, MP3, OGG
- **Metadata Editing**: Add title, artist, album info

### AI Text Correction

Use Gemini AI to:
- Fix grammar and spelling
- Improve clarity
- Normalize text for TTS
- Custom prompts for specific improvements

---

## Troubleshooting

### macOS: "App is damaged and can't be opened"

This happens when macOS blocks unsigned apps.

**Solution**:
```bash
xattr -cr "/Applications/clearspeak-v3.app"
```

Then right-click and select "Open".

### Windows: "Windows protected your PC"

This is Windows SmartScreen blocking unsigned applications.

**Solution**:
1. Click "More info"
2. Click "Run anyway"

### TTS API Errors

**"Invalid API key"**:
- Verify your API key is correct
- Check API is enabled in Google Cloud Console
- Ensure billing is enabled (Google requires it)

**"Quota exceeded"**:
- Check your usage in Google Cloud Console
- Upgrade your quota or wait for reset
- Free tier: 1 million characters/month

### Audio Not Playing

- Check your system audio settings
- Verify audio output device is connected
- Try exporting to WAV and playing externally

---

## Privacy & Data

ClearSpeak V3 **DOES NOT**:
- Collect or transmit your personal data
- Track your usage
- Send analytics to servers
- Share data with third parties

All data stays on your computer. API credentials you provide are:
- Stored locally with encryption
- Never transmitted to ClearSpeak servers
- Only sent to services you configure (Google, ElevenLabs)

See `PRIVACY-POLICY.txt` for full details.

---

## License

ClearSpeak V3 is **FREE** software licensed under a proprietary freeware license.

**You MAY**:
- Use for personal projects
- Use for commercial projects
- Install on unlimited computers

**You MAY NOT**:
- Redistribute or resell the software
- Modify or reverse-engineer
- Remove copyright notices

See `LICENSE.txt` for full terms.

**Copyright © 2025 Jonathon McDonald. All rights reserved.**

---

## Support

### Known Issues

- macOS security warnings on first launch (expected behavior)
- Windows SmartScreen warnings (expected for unsigned apps)
- Wine errors during Windows build on Mac (doesn't affect functionality)

### Reporting Issues

This is a learning project released as free software. While I strive for quality, support may be limited.

If you encounter bugs:
1. Check this README for solutions
2. Verify you're using the latest version
3. Include detailed steps to reproduce

### Feature Requests

Feature requests are welcome! However, as this is a learning project provided for free, implementation cannot be guaranteed.

---

## Credits

**Developer**: Jonathon McDonald
**Built With**: Electron, Node.js
**TTS Services**: Google Cloud, ElevenLabs
**AI Services**: Google Gemini

---

## Version History

### 3.17.0 (January 2025) - Free Edition
- Removed Gumroad license activation system
- Made completely free for all users
- Updated license to proprietary freeware
- Added privacy policy
- Improved Gemini API fallback system
- Updated Google Cloud authentication

### 3.16.0 (January 2025)
- Added Gemini API multi-model fallback
- Improved Google Cloud auth
- Fixed Windows UI bugs
- Enhanced stability

---

## FAQ

**Q: Is this really free?**
A: Yes! Completely free for personal and commercial use. No hidden costs, no trials, no subscriptions.

**Q: Why is it free?**
A: This started as a learning project. I'm releasing it free to help others and build my portfolio.

**Q: Do I need Google Cloud to use this?**
A: You need API credentials from Google Cloud or ElevenLabs to generate speech. Both offer free tiers.

**Q: Can I use this for my business?**
A: Yes! Free for commercial use. See LICENSE.txt for restrictions (mainly: don't redistribute).

**Q: Will there be updates?**
A: Maybe! This is a learning project, so updates depend on my availability and interest.

**Q: Can I request features?**
A: Feel free to ask, but implementation isn't guaranteed. This is provided as-is.

**Q: Is my data safe?**
A: Yes. All data stays on your computer. API keys are stored with encryption locally.

**Q: Why do I need to provide my own API keys?**
A: To keep this truly free, I don't run backend servers. You connect directly to TTS providers.

---

**Enjoy ClearSpeak V3!**

Built with ❤️ as a learning journey.
