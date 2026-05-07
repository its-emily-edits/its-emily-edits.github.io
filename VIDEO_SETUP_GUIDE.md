# Video Setup Guide

## Overview

Your portfolio now uses **direct video embeds** with HTML5 video players, similar to the reference site you provided. Videos show thumbnails, auto-play previews on hover, and display engagement metrics (likes, views, comments, shares).

## How It Works

### 1. Video Card Structure

Each work card needs these `data-` attributes:

```html
<button class="work-card"
        data-platform="tiktok"
        data-video="path/to/video.mp4"
        data-thumb="path/to/thumbnail.jpg"
        data-likes="12.5K"
        data-views="245K"
        data-comments="89"
        data-shares="234">
  <!-- Card content -->
</button>
```

### 2. Required Attributes

- **`data-platform`**: `"tiktok"` or `"instagram"` (for display styling)
- **`data-video`**: Path to your video file (MP4 recommended)
- **`data-thumb`**: Path to thumbnail image (JPG/PNG, 1080x1920 ideal)

### 3. Optional Attributes (Engagement Stats)

- **`data-likes`**: e.g., `"12.5K"`, `"1.2M"`
- **`data-views`**: e.g., `"245K"`
- **`data-comments`**: e.g., `"89"`
- **`data-shares`**: e.g., `"234"`

## Features

### ✨ Card Preview (Hover)
- Video auto-plays on mouse hover
- Video pauses when mouse leaves
- Muted playback with loop

### 🎬 Modal Player (Click)
- Full-screen video player opens
- Shows engagement stats overlay
- Video controls enabled
- Auto-plays when opened

### 📊 Engagement Stats
- Displayed on card hover
- Shows in modal overlay
- Icons for likes, views, comments, shares
- Formatted numbers (e.g., "12.5K")

## File Organization

Create a `videos/` folder in your project:

```
ItsEmilyEditsPortfolio/
├── index.html
├── rates.html
├── videos/
│   ├── sample1.mp4
│   ├── sample1-thumb.jpg
│   ├── sample2.mp4
│   ├── sample2-thumb.jpg
│   └── ...
```

## Example: Complete Work Card

```html
<button class="work-card"
        data-platform="instagram"
        data-video="videos/my-reel.mp4"
        data-thumb="videos/my-reel-thumb.jpg"
        data-likes="8.2K"
        data-views="156K"
        data-comments="124">
  <div class="placeholder"><span class="placeholder-text">Loading...</span></div>
  <div class="play-btn">
    <svg width="11" height="11" viewBox="0 0 10 10">
      <path d="M0 0L10 5L0 10Z"/>
    </svg>
  </div>
  <div class="work-info">
    <div class="work-brand">
      <svg class="platform-icon" viewBox="0 0 24 24">
        <!-- Instagram icon SVG path -->
      </svg>
      Personal · 3D printing
    </div>
    <div class="work-title">Making whimsical things</div>
    <div class="video-stats">
      <span>
        <svg viewBox="0 0 24 24">
          <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
        </svg>
        8.2K
      </span>
      <span>
        <svg viewBox="0 0 24 24">
          <path d="M12 4.5C7 4.5 2.73 7.61 1 12c1.73 4.39 6 7.5 11 7.5s9.27-3.11 11-7.5c-1.73-4.39-6-7.5-11-7.5zM12 17c-2.76 0-5-2.24-5-5s2.24-5 5-5 5 2.24 5 5-2.24 5-5 5zm0-8c-1.66 0-3 1.34-3 3s1.34 3 3 3 3-1.34 3-3-1.34-3-3-3z"/>
        </svg>
        156K
      </span>
      <span>
        <svg viewBox="0 0 24 24">
          <path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm0 14H6l-2 2V4h16v12z"/>
        </svg>
        124
      </span>
    </div>
  </div>
</button>
```

## Getting Your Video Files

### Option 1: Download from Social Media
1. Use a downloader tool to get MP4 files from TikTok/Instagram
2. Extract a frame for the thumbnail or use the platform's thumbnail

### Option 2: Upload Original Files
1. Use your original video files (.mp4, .mov)
2. Create thumbnails from the video (first frame or custom)
3. Optimize for web (compress if needed)

## Video Optimization Tips

- **Format**: MP4 (H.264 codec)
- **Resolution**: 1080x1920 (9:16 aspect ratio)
- **File Size**: Under 10MB for fast loading
- **Thumbnails**: JPG, 1080x1920, optimized

## Quick Start Checklist

1. ✅ Create `videos/` folder
2. ✅ Add your video files (.mp4)
3. ✅ Create thumbnail images (.jpg)
4. ✅ Update work card with `data-video` and `data-thumb` paths
5. ✅ Add engagement stats (optional)
6. ✅ Test: hover for preview, click for full player

## Current Status

Your index.html now has:
- ✅ Video preview on hover
- ✅ Full modal player with controls
- ✅ Engagement stats display
- ✅ One example card configured (line 519)

## Next Steps

1. Add your video files to a `videos/` folder
2. Update the remaining work cards with actual video paths
3. Add engagement statistics to each card
4. Test in browser to see videos load and play

The placeholders will show until you add the actual video files!
