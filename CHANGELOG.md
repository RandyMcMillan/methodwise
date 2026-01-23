# Changelog

All notable changes to this project will be documented in this file.

## [0.1.1] - 2026-01-23

### Fixed
- Fixed favicon path in website index.html

### Improved
- Website is now mobile responsive with proper scaling for all screen sizes

### Added
- Unit tests for `renderer.rs` to verify HTML rendering and form extraction logic.
- Enabled HTTP compression (gzip, brotli, deflate) support in `reqwest` and updated network headers to mimic standard browsers. This fixes access to sites like Amazon that block non-compressed clients.

### Changed
- Refactored `FormField` struct in `renderer.rs` to remove redundant `form_action` and `form_method` fields, improving memory usage.
- Home button now navigates to `methodwise.com/text.html` instead of showing static embedded homepage.
- `Tab::new()` now accepts engine name parameter for consistent start page across tabs.
- New tabs now display the proper start page with correct search engine instead of a blank message.
- Consolidated duplicate tab creation code - `Shift+T` now calls `create_new_tab()` method.

### Fixed
- Fixed mouse click coordinates not matching UI layout - clicks on tabs, navigation buttons, and content links now work correctly.
- Fixed tab/app state synchronization issues where tabs could show different content than the main view.
- Fixed `go_home()` not syncing state with active tab.
- Fixed new tabs always using DuckDuckGo regardless of selected search engine.
- Fixed unused field warning for `title` in `Tab` struct (`browser.rs`).
- Fixed unused field warnings for `form_action` and `form_method` in `FormField` (`renderer.rs`).

### Updated
- `website/text.html` now matches native Rust homepage format with numbered links `[1]`, `[2]`, etc.
- Added "Press 's' to switch engine" instruction to `text.html` footer.

## [0.1.0] - 2026-01-22

- Initial release
