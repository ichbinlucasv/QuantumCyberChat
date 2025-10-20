# QuantumCyberChat

## Overview
QuantumCyberChat is an open-source, privacy-centric chat application designed for secure, decentralized communication. It emphasizes resistance to quantum computing threats and governmental surveillance through post-quantum cryptography, peer-to-peer architecture, optional Tor anonymity, and minimal metadata exposure. Inspired by privacy-focused tools, this prototype serves as a foundation to attract developers for enhancements.

Key Features:
- Peer-to-peer messaging with no central servers.
- End-to-end encryption using post-quantum algorithms (ML-KEM-768 for key encapsulation and AES-256-GCM for symmetric encryption).
- Minimal metadata exposure for enhanced privacy.
- Optional Tor integration: Run the server as a hidden service and connect clients via Tor for IP obfuscation and anti-surveillance.
- Support for future integrations like I2P or advanced group messaging.

## Why This Approach?
This app prioritizes user privacy and security against advanced threats, including quantum attacks and potential monitoring, by leveraging Rust's safety guarantees, decentralized protocols, and Tor for anonymity.

## Installation
1. Install Rust: Visit https://www.rust-lang.org/tools/install.
2. Clone the repository: `git clone https://github.com/ichinlucasv/QuantumCyberChat.git`
3. Navigate to the directory: `cd QuantumCyberChat`
4. Build: `cargo build`

## Usage
- **Server**:
  - Basic: `cargo run --bin server -- --host 127.0.0.1 --port 55555`
  - With Tor (hidden service): `cargo run --bin server -- --tor`
    - The server will print the .onion address upon startup.
- **Client**:
  - Basic: `cargo run --bin client -- --host 127.0.0.1 --port 55555`
  - With Tor: `cargo run --bin client -- --host <onion_address> --tor`
- Exchange messages securely; type 'exit' to quit.

Note: This is a local prototype. For real P2P, expand with libraries like libp2p.

## E2EE Implementation
- **Quantum-Resistant Encryption**: Messages are protected using ML-KEM-768 for key encapsulation and AES-256-GCM for symmetric encryption.
- **Usage Notes**: Run the server, then multiple clients. Clients will automatically exchange public keys and encrypt messages end-to-end. The server acts solely as a relay for ciphertexts.

## Roadmap
- Integrate full post-quantum crypto crates (e.g., oqs-rs).
- Add Tor/I2P support for anonymity.
- Implement user authentication and group chats.
- Develop GUI (e.g., using iced or druid) and mobile ports.
- Enhance decentralization with DHT peer discovery.

## Contributing
Contributions are encouraged to strengthen privacy features. Fork the repo, create a branch, and submit pull requests.

## License
MIT License. See LICENSE for details.

## Contact
Open issues on GitHub for discussions.
