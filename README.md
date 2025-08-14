# secure p2p

A browser-based, peer-to-peer (P2P) file sharing system that provides secure, real-time file transfers with end-to-end encryption.

---

## 📜 Description

Traditional file sharing methods like email or cloud storage expose your data to interception and unauthorized access by third parties. This project solves that problem by allowing two users to exchange files directly through their browsers, with no central server storing the files.

It uses **WebRTC** for a direct P2P connection and a strong cryptographic stack for security. An **Elliptic Curve Diffie-Hellman (ECDH)** key exchange securely creates a shared key, and files are encrypted chunk-by-chunk using **AES-GCM**, ensuring confidentiality and data integrity. The entire application runs in the browser, requiring no extra software or plugins.

---

## ✨ Key Features

* **End-to-End Encryption**: File transfers are secured using AES-GCM authenticated encryption.
* **Secure Key Exchange**: Uses Elliptic Curve Diffie-Hellman (ECDH) to establish a shared secret key without exposing it to any intermediary.
* **Serverless File Transfer**: Files are sent directly between peers using WebRTC. A minimal signaling server is used only to establish the initial connection.
* **Browser-Based**: Runs entirely in modern web browsers (Chrome, Firefox, etc.) without needing plugins or extensions.
* **Large File Support**: Efficiently handles large files by breaking them into smaller chunks for transfer.

---

## 🏗️ Architecture

The system uses a modular, layered architecture for security and performance.

* **User Interface (UI) Layer**: Built with React.js, this layer handles user interaction for selecting files and managing connections.
* **Application Logic / Controller Layer**: The core of the application, managing peer discovery, session tokens, and file selection logic.
* **Encryption & Security Layer**: Manages all cryptographic operations, including the ECDH key exchange and AES-GCM encryption/decryption of files.
* **Network Communication Layer**: Handles the real-time P2P data transmission using WebRTC and uses STUN/TURN servers for NAT traversal to connect peers across different networks.
* **Platform/Device Layer**: Ensures cross-platform compatibility by using standard browser APIs for file access.

---

## 🛠️ Tech Stack

* **Frontend**: React.js (v17+), Material-UI (MUI), Socket.IO Client
* **Backend**: Node.js (v16+), Express.js, Socket.IO (v4+)
* **Core Technologies**: WebRTC, Web Crypto API (SubtleCrypto)
* **Development Tools**: Visual Studio Code, npm/yarn

---

## 🚀 Getting Started

### Prerequisites

* Node.js (v16 or later)
* npm or yarn package manager
* A modern web browser with WebRTC support

### Installation & Setup

**1. Clone the repository:**
```bash
git clone [https://github.com/your-username/secure-p2p.git](https://github.com/your-username/secure-p2p.git)
cd secure-p2p
