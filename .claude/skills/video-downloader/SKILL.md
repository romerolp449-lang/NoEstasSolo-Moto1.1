---
name: video-downloader
description: Download YouTube videos with flexible quality and format customization. Supports MP4/WebM/MKV formats, quality selection from best to 360p, audio-only extraction as MP3, and custom output directories.
---

# Video Downloader

This skill enables downloading YouTube videos with flexible quality and format customization.

## Key Capabilities

- Quality options ranging from best available down to 360p or worst quality
- Format choices: MP4 (default), WebM, or MKV containers
- Audio extraction functionality that saves as MP3
- Custom output directory specification

## Basic Usage

```bash
python scripts/download_video.py "URL"
```

### Optional Parameters

- Quality: `--quality 1080p` (or best, 720p, 480p, 360p, worst)
- Format: `--format mp4` (or webm, mkv)
- Audio only: `-a` flag
- Output directory: `--output /path/to/dir`

## Notable Features

- Uses yt-dlp which automatically installs itself if not present
- Handles stream merging when necessary
- Files save to `/mnt/user-data/outputs/` by default
- Filenames derived from video titles
- Processes individual videos only (skips playlists automatically)

## Notes

- Higher quality selections may require additional time and storage space
- Audio-only downloads are significantly smaller and faster
- MP4 is recommended for broad compatibility
