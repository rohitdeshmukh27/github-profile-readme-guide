# 📊 GitHub Readme Stats — Dynamic GitHub Statistics for Your Profile

> Display your GitHub activity stats beautifully with dynamically generated cards showing stars, commits, PRs, issues, and contribution rank.

---

## 📖 Overview

[GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats) is the most popular tool for adding dynamic statistics to your GitHub profile README. Created by [Anurag Hazra](https://github.com/anuraghazra), it generates SVG images that display your GitHub activity in real time.

With over **70,000 stars** on GitHub, it's the go-to solution used by millions of developers worldwide for GitHub profile customization.

---

## ✨ What It Does

- Displays your **total stars**, **commits**, **PRs**, **issues**, and **contribution rank**
- Shows your **most used programming languages** across repositories
- Generates **repository pin cards** for featured projects
- Integrates with **WakaTime** for coding activity stats
- Supports **30+ themes** and extensive customization
- Updates automatically based on your GitHub activity

---

## 🚀 Installation & Setup

### Step 1: Choose Your Card Type

GitHub Readme Stats offers several card types:

1. **Stats Card** — Overall GitHub statistics
2. **Top Languages Card** — Most used programming languages
3. **Repository Card** — Featured repository pins
4. **WakaTime Card** — Coding activity (requires WakaTime)

### Step 2: Add to Your README

Copy the code below and replace `torvalds` with your GitHub username:

**Stats Card:**
```html
<img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

**Top Languages Card:**
```html
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=torvalds&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

**Repository Card:**
```html
<img src="https://github-readme-stats.vercel.app/api/pin/?username=torvalds&repo=REPO_NAME&theme=tokyonight&hide_border=true" alt="Repo Card"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Step 3: Customize

Add parameters to customize the appearance. See the customization options below.

---

## 💻 Example Code

### Basic Stats Card
```html
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight" alt="GitHub Stats"/>
</div>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Stats + Languages Side by Side
```html
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight&hide_border=true" height="180"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=torvalds&layout=compact&theme=tokyonight&hide_border=true" height="180"/>
</div>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Custom Colors
```html
<img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&bg_color=0D1117&title_color=00FF9C&text_color=FFFFFF&icon_color=00FF9C&hide_border=true" alt="Custom Stats"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Hide Specific Stats
```html
<img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight&hide=issues,contribs" alt="Stats"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Include Private Contributions
```html
<img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight&count_private=true" alt="Stats"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## 🎨 Popular Themes

| Theme | Description |
|---|---|
| `default` | Light theme with blue accents |
| `dark` | Simple dark background |
| `tokyonight` | Dark blue with cyan accents |
| `dracula` | Dark purple theme |
| `radical` | Pink and purple gradient |
| `merko` | Dark green theme |
| `gruvbox` | Warm retro colors |
| `onedark` | Atom One Dark theme |
| `cobalt` | Dark blue cobalt |
| `synthwave` | Retro synthwave neon |
| `highcontrast` | Black with bright colors |
| `github_dark` | GitHub's dark mode |

### All Available Parameters

| Parameter | Type | Default | Description |
|---|---|---|---|
| `username` | string | *required* | Your GitHub username |
| `show_icons` | boolean | `false` | Show icons next to stats |
| `theme` | string | `default` | Color theme |
| `hide_border` | boolean | `false` | Remove card border |
| `bg_color` | string | theme default | Background color (hex) |
| `title_color` | string | theme default | Title text color |
| `text_color` | string | theme default | Body text color |
| `icon_color` | string | theme default | Icon color |
| `hide` | string | none | Comma-separated stats to hide |
| `count_private` | boolean | `false` | Include private contributions |
| `hide_rank` | boolean | `false` | Hide the rank circle |
| `line_height` | number | `25` | Line height between stats |
| `custom_title` | string | auto | Custom card title |
| `cache_seconds` | number | `14400` | Cache duration (min 7200) |
| `locale` | string | `en` | Language locale |

---

## ✅ Pros

- **Easy setup** — Just paste a URL, no configuration needed
- **Highly customizable** — Colors, themes, layouts, and content
- **Auto-updating** — Stats refresh automatically
- **Multiple card types** — Stats, languages, repos, WakaTime
- **Well maintained** — Active community with 70k+ stars
- **Self-hostable** — Deploy your own instance on Vercel for reliability

---

## ❌ Cons

- **Rate limiting** — The public Vercel instance can hit GitHub API limits during peak times
- **Cache delay** — Stats may take several hours to update (default 4-hour cache)
- **Language accuracy** — Top Languages is based on repository code, not actual usage
- **No real-time data** — Uses cached GitHub API data, not live statistics

---

## 🎯 Best Use Cases

- **Job seekers** — Show your GitHub activity to potential employers
- **Open source contributors** — Display your contribution stats prominently
- **Portfolio profiles** — Add professional statistics to your developer portfolio
- **Everyone** — This is an essential tool for any GitHub profile customization

---

## 🔗 Official Resources

- **Repository:** [github.com/anuraghazra/github-readme-stats](https://github.com/anuraghazra/github-readme-stats)
- **Theme Gallery:** [github-readme-stats themes](https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md)
- **Demo:** [github-readme-stats.vercel.app](https://github-readme-stats.vercel.app)
- **Self-Hosting Guide:** [Vercel deployment docs](https://github.com/anuraghazra/github-readme-stats#deploy-on-your-own)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
