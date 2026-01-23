# Contributing to Methodwise

First off, thank you for considering contributing to Methodwise! It's people like you that make Methodwise such a great tool.

## Legal Note (Source Available)
Methodwise is **Source Available**, not Open Source in the traditional OSI sense.
- You **CAN** view, modify, and run the code for personal use.
- You **CAN** contribute PRs to this repository.
- You **CANNOT** redistribute modified binaries or sell the software without permission.
- By contributing, you agree that your contributions are licensed to the project maintainers under the same terms.

## How to Contribute

### Reporting Bugs
This section guides you through submitting a bug report for Methodwise. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports.

- **Use a clear and descriptive title** for the issue to identify the problem.
- **Describe the exact steps which reproduce the problem** in as much detail as possible.
- **Provide specific examples** to demonstrate the steps.

### Pull Requests
1.  Fork the repo and create your branch from `main`.
2.  If you've added code that should be tested, add tests.
3.  Ensure the test suite passes (`cargo test`).
4.  Make sure your code lints (`cargo clippy`).
5.  Format your code (`cargo fmt`).

## Development Setup

1.  Install Rust and Cargo.
2.  Clone the repo:
    ```bash
    git clone https://github.com/Geekspeaker/methodwise.git
    ```
3.  Build:
    ```bash
    cargo build
    ```

## Style Guide
- We follow standard Rust formatting (`cargo fmt`).
- Variable names should be descriptive.
- Comments are encouraged for complex logic, especially in `renderer.rs` and `network.rs`.
