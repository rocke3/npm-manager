# Changelog

All notable changes to the **NPM Manager** extension will be documented in this file.

## [1.0.6] - 2026-04-04

### Redesigned
- **Simplified Table Layout** — Removed Installed, Latest, and Downgrade columns for a cleaner look. Installed version now shown as a subtitle under the package name.
- **Color-Coded Upgrade Buttons** — Upgrade button color indicates update impact: green (patch — bug fixes), amber (minor — new features), coral (major — breaking changes).
- **Hover Tooltips** — Upgrade buttons show a contextual tooltip on hover with an icon and description of the update type (shield for patch, star for minor, alert for major).
- **Change Version Dropdown** — Single dropdown combining all stable upgrade and downgrade versions, replacing the separate Upgrade/Downgrade dropdowns.
- **Smart Version Sampling** — When a package has many versions, the dropdown is intelligently sampled to keep the list under 20 items.
- **Stable Versions Only** — Beta, RC, alpha, canary, and other pre-release versions are automatically filtered out from all upgrade suggestions and version dropdowns.
- **Uninstall Icon** — Uninstall button now uses a trash icon instead of an X.
- **Search Install Buttons** — Redesigned Install (green with + icon) and Dev Install (blue with code icon) buttons in search results. "Dev" renamed to "Dev Install".
- **Search Input Visibility** — Improved search input border contrast and shadow for better visibility in dark themes.
- **Version Column** — Installed version moved to its own dedicated column for clarity.
- **Package Details Popover** — Click any package name to open a popover showing description, version, type badge (dep/dev), latest version, and quick links to npm, GitHub, and homepage/docs.
- **Inline Package Links** — Each package shows small npm, repo, and docs links directly below the name for quick access.
- **Package Metadata** — Description, repository, and homepage URLs are now fetched from the npm registry for each package.
- **Clean Version Display** — Long version strings like `5.1.0-rc-fb9a90fa48-20240614` are shortened to `v5.1.0`. All versions now prefixed with `v`.
- **Bundle Size Display** — Each package shows its gzipped bundle size above the version number, fetched from bundlephobia in the background.
- **Duplicate Dependency Warning** — Detects packages that appear in both `dependencies` and `devDependencies` and shows an amber "duplicate" badge next to the name.
- **Security Audit** — Runs `npm audit --json` (or equivalent for yarn/pnpm/bun) in the background. Shows a Security column with vulnerability count badges, color-coded by severity. Click to see details with advisory links. New stat card shows total vulnerable packages.

## [1.0.5] - 2026-03-02

### Added
- **NPM Registry Search** — Search bar now queries the npm registry in real-time (debounced) and displays up to 10 uninstalled packages with name, description, and version.
- **Install New Packages** — Each search result has an **Install** button (production dependency) and a **Dev** button (devDependency) to add new packages directly from the UI.
- Loading spinner and "no results" feedback while searching.
- Search results dropdown closes automatically when clicking outside.
- Search results persist after install so you can install multiple packages in a row.

### Optimized
- Search results cached on backend — repeated queries return instantly without hitting npm registry.
- Stale search results discarded — fast typing no longer causes old results to flash.
- Version prefetching batched (5 concurrent) to avoid flooding the network on projects with many packages.

## [1.0.4] - 2025-12-20

### Added
- Enhanced error handling for package data updates with detailed messages for "no workspace" and "no package.json" scenarios.

## [1.0.3] - 2025-12-18

### Fixed
- Version number bump for marketplace release.

## [1.0.2] - 2025-12-17

### Fixed
- Updated repository URL and added publisher and icon fields in package.json.
- Removed logo from README.md.

## [1.0.1] - 2025-12-15

### Fixed
- Updated VS Code engine version to `^1.109.0` for broader compatibility.

### Added
- Updated package dependencies and improved version selection UI with smart filtering (milestone versions for large lists).

## [1.0.0] - 2025-12-12

### Added
- Initial release of NPM Manager.
- Visual dashboard to view all dependencies and devDependencies from `package.json`.
- Installed vs latest version comparison with status indicators (green/yellow dots).
- **Update** individual packages to latest or select a specific version from dropdown.
- **Update All** outdated packages in one click.
- **Downgrade** packages to any previously published version.
- **Uninstall** packages with confirmation step.
- Smart version dropdown filtering (shows milestones when >10 versions available).
- Environment info bar showing project name, Node.js version, and package manager version with latest-available indicators.
- Stats cards with clickable filters (Total / Up to Date / Outdated).
- Search bar to filter installed packages by name.
- Multi-package manager support: npm, yarn, pnpm, bun (auto-detected via lock files).
- Sidebar tree view with package status icons.
- Auto-refresh on `package.json` changes via file watcher.
- Cached data for instant panel load on reopen.
- Links to npmjs.com for each package.
