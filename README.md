# Insta Story Gallery

![Insta Story Gallery poster](assets/poster.svg)

Responsive, **local-only** media gallery for photos and videos. No account credentials required, no cloud upload, no backend. Media stays in the browser tab; refreshing the page clears the gallery selection.

> **Status:** Working static gallery, not an Instagram API downloader. Instagram cookies, session tokens, private stories and highlights are **not** imported or accessed. The poster is a concept illustration rather than a screenshot.

## Features

- Add multiple JPG, PNG, WEBP, GIF, MP4 and WEBM files by picker or drag and drop
- Mobile-responsive gallery, image and video viewer, arrow navigation
- Filename search, photos/videos filters and sorting
- Download individual files or export every selected file to ZIP without a backend
- Dark/light theme

## Windows PC (CMD)

Install [Git](https://git-scm.com/downloads) and Python 3, then run:

```bat
git clone https://github.com/RuslanSharifov/insta-story-gallery.git
cd insta-story-gallery
py -m http.server 3000 --bind 127.0.0.1
```

Open **http://127.0.0.1:3000** in your browser. Stop with Ctrl+C. If the `py` launcher is missing, use `python -m http.server 3000 --bind 127.0.0.1`.

## Android (Termux)

Install Termux, then run:

```sh
pkg update && pkg upgrade
pkg install python git
git clone https://github.com/RuslanSharifov/insta-story-gallery.git
cd insta-story-gallery
python -m http.server 3000 --bind 127.0.0.1
```

Open **http://127.0.0.1:3000** using the browser on the same Android device. Stop with Ctrl+C.

## How to use

1. Click **Fayl əlavə et** or drag files onto the drop area.
2. Use **Hamısı**, **Fotolar**, and **Videolar** to filter, or search by file name.
3. Click a thumbnail for a full-screen preview and move between files.
4. Use the download control for one file, or **Hamısını ZIP yüklə** to package all imported media.

## Privacy and limitations

Imported files are handled in the browser using local object URLs. They are not uploaded to any server by this code. This is *not* a persistent media library; reopening or refreshing the page requires selecting files again. Large ZIP exports consume RAM and may be limited by mobile device memory. Never share Instagram cookie or session files; they can grant access to an account.

## Files

- `index.html` – markup and controls
- `styles.css` – responsive design
- `app.js` – browser-local media gallery and ZIP export
- `assets/poster.svg` – README cover artwork

No npm installation or third-party runtime dependencies are required.
