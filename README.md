<p align="center">
  <img src="https://raw.githubusercontent.com/rocke3/npm-manager/main/img/logo.png" alt="NPM Manager" width="128" height="128" />
</p>

<h1 align="center">NPM Manager</h1>

![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/MdRashid.npm-manager)
![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/MdRashid.npm-manager)
![Visual Studio Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/MdRashid.npm-manager)

**NPM Manager** is a powerful Visual Studio Code extension that gives you a beautiful, intuitive visual interface to manage all your project dependencies — without ever touching the terminal.

Supports **npm**, **yarn**, **pnpm**, and **bun**.

---

## 🖼️ Preview

![Preview](https://raw.githubusercontent.com/rocke3/npm-manager/main/img/preview.webp)

---

<table>
<tr>
<td width="110" align="center" valign="middle">
<a href="https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom?utm_source=item-share-cb">
<img src="https://raw.githubusercontent.com/rocke3/npm-manager/main/img/TabAutoPilot.png" alt="TabAutoPilot" width="88" height="88" />
</a>
</td>
<td valign="middle">

#### 🚀 Try TabAutoPilot &nbsp;·&nbsp; <sub>AI Tab Organizer for Chrome</sub>

**Drowning in tabs?** A free Chrome extension by the same author — auto-groups tabs by topic, removes duplicates, hibernates inactive ones, and saves sessions as workspaces. 100% on-device, no tracking.

<a href="https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom?utm_source=item-share-cb"><img src="https://img.shields.io/badge/Install%20for%20Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Install for Chrome" /></a> &nbsp; <img src="https://img.shields.io/badge/Free-00C853?style=for-the-badge" alt="Free" /> &nbsp; <img src="https://img.shields.io/badge/On--device-FF6B35?style=for-the-badge" alt="On-device" />

</td>
</tr>
</table>

---

## ✨ Features

### 📊 Dashboard & Overview

- 🖥️ **Visual Dashboard** — Clean webview panel showing all your dependencies and devDependencies at a glance
- 🌳 **Sidebar Tree View** — Quick-access tree in the activity bar with colored status indicators (✅ up-to-date, 🟡 outdated)
- ℹ️ **Environment Info Bar** — See your project name, version, Node.js version, package manager version, and `node_modules` size — all in one place
- 🔢 **Stats Cards** — Interactive stat cards showing total packages, up-to-date count, available updates, and vulnerabilities — click any card to filter the table

### 🚀 Smart Upgrades

- 🎨 **Color-Coded Update Buttons** — Instantly see the impact of each update:
  - 🟢 Green = patch (bug fixes — safe to update)
  - 🟠 Amber = minor (new features — backward compatible)
  - 🔴 Coral = major (breaking changes — review docs first)
- 💬 **Hover Tooltips** — Hover any upgrade button to see a contextual hint with icon and description of the update type
- ⚡ **Update All** — One-click bulk update for all outdated packages
- 🏷️ **Stable Versions Only** — Pre-release versions (beta, RC, alpha, canary) are automatically filtered out from all upgrade suggestions

### 🔄 Version Management

- 📏 **Bundle Size** — Each package shows its gzipped bundle size, fetched from Bundlephobia in the background
- 📋 **Change Version Dropdown** — Browse all stable versions of any package in a single dropdown to upgrade or downgrade
- ✂️ **Clean Version Display** — Long version strings like `5.1.0-rc-fb9a90fa48-20240614` are shortened to `v5.1.0` for readability
- 🧠 **Smart Version Sampling** — When a package has hundreds of versions, the list is intelligently sampled to keep it under 20 items
- ⏳ **Version Prefetching** — All available versions are fetched in the background so dropdowns are ready instantly

### ➕ Package Installation

- 🔍 **NPM Registry Search** — Search for new packages directly from the search bar with real-time results from the npm registry
- 🖱️ **One-Click Install** — Install any package as a dependency or dev dependency with dedicated Install and Dev Install buttons
- 💾 **Search Caching** — Previously searched queries are cached for instant repeat results

### 🗑️ Package Removal

- ⚠️ **Safe Uninstall** — Trash icon with a confirmation popup dialog to prevent accidental removals

### 🔎 Search & Filtering

- ⌨️ **Real-Time Search** — Filter installed packages by name as you type
- 🏷️ **Status Filtering** — Click stat cards to show only up-to-date, outdated, or vulnerable packages
- 🔗 **Combined Search** — Search bar filters installed packages and queries the npm registry simultaneously

### 🛡️ Security Audit

- 🔬 **Vulnerability Scanning** — Runs `npm audit` (or equivalent for yarn/pnpm/bun) in the background to detect known vulnerabilities
- 🛡️ **Security Column** — Each package shows a shield icon: ✅ green checkmark if safe, or a colored badge with vulnerability count if issues are found
- 🚨 **Severity Levels** — Vulnerabilities are color-coded: 🔴 critical, 🟠 high, 🟡 moderate, ⚪ low
- 🖱️ **Hover for Details** — Hover over any vulnerability badge to see a popover listing each issue with severity level, title, and link to the advisory
- 📊 **Security Stat Card** — A dedicated stat card shows the total count of vulnerable packages — click to filter the table

### 📄 Package Details

- 🔗 **Quick Links** — Each package shows small npm, repo, and docs links directly below the name
- 📝 **Click for Details** — Click any package name to open a popover with description, version, type badge, latest version, and links to npm, GitHub, and homepage
- 📖 **Package Descriptions** — Fetched from the npm registry and displayed in the detail popover

### ⚠️ Duplicate Detection

- 🔁 **Duplicate Warning** — If the same package appears in both `dependencies` and `devDependencies`, an amber "Duplicate" badge is shown next to the package name

### 🔄 Auto Detection & Refresh

- 🔍 **Auto-Detect Package Manager** — Automatically detects npm, yarn, pnpm, or bun based on lock files in your project
- 👀 **File Watcher** — Watches `package.json` for changes and refreshes the UI automatically
- 💾 **Cached Data** — Panel loads instantly with cached data while fresh data is fetched in the background
- ⏱️ **Refresh Cooldown** — Smart throttling prevents excessive refreshes (30-second minimum between auto-refreshes)

### ⚡ Performance & Optimization

- 🗄️ **Registry Cache** — npm registry responses cached for 5 minutes, eliminating redundant network calls
- 🔀 **Concurrency Limits** — Registry fetches batched at 15 concurrent requests to avoid flooding the network
- 📁 **node_modules Size Cache** — Size calculation cached by directory mtime, skipping expensive recalculation when nothing changed
- 🚫 **Duplicate Action Prevention** — Update, install, and uninstall blocked while a previous operation on the same package is in progress

### 🔒 Security Hardening

- ✅ **Input Validation** — Package names and versions validated via strict regex to prevent command injection
- 🌐 **URL Validation** — External URLs validated to only allow `http://` and `https://` schemes
- 🛡️ **Path Traversal Prevention** — Package name validation added to internal file lookups
- 📦 **Search Cache Limit** — npm search cache limited to 50 entries to prevent unbounded memory growth

### 🎨 Developer Experience

- 🌗 **Theme Aware** — Follows your VS Code theme (light and dark) seamlessly with soft, non-distracting colors
- 📌 **Scroll Preservation** — Your scroll position is maintained when the package list refreshes
- ⏳ **Loading States** — Spinners at page, row, and cell level so you always know what's happening

---

## 🚀 Installation

1. Open **VS Code**
2. Go to the **Extensions** panel (`Ctrl+Shift+X`)
3. Search for **NPM Manager**
4. Click **Install**

Or install from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager).

---

## 📦 Supported Package Managers

| Manager | Lock File                | Status |
| ------- | ------------------------ | ------ |
| npm     | `package-lock.json`      | ✅ Fully supported |
| yarn    | `yarn.lock`              | ✅ Fully supported |
| pnpm    | `pnpm-lock.yaml`         | ✅ Fully supported |
| bun     | `bun.lockb` / `bun.lock` | ✅ Fully supported |

---

## 📄 License

This extension is free to use. All rights reserved.

See [LICENSE](LICENSE) for details.

---

## 👨‍💻 Author

**Mamunur Rashid** — Senior Software Engineer with 10+ years of experience in web development, specializing in dynamic CMS-based and custom web applications.

**Tech Stack:** PHP, Laravel, Node.js, TypeScript, Vue.js, React.js, C#/.NET, MySQL, PostgreSQL, Docker, AWS

🌐 [Website](https://mdrashid.com) · 🐙 [GitHub](https://github.com/rocke3) · 💼 [LinkedIn](https://linkedin.com/in/rfmamun) · 🎯 [Fiverr](https://fiverr.com/mamunurrashi461)
