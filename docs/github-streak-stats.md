# 🔥 GitHub Streak Stats — Track Your Contribution Streak

> Display your daily GitHub contribution streak, longest streak, and total contributions with a beautiful, customizable card.

---

## 📖 Overview

[GitHub Streak Stats](https://streak-stats.demolab.com) is a popular tool that generates a dynamic card showing your contribution streak on GitHub. Created by [DenverCoder1](https://github.com/DenverCoder1), it motivates developers to maintain consistent coding habits by tracking consecutive days of contributions.

---

## ✨ What It Does

- Shows your **current contribution streak** (consecutive days)
- Displays your **longest streak** (personal record)
- Counts your **total contributions** (lifetime)
- Updates **daily** based on your GitHub activity
- Supports **20+ themes** and custom colors

---

## 🚀 Installation & Setup

### Step 1: Copy the Code

Add this to your GitHub profile README:

```html
<img src="https://streak-stats.demolab.com/?user=torvalds&theme=highcontrast&hide_border=true" alt="GitHub Streak"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Step 2: Replace Username

Change `torvalds` to your actual GitHub username.

### Step 3: Customize (Optional)

Choose a theme and add additional parameters:

```html
<img src="https://streak-stats.demolab.com/?user=torvalds&theme=tokyonight&hide_border=true&border_radius=10" alt="GitHub Streak"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## 💻 Example Code

### Basic Streak Card
```html
<div align="center">
  <img src="https://streak-stats.demolab.com/?user=torvalds&theme=highcontrast" alt="GitHub Streak"/>
</div>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### With Custom Colors
```html
<img src="https://streak-stats.demolab.com/?user=torvalds&background=0D1117&border=0D1117&stroke=00FF9C&ring=00FF9C&fire=FF6600&currStreakNum=FFFFFF&sideNums=FFFFFF&currStreakLabel=00FF9C&sideLabels=00FF9C&dates=888888" alt="Streak Stats"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Compact Layout
```html
<img src="https://streak-stats.demolab.com/?user=torvalds&theme=dark&type=svg&mode=weekly" alt="Weekly Streak"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Alternative (Nirzak Fork)
```html
<img src="https://nirzak-streak-stats.vercel.app/?user=torvalds&theme=tokyonight" alt="GitHub Streak"/>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

### Side by Side with Stats
```html
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=torvalds&show_icons=true&theme=tokyonight&hide_border=true" height="180"/>
  <img src="https://streak-stats.demolab.com/?user=torvalds&theme=tokyonight&hide_border=true" height="180"/>
</div>
```

> 📝 **Note:** Replace `torvalds` with your GitHub username.

---

## 🎨 Customization Options

| Parameter | Type | Default | Description |
|---|---|---|---|
| `user` | string | *required* | Your GitHub username |
| `theme` | string | `default` | Color theme |
| `hide_border` | boolean | `false` | Remove card border |
| `border_radius` | number | `4.5` | Border radius in pixels |
| `background` | string | theme | Background color (hex) |
| `border` | string | theme | Border color |
| `stroke` | string | theme | Stroke line color |
| `ring` | string | theme | Ring color |
| `fire` | string | theme | Fire icon color |
| `currStreakNum` | string | theme | Current streak number color |
| `sideNums` | string | theme | Side numbers color |
| `currStreakLabel` | string | theme | Current streak label color |
| `sideLabels` | string | theme | Side labels color |
| `dates` | string | theme | Date text color |
| `date_format` | string | auto | Custom date format |
| `locale` | string | `en` | Language locale |

### Popular Themes

`default`, `dark`, `highcontrast`, `radical`, `merko`, `gruvbox`, `tokyonight`, `onedark`, `cobalt`, `synthwave`, `dracula`, `prussian`, `monokai`, `vue`, `vue-dark`, `shades-of-purple`, `nightowl`, `buefy`, `blue-green`, `algolia`, `great-gatsby`, `darcula`

---

## ✅ Pros

- **Zero setup time** — Just paste a URL
- **Motivating** — Encourages daily contributions
- **Beautiful design** — Clean, professional look
- **Highly customizable** — Full color and theme control
- **Lightweight** — Loads quickly as an SVG
- **Self-hostable** — Deploy on Vercel for reliability

---

## ❌ Cons

- **Timezone sensitivity** — Streak may reset if timezone is misconfigured
- **Pressure** — Can create unhealthy pressure to commit daily
- **Limited data** — Only shows streak and total, not detailed analytics
- **Rate limits** — Public instance may experience occasional downtime

---

## 🎯 Best Use Cases

- **Building coding habits** — Maintain a daily commitment to coding
- **Portfolio profiles** — Show consistency to potential employers
- **Personal motivation** — Track your progress visually
- **Pairing with GitHub Stats** — Combine with Stats card for a complete picture

---

## 🔗 Official Resources

- **Website:** [streak-stats.demolab.com](https://streak-stats.demolab.com)
- **Repository:** [github.com/DenverCoder1/github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats)
- **Theme Gallery:** [streak-stats themes](https://github.com/DenverCoder1/github-readme-streak-stats/blob/main/docs/themes.md)
- **Alternative (Nirzak):** [nirzak-streak-stats.vercel.app](https://nirzak-streak-stats.vercel.app)

---

<div align="center">

[← Back to Main README](../README.md) · [View All Docs](../README.md#-documentation)

</div>
