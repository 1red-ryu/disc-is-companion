# disc.is Companion

An optional Windows app for local MP3 and Soulseek listening rooms on [disc.is](https://disc.is).

## Download

[Windows x64 portable ZIP](https://github.com/1red-ryu/disc-is-companion/releases/download/companion-v0.1.5/disc-is-companion-0.1.5-windows-x64.zip) · [Release notes and checksum](https://github.com/1red-ryu/disc-is-companion/releases/tag/companion-v0.1.5)

This is an unsigned preview. Extract the entire ZIP and open `disc.is-Companion.exe`. Keep the resources and sidecar files together.

Install **FFmpeg and FFprobe** and add them to PATH, or select their paths in the app's Media tools. They are not bundled. MP3 is the supported source format.

## Start a room

1. Sign in to disc.is with a claimed username.
2. Open **Companion → Pair Companion**.
3. Paste the single-use pairing code into Companion.
4. Back on disc.is, open **Companion → Companion settings**, choose a music folder, and scan it. Connect Soulseek there to browse peers. Start a room when ready to queue MP3s.
5. Join it on disc.is and queue a song. Choose Public in room settings for discovery, then share the room link.

Guests can listen to public and unlisted rooms in a browser without signup or a download. DJ controls require a disc.is account.

For SoundCloud, YouTube and Spotify, use **Rooms → Your room → Go live with my music** directly in the browser. Companion is optional for that mode; each service's availability and preview restrictions apply.

## Browse Soulseek

Pair your disc.is account and choose a music folder. On disc.is, open **Companion → Companion settings**, enter your Soulseek account, and confirm sharing. Once the client is connected and your folder is indexed, use **Search** or **Browse files**. Search results include a button to browse the sharing user. You can browse and filter folders and files without a room; this does not download anything. Start a room and explicitly choose **Queue MP3** to play a compatible file there.

**Connection status:** Starting the client is separate from logging in and indexing your music. Wait for **Connected** and a shared-file count before browsing. Large folders index after startup; startup failures stay visible and can be retried.

**Browser controls:** Manage the paired computer from disc.is, including from another device. Private controls use a separate owner-only relay connection with expiring authority and end-to-end encryption. Browsing does not start or stop your listening room. Initial pairing and executable paths are configured in the app.

## What's included

Companion decodes local MP3s and sends one continuous Opus track over WebRTC. It does not record the microphone or desktop audio. The managed Soulseek client starts only after the user supplies an account and agrees to share a folder. Compatible MP3 transfers can begin playing while their sequential download is unfinished.

Queue rules include DJ seat limits, selected/open/random admission, turn order, songs per turn, per-person queue limits and host-only skipping. Keep the computer online while hosting. Closing the Companion window keeps it running in the system tray; use the tray menu to reopen it, open website controls, or quit.

## Source and licenses

The portable ZIP includes Companion application source under `resources/app`, setup/build information in `resources/app/README.md`, and the complete corresponding modified slskd source, original archive, patch, license and notices under `resources/app/runtime/slskd`. See those bundled files for third-party license terms and reproducible build details.

This repository distributes the app and setup notes. The disc.is website repository is separate.

Actual Soulseek peer transfers and physical iPhone acceptance are still pending. There is no installer or automatic updater in this preview.

## Soulseek downloads in your browser

Choose **Soulseek** in the regular disc.is search bar. Results show discs and track information, load more as you scroll, and have a **+** button to save an audio file to your device. Keep Companion online and Soulseek connected; no live room is needed.

Downloads travel through the paired computer over your private encrypted connection. Browsers with a Save picker support files up to 512 MiB; other browsers, including iPhone Safari, support up to 64 MiB. MP3 remains the format supported for room broadcasts.

Set a custom **disc.is/r/your-room** link under **Rooms → Your room → Room URL**. Old room links keep working.

## Listen while a track downloads

With Companion 0.1.5, click an MP3 disc in the regular disc.is Soulseek search. It opens a temporary large disc and plays once enough peer audio arrives, without creating a room. Pause, resume and volume use the normal site controls; return to the same search results with Back. **+** separately saves the original file to your browser.

Companion decodes the growing MP3 and sends bounded audio chunks over your private encrypted connection. Keep your computer and Soulseek online. Preview supports MP3s with known duration up to one hour and size up to 250 MB; seeking is unavailable during progressive preview. Other supported formats remain downloadable. If your browser tab is hosting a provider room, use another tab for private previews.
