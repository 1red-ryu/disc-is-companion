# disc.is Companion

An optional Windows app for local MP3 and Soulseek listening rooms on [disc.is](https://disc.is).

## Download

[Windows x64 portable ZIP](https://github.com/1red-ryu/disc-is-companion/releases/download/companion-v0.1.0/disc-is-companion-0.1.0-windows-x64.zip) · [Release notes and checksum](https://github.com/1red-ryu/disc-is-companion/releases/tag/companion-v0.1.0)

This is an unsigned preview. Extract the entire ZIP and open `disc.is-Companion.exe`. Keep the resources and sidecar files together.

Install **FFmpeg and FFprobe** and add them to PATH, or select their paths in the app's Media tools. They are not bundled. MP3 is the supported source format.

## Start a room

1. Sign in to disc.is with a claimed username.
2. Open **Rooms → Room settings / companion → Use companion instead**.
3. Paste the single-use pairing code into Companion.
4. Choose a music folder, scan MP3s, and start the room.
5. Join it on disc.is and queue a song. Choose Public in room settings for discovery, then share the room link.

Guests can listen to public and unlisted rooms in a browser without signup or a download. DJ controls require a disc.is account.

For SoundCloud, YouTube and Spotify, use **Rooms → Start public room** directly in the browser. Companion is optional for that mode; each service's availability and preview restrictions apply.

## What's included

Companion decodes local MP3s and sends one continuous Opus track over WebRTC. It does not record the microphone or desktop audio. The managed Soulseek client starts only after the user supplies an account and agrees to share a folder. Compatible MP3 transfers can begin playing while their sequential download is unfinished.

Queue rules include DJ seat limits, selected/open/random admission, turn order, songs per turn, per-person queue limits and host-only skipping. Keep the app open while hosting.

## Source and licenses

The portable ZIP includes Companion application source under `resources/app`, setup/build information in `resources/app/README.md`, and the complete corresponding modified slskd source, original archive, patch, license and notices under `resources/app/runtime/slskd`. See those bundled files for third-party license terms and reproducible build details.

This repository distributes the app and setup notes. The disc.is website repository is separate.

Actual Soulseek peer transfers and physical iPhone acceptance are still pending. There is no installer or automatic updater in this preview.
