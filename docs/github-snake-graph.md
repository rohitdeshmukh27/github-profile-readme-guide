# 🐍 Snake Contribution Graph — Animated Snake on Your GitHub Profile

> Transform your GitHub contribution grid into an animated snake game where the snake eats your contributions.

---

## 📖 Overview

[Platane/snk](https://github.com/Platane/snk) generates an SVG animation of a snake moving across your GitHub contribution graph. The snake eats contribution squares as it moves, creating a fun and eye-catching animation. It's one of the most popular animated elements for GitHub profiles.

---

## ✨ What It Does

- Animates a **snake** eating your contribution grid squares
- Supports **dark and light mode** via `<picture>` tag
- Generates **SVG and GIF** output formats
- Runs via **GitHub Actions** on a schedule
- Auto-updates daily with your latest contributions

---

## 🚀 Installation & Setup

### Step 1: Create the Workflow

Create `.github/workflows/snake.yml` in your profile repository:

```yaml
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"  # Runs daily at midnight
  workflow_dispatch:       # Allows manual trigger

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      - name: Generate Snake SVG
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Step 2: Run the Workflow

1. Go to your repository → **Actions** tab
2. Select the **"Generate Snake"** workflow
3. Click **"Run workflow"**
4. Wait for it to complete

### Step 3: Add to Your README

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake.svg"/>
  <img alt="Snake animation" src="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake.svg"/>
</picture>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## 💻 Example Code

### Simple (No Dark Mode)
```html
<img src="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake.svg" alt="Snake Animation"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### With Dark/Light Mode
```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake.svg"/>
  <img alt="Snake animation" src="https://raw.githubusercontent.com/torvalds/torvalds/output/github-snake.svg"/>
</picture>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## ✅ Pros
- Extremely popular and recognizable
- Fun and engaging animation
- Dark/light mode support
- Auto-updates via GitHub Actions

## ❌ Cons
- Requires GitHub Actions (slightly complex setup)
- Uses GitHub Actions minutes
- SVG file can be large
- Takes a few minutes to generate

## 🎯 Best Use Cases
- Adding a fun, animated element to your profile
- Making your profile memorable
- Showcasing contribution activity creatively

---

## 🔗 Official Resources

- **Repository:** [github.com/Platane/snk](https://github.com/Platane/snk)
- **Demo:** [platane.github.io/snk](https://platane.github.io/snk/)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
