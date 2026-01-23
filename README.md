<div align="center">
  <img src="website/assets/Methodwise-logo.png" alt="Methodwise Logo" width="600">
  <br>
  
  [![Made with Rust](https://img.shields.io/badge/Made_with-Rust-1f425f.svg?logo=rust&logoColor=white)](https://www.rust-lang.org/)
  [![Crates.io](https://img.shields.io/crates/v/methodwise.svg)](https://crates.io/crates/methodwise)
  [![Build Status](https://github.com/Geekspeaker/methodwise/actions/workflows/release.yml/badge.svg)](https://github.com/Geekspeaker/methodwise/actions/workflows/release.yml)
</div>

# Methodwise Browser
> *A precise, methodic TUI web browser for the terminal enthusiast.*

Methodwise is a Rust-based terminal web browser designed for speed, simplicity, and keyboard-driven navigation. It renders the modern web into clean, readable text, stripping away the noise of ads and heavy scripts.

## Features

-   **Text-First Browsing**: Renders HTML content into readable text and ASCII layouts.
-   **Keyboard Navigation**: Vim-like bindings (j/k/h/l) and numeric shortcuts for links.
-   **Smart Search**: Unified URL/Search bar. Type a URL or just search terms.
-   **Link Following**: Press `f` followed by a link number to navigate instantly.
-   **Form Input Support**: Tab into search boxes, type, and submit forms.
-   **Multi-Tab Browsing**: Open up to 9 tabs, switch with number keys.
-   **Theme Support**: 4 color schemes (Dark, Light, Retro, Ocean).
-   **Bookmarks & History**: Save favorites and browse your history.
-   **Debug Console**: Built-in developer tools (F12) to inspect browser events.
-   **Zero-Distraction**: No ads, no popups, just content.
-   **Cross-Platform**: Runs on Windows, Linux, and macOS.

## Privacy Promise
We are committed to a strict **Zero Data Collection** policy.
-   **No Telemetry**: We do not track your usage.
-   **No Cloud Storage**: History and bookmarks stay on your device.
-   **No Tracking**: Sponsored links are static text only.
-   [Read our full Privacy Policy](PRIVACY.md)

## Getting Started

### Prerequisites
-   Rust & Cargo (latest stable version)
-   A terminal with UTF-8 support (modern Windows Terminal, Alacritty, iTerm2, etc.)

### Installation

**Option 1: Developer Install (Recommended for Rust users)**
This compiles the project and adds `methodwise` to your global PATH.
```bash
cargo install --path .
# Now you can just run:
methodwise
```

**Option 2: Build from Source**
```bash
git clone https://github.com/Geekspeaker/methodwise.git
cd methodwise
cargo build --release
# Run via cargo:
cargo run --release
```

**Option 3: Package Managers(COMING SOON)**
See [DISTRIBUTION.md](docs/DISTRIBUTION.md) for APT (Ubuntu/Debian) and Homebrew (macOS) instructions. These methods automatically add `methodwise` to your PATH.


### Usage

Run the browser:
```bash
cargo run --release
```

## Shortcuts

| Key | Action |
| :--- | :--- |
| **Navigation** | |
| `j` / `Down` | Scroll Down |
| `k` / `Up` | Scroll Up |
| `h` / `Left` | Go Back |
| `l` / `Right` | Go Forward |
| `PgDn` / `PgUp` | Page Scroll |
| **Actions** | |
| `e` / `g` | Edit URL / Search |
| `/` | Find text in page |
| `f` / `0-9` | Follow Link Mode |
| `Tab` | Enter form input mode |
| `?` | Toggle Help |
| `F12` | Toggle Debug Log |
| **Tabs** | |
| `Shift+T` | New Tab |
| `Shift+W` | Close Tab |
| `1-9` | Switch to Tab # |
| **Themes & Bookmarks** | |
| `t` | Cycle Theme (Dark/Light/Retro/Ocean) |
| `b` | Toggle Bookmarks |
| `B` | Add Bookmark |
| `H` | Toggle History |

## Themes

Press `t` to cycle through color schemes:
- **Dark** (default): Cyan accents on dark background
- **Light**: Blue accents on light background
- **Retro**: Green terminal aesthetic
- **Ocean**: Blue shades

## Form Input

Methodwise supports basic form interaction:
1. Navigate to a page with a search form (e.g., duckduckgo.com)
2. Press `Tab` to enter form mode
3. Type your search query
4. Press `Enter` to submit
5. Press `Esc` to cancel

## Configuration

Methodwise is zero-config by default, but supports CLI flags:

```bash
# Run with default search engine (DuckDuckGo)
.\target\release\methodwise.exe

# Choose search engine
.\target\release\methodwise.exe --google
.\target\release\methodwise.exe --duckduck
.\target\release\methodwise.exe --bing
.\target\release\methodwise.exe --brave

# Open a URL directly
.\target\release\methodwise.exe https://example.com

# Force static homepage (skip fetching methodwise.com)
.\target\release\methodwise.exe --static-homepage
```

## Troubleshooting

-   **Redirects**: Some sites require cookies or complex redirects. Methodwise handles standard redirects and META refresh tags.
-   **Rendering**: If text wraps oddly, try resizing your terminal. The renderer adapts to viewport width.
-   **Forms**: Standard GET/POST forms are supported. JavaScript-heavy forms may not work.
-   **Access Denied/Bot Detection**: Methodwise uses a standard browser User-Agent and accepts compressed content to mitigate bot detection on sites like Amazon.

## Support & Sponsorship

Methodwise is an independent project. If you find it useful, consider supporting its development!

-   **GitHub Sponsors**: Support the developer directly.

## License

Methodwise is free to use but **Source Available**.
You may use and run the software freely. You may verify and modify the source for personal use, but **redistribution of modified versions is prohibited**.
Contributions are welcome! By submitting code, you agree to transfer ownership to the project maintainers.
See [LICENSE](LICENSE) for details.

---
*Built with Rust, Ratatui, and Tokio. by [Geekspeaker Inc.](https://geekspeaker.com)*
