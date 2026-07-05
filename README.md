<p align="center">
  <img src="https://raw.githubusercontent.com/rocke3/npm-manager/main/img/logo.png" alt="NPM Manager" width="128" height="128" />
</p>

<h1 align="center">NPM Manager — Visual Package Manager for VS Code</h1>

<p align="center">
  <strong>Manage npm, yarn, pnpm &amp; bun dependencies from a visual dashboard — update, downgrade, install, uninstall, and audit packages without the terminal.</strong>
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager"><img src="https://img.shields.io/visual-studio-marketplace/v/MdRashid.npm-manager?label=Marketplace&color=4285F4" alt="Visual Studio Marketplace version of the NPM Manager extension" /></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager"><img src="https://img.shields.io/visual-studio-marketplace/i/MdRashid.npm-manager?label=Installs&color=00C853" alt="Install count for the NPM Manager VS Code extension" /></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager&ssr=false#review-details"><img src="https://img.shields.io/visual-studio-marketplace/r/MdRashid.npm-manager?label=Rating&color=FF6B35" alt="User rating for NPM Manager on the VS Code Marketplace" /></a>
</p>

**NPM Manager** is a free [Visual Studio Code](https://code.visualstudio.com/) extension that turns dependency management into a fast, visual experience. Instead of memorizing terminal commands, you get a clean dashboard to **view, update, downgrade, install, uninstall, and audit** the packages in your `package.json`. Spot outdated dependencies at a glance, understand the risk of every update with color-coded semver badges, scan for security vulnerabilities in one click, and check gzipped bundle sizes before you install.

Works with **npm**, **yarn**, **pnpm**, and **bun** — auto-detected from your lock file, no configuration required.

### Why NPM Manager?

- 🚫 **No terminal required** — update, install, and remove packages with a click
- 🎯 **Safe, semver-aware upgrades** — patch, minor, and major changes are color-coded so you know the risk before you click
- 🛡️ **Built-in security audit** — surface `npm audit` vulnerabilities right next to each dependency
- 📦 **Bundle-size awareness** — see the gzipped cost of a package before adding it
- 🔁 **One tool for every package manager** — npm, yarn, pnpm, and bun in a single UI
- 🌗 **Native feel** — theme-aware, fast, and built to match your VS Code setup

---

## 🖼️ Preview

![NPM Manager dashboard in VS Code showing installed dependencies, color-coded update buttons, security audit results, and bundle sizes](https://raw.githubusercontent.com/rocke3/npm-manager/main/img/preview.webp)

---

<table>
<tr>
<td width="110" align="center" valign="middle">
<a href="https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom?utm_source=item-share-cb">
<img src="https://raw.githubusercontent.com/rocke3/npm-manager/main/img/tap.png" alt="TabAutoPilot" width="88" height="88" />
</a>
</td>
<td valign="middle">

#### 🚀 Try TabAutoPilot &nbsp;·&nbsp; <sub>AI Tab Organizer for Chrome</sub>

**Drowning in tabs?** A free Chrome extension by the same author — auto-groups tabs by topic, removes duplicates, hibernates inactive ones, and saves sessions as workspaces. 100% on-device, no tracking.

<a href="https://chromewebstore.google.com/detail/tabautopilot-smart-tab-ma/nplekjmldglpfcdiechmgahoefhfheom?utm_source=item-share-cb"><img src="https://img.shields.io/badge/Install%20for%20Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Install for Chrome" /></a> &nbsp; <img src="https://img.shields.io/badge/Free-00C853?style=for-the-badge" alt="Free" /> &nbsp; <img src="https://img.shields.io/badge/On--device-FF6B35?style=for-the-badge" alt="On-device" />

</td>
</tr>
</table>

<table>
<tr>
<td width="110" align="center" valign="middle">
<a href="https://net.mdrashid.com/">
<img src="https://raw.githubusercontent.com/rocke3/npm-manager/main/img/lmt.png" alt="LiveMetrics" width="88" height="88" />
</a>
</td>
<td valign="middle">

#### 🚀 Try LiveMetrics &nbsp;·&nbsp; <sub>Network & system monitor for Mac</sub>

**Chrome eating your RAM isn't the only thing worth watching.** A free macOS menu bar app showing live upload and download speed every second — read from your Mac's own interface counters, so the numbers reflect what's actually moving. CPU, GPU, RAM and temperature by default too.

<a href="https://net.mdrashid.com/"><img src="https://img.shields.io/badge/Download%20for%20macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="Download for macOS" /></a> &nbsp; <img src="https://img.shields.io/badge/Free-00C853?style=for-the-badge" alt="Free" /> &nbsp; <img src="https://img.shields.io/badge/Menu%20bar-FF6B35?style=for-the-badge" alt="Menu bar" />

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

Get the NPM Manager extension running in under a minute:

1. Open **VS Code**
2. Go to the **Extensions** panel (`Ctrl+Shift+X`)
3. Search for **NPM Manager**
4. Click **Install**

Or install from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MdRashid.npm-manager).

---

## 📦 Supported Package Managers

| Manager | Lock File                | Status             |
| ------- | ------------------------ | ------------------ |
| npm     | `package-lock.json`      | ✅ Fully supported |
| yarn    | `yarn.lock`              | ✅ Fully supported |
| pnpm    | `pnpm-lock.yaml`         | ✅ Fully supported |
| bun     | `bun.lockb` / `bun.lock` | ✅ Fully supported |

---

## 💡 Common Use Cases

- **Update outdated npm packages** without leaving the editor or running `npm outdated`
- **Safely upgrade or downgrade a dependency** to a specific version from a dropdown of stable releases
- **Audit a project for security vulnerabilities** and see affected packages at a glance
- **Compare bundle sizes** before adding a new dependency to keep your app lean
- **Migrate between package managers** — the same UI works for npm, yarn, pnpm, and bun
- **Onboard onto an unfamiliar codebase** by browsing every dependency, its version, and its description in one panel

---

## ❓ Frequently Asked Questions

**Is NPM Manager free?**
Yes. NPM Manager is completely free to install and use from the Visual Studio Code Marketplace.

**How do I update npm packages in VS Code with NPM Manager?**
Open the NPM Manager panel, and any dependency with a newer release shows a color-coded update button (green for patch, amber for minor, coral for major). Click it to update a single package, or use **Update All** to upgrade every outdated package at once.

**Does it work with yarn, pnpm, and bun?**
Yes. NPM Manager auto-detects your package manager from the lock file (`package-lock.json`, `yarn.lock`, `pnpm-lock.yaml`, or `bun.lockb` / `bun.lock`) and runs the correct commands for you.

**Can I downgrade a package to an older version?**
Yes. Open the version dropdown for any package to browse its stable releases and switch to any version — upgrade or downgrade.

**How does the security audit work?**
NPM Manager runs `npm audit` (or the yarn/pnpm/bun equivalent) in the background and shows a shield badge on each package, color-coded by severity, with a hover popover linking to the advisory.

**Will it slow down VS Code?**
No. Registry responses are cached, network requests are batched, and the panel loads instantly from cached data while fresh results are fetched in the background.

**Does it send my data anywhere?**
No. NPM Manager only talks to the public npm registry and Bundlephobia to fetch version, description, and bundle-size information. Your code stays on your machine.

---

## 📄 License

This extension is free to use. All rights reserved.

See [LICENSE](LICENSE) for details.

---

## 👨‍💻 Author

**Mamunur Rashid** — Senior Software Engineer with 10+ years of experience in web development, specializing in dynamic CMS-based and custom web applications.

**Tech Stack:** PHP, Laravel, Node.js, TypeScript, Vue.js, React.js, C#/.NET, MySQL, PostgreSQL, Docker, AWS

🌐 [Website](https://mdrashid.com) · 🐙 [GitHub](https://github.com/rocke3) · 💼 [LinkedIn](https://linkedin.com/in/rfmamun) · 🎯 [Fiverr](https://fiverr.com/mamunurrashi461)
