# QuantumCyberChat

[![GitHub license](https://img.shields.io/github/license/ichbinlucasv/QuantumCyberChat)](https://github.com/ichbinlucasv/QuantumCyberChat/blob/main/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/ichbinlucasv/QuantumCyberChat)](https://github.com/ichbinlucasv/QuantumCyberChat/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/ichbinlucasv/QuantumCyberChat)](https://github.com/ichbinlucasv/QuantumCyberChat/issues)

A superior, open-source alternative to SimpleX Chat. Privacy-focused P2P messaging with post-quantum crypto (Kyber/Dilithium hybrid), Tor anonymity, unlimited groups, QR code invites, file/voice sharing, and cross-platform support (Linux/Android via Haskell backend + Python UI).

## Overview

QuantumCyberChat is a decentralized, secure chat application designed for individuals, families, and friends who prioritize privacy. It uses peer-to-peer architecture with no central servers, ensuring metadata protection. Key features include:
- Post-quantum encryption for quantum-resistant security.
- Tor integration for anonymous networking.
- Unlimited group sizes with moderation tools.
- QR code and one-time link invitations (like SimpleX).
- File sharing and voice call stubs.
- Fast performance for small groups.
- Multi-factor auth (PIN/biometrics).
- Zero-knowledge proofs for advanced verification.

Better than SimpleX: Enhanced UI with Kivy (mobile-friendly), faster P2P discovery, group directory search, and built-in moderation.

## Screenshots

[Add images here, e.g., via GitHub upload: UI screenshot, QR example]

## Installation

### Prerequisites
- Haskell: Install GHC and Stack (https://www.haskell.org/).
- Python: 3.12+ with pip.
- SQLite for DB.

### Setup
1. Clone the repo: `git clone https://github.com/ichbinlucasv/QuantumCyberChat.git`
2. For Haskell backend: `cd src && stack install`
3. For Python UI: `cd ui && pip install -r requirements.txt`
4. Run DB schema: `sqlite3 quantum_chat.db < db/ultra_chat_schema.sql`

## Usage

- Start backend: `./QuantumCyberChat` (from src after build).
- Start UI: `python quantum_cyber_chat.py` (from ui).
- Connect via Tor: Ensure Tor is running on port 9050.
- Generate QR invite: Use UI "Gen QR" button.
- Scan QR: Paste QR text in UI (camera integration TODO).
- Create group: UI "Create Group", invite members via QR/links.
- Send messages/files: Type in UI, select recipient/group.

For Android: Build with Kivy/Buildozer.

## Architecture

- **Backend (Haskell)**: Core logic, crypto, P2P, Tor integration.
- **UI (Python/Kivy)**: Cross-platform interface for Linux/Android.
- **DB (SQLite)**: Local encrypted storage for messages/groups.

## Roadmap

- Full voice calls integration.
- Mobile camera for QR scanning.
- AI-based anomaly detection enhancements.
- iOS support.
- Community directory for public groups.

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

See [SECURITY.md](SECURITY.md) for reporting vulnerabilities. We use hybrid crypto and regular audits.

## License

Licensed under AGPLv3. See [LICENSE](LICENSE) for details.

## Contact/Acknowledgments

- Inspired by SimpleX Chat.
- Code generation assistance from xAI/Grok.
- Contact: Open an issue or email [your email].

As of December 09, 2025.