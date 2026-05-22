# 🎵 JioSaavn API (Unofficial)

A fast and lightweight unofficial JioSaavn API built with Python and Flask.  
Search songs directly by name or fetch complete details using JioSaavn song, album, or playlist links.

[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/amjadimdad00/JioSaavnAPI)
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.png?v=103)](./LICENSE)


---

## ✨ Features

The API can return detailed song information in JSON format, including:

- Song Title
- Artist / Singer Names
- Album Information
- Album URL
- Song Duration
- High Resolution Thumbnail
- Language
- Direct Audio URL
- Release Year
- Lyrics Support
- Album Artwork
- Playlist & Album Parsing
- Search by Song Name
- Much More...

---

## 📦 Sample Response

```json
{
  "320kbps": "true",
  "album": "Guzaarishein (From 'Parwarish') (Original Motion Picture Soundtrack)",
  "album_url": "https://www.jiosaavn.com/album/guzaarishein-from-parwarish-original-motion-picture-soundtrack/b,BYi6A-pHI_",
  "albumid": "64795627",
  "artistMap": {
    "Alistair Alvin": "3423920",
    "Samar Jafri": "18649856"
  },
  "cache_state": "false",
  "copyright_text": "\u00a9 2025 ARY Digital",
  "disabled": "true",
  "disabled_text": "Pro Only",
  "duration": "211",
  "encrypted_drm_media_url": "ID2ieOjCrwdjlkMElYlzWCptgNdUpWD8L+yDWMSNt/DKqZFilDvYERevNyOJmcZUi5Jb549oJSKMkNoLVaobJI92mytrdt3FDnQW0nglPS4=",
  "encrypted_media_path": "NMKyboFo/Fi0VFqJf5Q3Rw==",
  "encrypted_media_url": "ID2ieOjCrwfgWvL5sXl4B1ImC5QfbsDy/OtH00bt4oxVKh8JmVdqXkhg2pBNl0z4fHHafPU9nbIFgouaDPeEORw7tS9a8Gtq",
  "explicit_content": 0,
  "featured_artists": "",
  "featured_artists_id": "",
  "has_lyrics": "false",
  "id": "N0rmlun0",
  "image": "https://c.saavncdn.com/821/Guzaarishein-From-Parwarish-Original-Motion-Picture-Soundtrack-Urdu-2025-20250521185818-500x500.jpg",
  "is_dolby_content": false,
  "is_drm": 1,
  "label": "Ary Digital",
  "label_id": "359201",
  "label_url": "/label/ary-digital-albums/,HIIV-pkHbY_",
  "language": "urdu",
  "lyrics": null,
  "lyrics_snippet": "",
  "media_preview_url": "https://preview.saavncdn.com/821/04343a9815038f8c357019a0959e1022_96_p.mp4",
  "media_url": "https://aac.saavncdn.com/821/04343a9815038f8c357019a0959e1022_320.mp4",
  "music": "",
  "music_id": "",
  "origin": "none",
  "perma_url": "https://www.jiosaavn.com/song/guzaarishein-from-parwarish-original-motion-picture-soundtrack/PlgZXBhFWQM",
  "play_count": 375253,
  "primary_artists": "Samar Jafri, Alistair Alvin",
  "primary_artists_id": "18649856, 3423920",
  "release_date": "2025-05-20",
  "rights": {
  "cacheable": true,
  "code": 1,
    "delete_cached_object": false,
    "reason": "Pro Only"
  },
  "singers": "Samar Jafri, Alistair Alvin",
  "song": "Guzaarishein (From 'Parwarish') (Original Motion Picture Soundtrack)",
  "starred": "false",
  "starring": "",
  "triller_available": false,
  "type": "",
  "webp": true,
  "year": "2025"
}
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/amjadimdad00/JioSaavnAPI.git
```

## 2. Move into the Project Folder

```bash
cd JioSaavnAPI
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Run the Server

```bash
python app.py
```

The API will start locally at:

```bash
http://127.0.0.1:5000
```

---

# 🔥 API Endpoints

## Universal Endpoint

Supports:
- Song Search
- Song Links
- Album Links
- Playlist Links

```http
GET /result/?query=<song-name-or-jiosaavn-link>&lyrics=true
```

### Example

```bash
http://127.0.0.1:5000/result/?query=alone
```

---

## Song Endpoint

Fetch details using a JioSaavn song URL.

```http
GET /song/?query=<jiosaavn-song-link>&lyrics=true
```

### Example

```bash
http://127.0.0.1:5000/song/?query=https://www.jiosaavn.com/song/khairiyat/PwAFSRNpAWw
```

---

## Playlist Endpoint

Fetch all songs from a playlist.

```http
GET /playlist/?query=<playlist-link>&lyrics=true
```

### Example

```bash
http://127.0.0.1:5000/playlist/?query=https://www.jiosaavn.com/featured/romantic-hits-2020---hindi/ABiMGqjovSFuOxiEGmm6lQ__
```

---

## Album Endpoint

Fetch complete album data.

```http
GET /album/?query=<album-link>&lyrics=true
```

### Example

```bash
http://127.0.0.1:5000/album/?query=https://www.jiosaavn.com/album/chhichhore/V4F3M5,cNb4_
```

---

## Lyrics Endpoint

Fetch lyrics using either:
- Song URL
- Song ID

```http
GET /lyrics/?query=<song-url-or-id>
```

### Example

```bash
http://127.0.0.1:5000/lyrics/?query=https://www.jiosaavn.com/song/khairiyat/PwAFSRNpAWw
```

---

# ⚡ Optional Lyrics Support

Add:

```bash
&lyrics=true
```

to any request if you want lyrics included in the response.

> Note: Enabling lyrics may slightly increase response time.

---

# 🌍 Deployment

You can deploy this API on:

- VPS
- Render
- Railway
- Heroku
- Any Python Hosting Platform

### Recommended

Use an Indian VPS/server for better accuracy and availability of songs.

---

# 🛠 Built With

- Python
- Flask
- Requests
- BeautifulSoup

---

<p align="center"> Made with 💖 by <a href="https://linkedin.com/in/amjadimdad" target="_blank"><b>Amjad Imdad</b></a><br> ✨ Star this repo if you found it useful! ✨<br> <sub>Contributions, feedback & PRs are always welcome 🚀</sub> </p>