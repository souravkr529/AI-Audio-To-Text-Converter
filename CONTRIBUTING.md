# Contributing to Secure AI Transcriber

Thank you for your interest in contributing! We welcome improvements to the UI, security hardening, or AI prompt engineering.

## How to Contribute

1.  **Fork the repository** on GitHub.
2.  **Clone your fork** locally.
3.  **Create a feature branch** (`git checkout -b feature/amazing-feature`).
4.  **Commit your changes** (`git commit -m 'Add some amazing feature'`).
5.  **Push to the branch** (`git push origin feature/amazing-feature`).
6.  **Open a Pull Request**.

## Guidelines

*   **Single File Philosophy**: Try to keep the application contained within `voice.html` if possible.
*   **Universal Design**: Ensure features work for ALL types of audio, not just specific domains like sales or medical.
*   **Security First**: Any changes to file handling must pass the Magic Bytes validation check.
