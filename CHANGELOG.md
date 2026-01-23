# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

### Added
- Unit tests for `renderer.rs` to verify HTML rendering and form extraction logic.
- Enabled HTTP compression (gzip, brotli, deflate) support in `reqwest` and updated network headers to mimic standard browsers. This fixes access to sites like Amazon that block non-compressed clients.

### Changed
- Refactored `FormField` struct in `renderer.rs` to remove redundant `form_action` and `form_method` fields, improving memory usage.

### Fixed
- Fixed unused field warning for `title` in `Tab` struct (`browser.rs`).
- Fixed unused field warnings for `form_action` and `form_method` in `FormField` (`renderer.rs`).
