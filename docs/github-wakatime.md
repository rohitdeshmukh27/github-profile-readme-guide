# ⏱ WakaTime — Coding Activity Stats for GitHub

> Track your coding activity automatically and display daily coding hours, languages, editors, and productivity stats on your GitHub profile.

---

## 📖 Overview

[WakaTime](https://wakatime.com) is a coding activity tracker that integrates with your code editor. Combined with the [waka-readme-stats](https://github.com/anmol098/waka-readme-stats) GitHub Action, it automatically updates your profile with detailed coding statistics.

---

## ✨ What It Does

- Tracks **daily and weekly coding hours**
- Shows **languages used** with percentages
- Displays **editor and OS** statistics
- Shows **most productive times**
- Auto-updates via **GitHub Actions**

---

## 🚀 Installation & Setup

### Step 1: Create a WakaTime Account
Sign up at [wakatime.com](https://wakatime.com) and install the plugin for your code editor (VS Code, IntelliJ, Vim, etc.).

### Step 2: Get Your API Key
Go to [wakatime.com/settings/api-key](https://wakatime.com/settings/api-key) and copy your API key.

### Step 3: Add Secrets to Your Repository
In your profile repository settings, add these secrets:
- `WAKATIME_API_KEY` — Your WakaTime API key
- `GH_TOKEN` — A GitHub personal access token with `repo` scope

### Step 4: Add Section Markers to README
```markdown
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->
```

### Step 5: Create the Workflow
Create `.github/workflows/wakatime.yml`:

```yaml
name: WakaTime Stats
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
```

---

## 💻 Example Output

```
📊 Weekly Development Breakdown

💬 Programming Languages:
TypeScript    12 hrs 30 mins  ██████████░░░░░░  45.2%
Python         8 hrs 15 mins  ██████░░░░░░░░░░  29.8%
JavaScript     4 hrs 20 mins  ███░░░░░░░░░░░░░  15.7%
CSS            1 hr 30 mins   █░░░░░░░░░░░░░░░   5.4%
Other          1 hr 5 mins    █░░░░░░░░░░░░░░░   3.9%

🔥 Editors:
VS Code       26 hrs 40 mins  ████████████████  100.0%

💻 Operating System:
Mac           26 hrs 40 mins  ████████████████  100.0%
```

---

## ✅ Pros
- Automatic tracking — no manual input
- Detailed breakdowns (languages, editors, OS, projects)
- Motivates productivity
- Supports 50+ code editors

## ❌ Cons
- Requires editor plugin installation
- Free tier has limited history (2 weeks)
- Requires GitHub Actions setup
- API key management needed

## 🎯 Best Use Cases
- Developers who want to show productivity
- Tracking coding habits
- Portfolio showcase

---

## 🔗 Official Resources

- **WakaTime:** [wakatime.com](https://wakatime.com)
- **GitHub Action:** [github.com/anmol098/waka-readme-stats](https://github.com/anmol098/waka-readme-stats)
- **Editor Plugins:** [wakatime.com/plugins](https://wakatime.com/plugins)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
