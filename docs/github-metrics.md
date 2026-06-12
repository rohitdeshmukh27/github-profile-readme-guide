# 📊 GitHub Metrics — Advanced Profile Analytics

> The most powerful and customizable GitHub profile visualization tool with 30+ plugins for detailed analytics and beautiful infographics.

---

## 📖 Overview

[GitHub Metrics](https://github.com/lowlighter/metrics) by [lowlighter](https://github.com/lowlighter) is the most feature-rich GitHub profile analytics tool available. It generates detailed SVG infographics using GitHub Actions, offering 30+ plugins that cover everything from language breakdowns to coding habits, achievements, and social stats.

With **13,000+ stars**, it's the go-to choice for developers who want advanced, detailed profile analytics beyond what simpler tools offer.

---

## ✨ What It Does

- 📊 **Languages** — Detailed programming language breakdown
- 🏆 **Achievements** — Milestone badges and achievements
- 📦 **Repositories** — Repository statistics and highlights
- 📅 **Activity** — Contribution calendar and activity feed
- 👥 **Followers** — Follower analytics and growth
- ⏰ **Habits** — Coding habits (active hours, days, etc.)
- ⭐ **Stars** — Star history and starred repos
- 🎭 **And 30+ more plugins** — Music, anime, chess, tweets, etc.

---

## 🚀 Installation & Setup

> **Note:** GitHub Metrics requires a GitHub Actions workflow, making it more complex to set up than URL-based tools. The extra effort is worth it for the advanced analytics.

### Step 1: Create a GitHub Token

1. Go to [GitHub Settings → Developer Settings → Personal Access Tokens](https://github.com/settings/tokens)
2. Click **"Generate new token (classic)"**
3. Give it a descriptive name (e.g., `metrics-token`)
4. Select these scopes: `repo`, `read:user`, `read:org`
5. Generate and copy the token

### Step 2: Add the Token to Your Repository

1. Go to your profile repository (`username/username`)
2. Navigate to **Settings → Secrets and variables → Actions**
3. Click **"New repository secret"**
4. Name: `METRICS_TOKEN`
5. Value: Paste your token

### Step 3: Create the Workflow File

Create `.github/workflows/metrics.yml` in your profile repository:

```yaml
name: Metrics
on:
  schedule: [{cron: "0 0 * * *"}]  # Runs daily at midnight
  workflow_dispatch:  # Allows manual trigger
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: torvalds
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Kolkata
          
          # Languages plugin
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_limit: 8
          plugin_languages_sections: most-used
          
          # Achievements plugin
          plugin_achievements: yes
          plugin_achievements_display: detailed
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: C
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Step 4: Run the Workflow

1. Go to your repository's **Actions** tab
2. Click **"Metrics"** workflow
3. Click **"Run workflow"**

### Step 5: Add to Your README

```html
<img src="github-metrics.svg" alt="GitHub Metrics"/>
```

---

## 💻 Example Configurations

### Minimal Setup
```yaml
- uses: lowlighter/metrics@latest
  with:
    token: ${{ secrets.METRICS_TOKEN }}
    user: torvalds
    template: classic
    base: header, activity, community, repositories
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Full Featured
```yaml
- uses: lowlighter/metrics@latest
  with:
    token: ${{ secrets.METRICS_TOKEN }}
    user: torvalds
    template: classic
    base: header, activity, community, repositories, metadata
    
    plugin_languages: yes
    plugin_languages_limit: 8
    
    plugin_achievements: yes
    plugin_achievements_display: detailed
    
    plugin_isocalendar: yes
    plugin_isocalendar_duration: half-year
    
    plugin_habits: yes
    plugin_habits_days: 14
    plugin_habits_facts: yes
    
    plugin_lines: yes
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Multiple Output Files
```yaml
# Generate separate SVG files for different sections
- uses: lowlighter/metrics@latest
  with:
    token: ${{ secrets.METRICS_TOKEN }}
    filename: header.svg
    base: header
    
- uses: lowlighter/metrics@latest
  with:
    token: ${{ secrets.METRICS_TOKEN }}
    filename: languages.svg
    base: ""
    plugin_languages: yes
```

---

## 🔌 Popular Plugins

| Plugin | Description |
|---|---|
| `languages` | Programming languages breakdown |
| `achievements` | GitHub milestones and achievements |
| `isocalendar` | Isometric contribution calendar |
| `habits` | Coding habits analysis |
| `lines` | Lines of code added/removed |
| `stars` | Star history |
| `topics` | Topic interests |
| `reactions` | Reaction statistics |
| `people` | Follower/following analysis |
| `discussions` | Discussion participation |
| `notable` | Notable contributions |
| `music` | Recently played music |
| `activity` | Recent activity feed |

---

## ✅ Pros

- **Most powerful** — Unmatched depth of analytics
- **Highly customizable** — 30+ plugins with extensive options
- **Beautiful output** — Professional SVG infographics
- **Multiple templates** — Classic, repository, terminal, markdown
- **Active development** — Regularly updated with new features
- **No external dependencies** — Runs entirely in GitHub Actions

---

## ❌ Cons

- **Complex setup** — Requires GitHub Actions knowledge
- **Longer setup time** — 15-30 minutes vs. 2 minutes for simpler tools
- **Token management** — Requires a personal access token
- **Action minutes** — Uses GitHub Actions compute time
- **SVG size** — Generated files can be large with many plugins enabled

---

## 🎯 Best Use Cases

- **Advanced users** — Developers who want detailed, comprehensive analytics
- **Portfolio showcase** — Maximum visual impact for professional profiles
- **Data enthusiasts** — Developers who love data visualization
- **Open source maintainers** — Showcase contribution depth

---

## 🔗 Official Resources

- **Repository:** [github.com/lowlighter/metrics](https://github.com/lowlighter/metrics)
- **Documentation:** [metrics.lecoq.io](https://metrics.lecoq.io)
- **Plugin Gallery:** [Metrics Plugin List](https://github.com/lowlighter/metrics#-plugins)
- **Examples:** [Metrics Examples](https://github.com/lowlighter/metrics/blob/master/.github/readme/partials/documentation/setup/examples.md)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
