# 👾 Pacman Contribution Graph — Retro Gaming Meets GitHub

> Transform your GitHub contribution grid into an animated Pacman game with dark and light mode support.

---

## 📖 Overview

The Pacman Contribution Graph converts your GitHub contribution calendar into a fun Pacman animation. Pacman moves across your contribution grid, eating the contribution squares as ghosts chase it. It supports both dark and light color schemes.

---

## ✨ What It Does

- Converts your **contribution grid** into a Pacman animation
- Supports **dark and light mode** with `<picture>` tag
- Generates an **SVG animation** via GitHub Actions
- Updates automatically on a schedule

---

## 🚀 Installation & Setup

### Step 1: Create the Workflow

Create `.github/workflows/pacman.yml` in your profile repository:

```yaml
name: Generate Pacman

on:
  schedule:
    - cron: "0 0 * * *"  # Daily at midnight
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      - name: Generate Pacman SVG
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/pacman-contribution-graph.svg
            dist/pacman-contribution-graph-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Step 2: Run the Workflow

Go to your repository's **Actions** tab and manually trigger the workflow.

### Step 3: Add to Your README

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph.svg">
  <img alt="Pacman Contribution Graph" src="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph.svg">
</picture>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## 💻 Example Code

### Simple (No Dark Mode)
```html
<img src="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph.svg" alt="Pacman Graph"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### With Dark/Light Mode Support
```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph.svg">
  <img alt="Pacman Contribution Graph" src="https://raw.githubusercontent.com/torvalds/torvalds/output/pacman-contribution-graph.svg">
</picture>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## ✅ Pros
- Unique and fun — stands out on any profile
- Dark/light mode support
- Auto-updates via GitHub Actions
- Great conversation starter

## ❌ Cons
- Requires GitHub Actions setup
- Uses Action minutes
- Large SVG file size
- Not everyone may appreciate the gaming aesthetic

## 🎯 Best Use Cases
- Gaming enthusiasts
- Fun-focused profiles
- Standing out from standard profiles
- Retro/cyberpunk themed profiles

---

## 🔗 Official Resources

- **Uses:** [github.com/Platane/snk](https://github.com/Platane/snk) (same tool as Snake Graph)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
