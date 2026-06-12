# 🎵 Spotify Now Playing — Music Widget for GitHub

> Display the song you're currently listening to on Spotify directly on your GitHub profile.

---

## 📖 Overview

[Spotify GitHub Profile](https://github.com/kittinan/spotify-github-profile) by [kittinan](https://github.com/kittinan) generates a dynamic widget that shows your currently playing or recently played Spotify track on your GitHub profile.

---

## ✨ What It Does

- Shows your **currently playing** song in real time
- Displays **album cover art**
- Falls back to **recently played** when nothing is active
- Multiple **themes** available
- Updates **automatically**

---

## 🚀 Installation & Setup

### Step 1: Authorize Spotify
Visit [spotify-github-profile.kittinanx.com](https://spotify-github-profile.kittinanx.com/) and click **"Connect with Spotify"** to authorize the app.

### Step 2: Copy Your Embed Code
After authorization, copy the generated image URL.

### Step 3: Add to Your README
```html
<img src="https://spotify-github-profile.kittinanx.com/api/view?uid=YOUR_SPOTIFY_ID&cover_image=true&theme=default&bar_color=53b14f" alt="Spotify Now Playing"/>
```

---

## 💻 Example Code

### Basic Widget
```html
<div align="center">
  <img src="https://spotify-github-profile.kittinanx.com/api/view?uid=YOUR_SPOTIFY_ID&cover_image=true&theme=default" alt="Spotify"/>
</div>
```

### Compact Version
```html
<img src="https://spotify-github-profile.kittinanx.com/api/view?uid=YOUR_SPOTIFY_ID&cover_image=true&theme=compact" alt="Spotify"/>
```

---

## 🎨 Parameters

| Parameter | Description | Options |
|---|---|---|
| `uid` | Your Spotify user ID | Your ID |
| `cover_image` | Show album art | `true`, `false` |
| `theme` | Widget theme | `default`, `compact`, `natemoo-re`, `novatorem` |
| `bar_color` | Progress bar color | Hex color (e.g., `53b14f`) |

---

## ✅ Pros
- Adds personality to your profile
- Shows what you're listening to in real time
- Multiple theme options
- Easy setup with OAuth

## ❌ Cons
- Requires Spotify account
- Shows nothing when not listening (shows last played)
- External service dependency
- Privacy consideration — shows your listening habits

## 🎯 Best Use Cases
- Music lovers and DJs
- Adding personality to your profile
- Creative/design-focused profiles

---

## 🔗 Official Resources

- **Repository:** [github.com/kittinan/spotify-github-profile](https://github.com/kittinan/spotify-github-profile)
- **Website:** [spotify-github-profile.kittinanx.com](https://spotify-github-profile.kittinanx.com/)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
