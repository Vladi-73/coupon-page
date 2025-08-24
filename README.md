# Coupon and Map Page

This repository contains a one-page website created for a company promotion.

* **Left side:** Image with a discount coupon.
* **Right side:** Interactive map with the location of the enterprise.

# feat(video): implement adaptive streaming with HLS transcoding

## Summary
Enhanced video delivery by converting MP4 source files to adaptive HLS streams using FFmpeg, enabling optimal playback across different network conditions and devices.

## Changes
- Added HLS transcoding pipeline using FFmpeg (v6.1) from official sources ( https://ffmpeg.org/download.html )
- Generated multi-bitrate streams for three quality tiers:
  - 1080p (high quality)
  - 720p (medium quality)
  - 480p (low quality for mobile)
- Implemented adaptive bitrate streaming technology

## Benefits
- 🚀 **Faster loading**: Segmented streaming allows progressive playback
- 📶 **Network adaptation**: Automatic quality adjustment based on connection speed
- 📱 **Device compatibility**: Universal support across modern browsers and devices
- ⚡ **Improved UX**: Smooth playback without buffering interruptions

## Technical Details
- Used FFmpeg with x264 encoding for optimal compression/quality balance
- Created master playlist (.m3u8) with variant streams
- Configured segment duration at 6 seconds for optimal caching
- Maintained original aspect ratio (16:9) across all renditions

Files modified:
- Added video processing script (`scripts/encode_hls.sh`)
- Added output directories for multi-bitrate streams
- Updated documentation (`docs/VIDEO_STREAMING.md`)


## How to view?
The finished page is available at the link: [Open site]( https://vladi-73.github.io/coupon-page/)

