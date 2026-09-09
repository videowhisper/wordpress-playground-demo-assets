# Broadcast Live Video Playground demo assets

This package provides six static, offline-only channel snapshots for the
Broadcast Live Video WordPress Playground preview. It is deliberately separate
from the plugin ZIP and WordPress.org SVN assets directory.

The preview downloads proportional listing thumbnails and full-size channel
previews. Broadcast Live Video uses the listing files at
`uploadsPath/_thumbs/<channel-title>.jpg` and its Playground-only channel view
uses `uploadsPath/_previews/<channel-title>.jpg`. No image processing, FFmpeg,
stream server, camera connection, WebRTC session, or player is used at runtime.

## Asset contract

| Location | Purpose | Format |
| --- | --- | --- |
| `images/originals/*.jpg` | Original static channel snapshot | 1536×1024 JPEG, sRGB |
| `images/thumbnails/*.jpg` | Channel-listing files | 320×213 JPEG, proportionally resized from the original (no crop) |

The public blueprint must use `raw.githubusercontent.com` URLs pinned to an
immutable commit SHA, with Playground networking explicitly enabled. Never use
the mutable `main` branch URL. New images require a fresh commit, a boot test,
and an explicit blueprint SHA update in the consuming plugin.

## Safety and visual requirements

The six scenes show only offline, unbranded, general-audience settings. They
contain no people, text, brands, watermarks, copyrighted characters, dangerous
activity, sensitive content, real surveillance footage, stream UI, or playback
claims. The preview labels its fixtures `Offline` and must not imply that video
delivery works in Playground.
