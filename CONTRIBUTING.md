# 🤝 Contributing to GitHub Profile README Guide

Thank you for considering contributing to this project! This repository thrives because of the open source community. Whether you want to add a new tool, submit your profile to the showcase, fix a typo, or improve documentation — every contribution matters.

---

## 📋 Table of Contents

- [How to Contribute](#how-to-contribute)
- [Adding a New Resource or Tool](#adding-a-new-resource-or-tool)
- [Adding an Example Profile](#adding-an-example-profile)
- [Submitting Your Profile to the Showcase](#submitting-your-profile-to-the-showcase)
- [Improving Documentation](#improving-documentation)
- [Pull Request Process](#pull-request-process)
- [Style Guide](#style-guide)
- [Code of Conduct](#code-of-conduct)

---

## 🚀 How to Contribute

1. **Fork** this repository
2. **Clone** your fork locally
   ```bash
   git clone https://github.com/YOUR_USERNAME/github-profile-readme-guide.git
   ```
3. **Create a branch** for your contribution
   ```bash
   git checkout -b feature/add-new-tool
   ```
4. **Make your changes** following the guidelines below
5. **Commit** with a descriptive message
   ```bash
   git commit -m "Add: New tool - ToolName for category"
   ```
6. **Push** to your fork
   ```bash
   git push origin feature/add-new-tool
   ```
7. **Open a Pull Request** against the `main` branch

---

## 🛠 Adding a New Resource or Tool

To add a new resource, update the appropriate file:

| What you're adding | Where to add it |
|---|---|
| A new stats/graph tool | `TOOLS.md` and the relevant `docs/` page |
| A new resource link | `RESOURCES.md` under the correct category |
| A new documentation guide | Create a new file in `docs/` |

### Format for `TOOLS.md`

Add a new row to the comparison table:

```markdown
| Tool Name | Category | ⭐ Beginner | ⭐⭐⭐⭐⭐ | ✅ | [Link](https://example.com) |
```

### Format for `RESOURCES.md`

Add under the correct category heading:

```markdown
- **[Tool Name](https://link.com)** — Brief description of what it does.
```

### Format for `docs/` Pages

If you're creating a new documentation page, follow this template:

```markdown
# 📊 Tool Name — Short Description

> One-line summary of the tool.

## 📖 Overview
## ✨ What It Does
## 🚀 Installation & Setup
## 💻 Example Code
## ✅ Pros
## ❌ Cons
## 🎯 Best Use Cases
## 🔗 Official Resources
```

---

## 👤 Adding an Example Profile

To add a new example profile:

1. Create a new file in `examples/` named `your-persona-profile.md`
2. Include these sections:
   - Hero Banner
   - About section
   - Skills / Tech Stack
   - GitHub Stats
   - Social Links
3. Use realistic, working markdown with placeholder usernames
4. Add a link to your new example in `README.md` under the Examples section

---

## 🌟 Submitting Your Profile to the Showcase

We love seeing how developers use these tools! To add your profile to the showcase:

1. Open `SHOWCASE.md`
2. Add your entry under the appropriate category:
   ```markdown
   | [@yourusername](https://github.com/yourusername) | Brief description of your profile style |
   ```
3. Submit a Pull Request with the title: `Showcase: Add @yourusername`

### Showcase Rules

- Your profile must use at least **2 tools** from this guide
- Your profile must be **public**
- Keep descriptions **under 100 characters**
- No NSFW content

---

## 📝 Improving Documentation

Documentation improvements are always welcome:

- Fix typos and grammar
- Improve clarity of explanations
- Add missing information to existing guides
- Update outdated links or screenshots
- Translate documentation (create a `docs/lang/` directory)

---

## 🔄 Pull Request Process

1. Ensure your changes follow the [Style Guide](#style-guide)
2. Update relevant files if your change affects multiple documents
3. Write a clear PR description explaining:
   - What you changed
   - Why you changed it
   - Any relevant screenshots
4. Link any related issues
5. Wait for review — maintainers will respond within 48 hours

### PR Title Format

```
Add: Brief description          — For new additions
Fix: Brief description          — For bug fixes and corrections
Update: Brief description       — For updates to existing content
Docs: Brief description         — For documentation improvements
Showcase: Add @username         — For showcase submissions
```

---

## 🎨 Style Guide

### Markdown

- Use ATX-style headers (`#`, `##`, `###`)
- Add a blank line before and after headers
- Use fenced code blocks with language identifiers
- Use tables for comparisons and structured data
- Use emojis sparingly but consistently with the rest of the repo

### Links

- Always use descriptive link text (not "click here")
- Prefer HTTPS links
- Test all links before submitting

### Images

- Use alt text for all images
- Prefer SVG for badges and icons
- Keep image widths reasonable (max 800px for screenshots)

### Content

- Write in clear, beginner-friendly language
- Include code examples wherever possible
- Provide both the code and a description of what it does
- Attribute original creators and link to source repositories

---

## 📜 Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).

By participating, you agree to:

- Be respectful and inclusive
- Accept constructive criticism gracefully
- Focus on what's best for the community
- Show empathy toward other community members

---

## 💬 Questions?

If you have questions about contributing, feel free to:

- Open an [Issue](../../issues) with the label `question`
- Start a [Discussion](../../discussions)

---

<div align="center">

**Thank you for making this resource better for everyone! 🙌**

</div>
