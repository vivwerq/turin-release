# Turin Security Toolkit

Welcome to the official release repository for the **Turin Security Toolkit**. 

Turin is a next-generation, high-performance, and AI-assisted dynamic application security testing (DAST) suite. It merges local interception proxying with parameter fuzzing, token entropy checks, smart string decoding, WAF evasion mechanisms, and collaborative cloud sync capabilities.

---

##  Key Features

*   **MITM Interception Proxy**: Intercept, analyze, modify, and replay HTTP/S and WebSocket web traffic.
*   **Request Repeater**: Multi-tab raw request editor supporting custom headers, redirection toggles, and SSL configurations.
*   **Intruder / Parameter Fuzzer**: Execute wordlist-based fuzzing campaigns with target-filtering and size-clustering validation.
*   **Token Sequencer**: Run predictability tests using Shannon entropy models and LCG sequence solvers to find weak tokens.
*   **Smart Recursive Decoder**: Decipher nested encodings (URL, Base64, Hex, HTML) down to cleartext layers in one click.
*   **WAF Evasion Engine**: Inject header payloads, normalize Unicode homoglyphs, and execute raw TCP smuggling bypasses.
*   **xcomrade.tech Sync**: Collaborate in real-time with team presence tracking, shared findings, and synchronized workspaces.

---

##  Installation & Setup

Choose the installation option that matches your Linux environment from our Releases Page
### Option 1: Debian / Ubuntu / Kali Linux (`.deb`)
The Debian package is recommended for Kali Linux, Ubuntu, and Debian desktop systems as it registers command-line shortcuts and desktop environment menus.

1. **Download the latest `.deb` package**:
   ```bash
   wget https://github.com/0xxc0mrade/turin-releases/releases/latest/download/turin.deb
   ```
2. **Install the package using apt** (to automatically resolve dependencies):
   ```bash
   sudo apt update
   sudo apt install ./turin.deb
   ```
3. **Launch the application**:
   * Open your application launcher and search for **Turin Security Toolkit**.
   * Or launch directly from your terminal:
     ```bash
     turin
     ```

### Option 2: Standalone AppImage (`.AppImage`)
The AppImage is a single, self-contained executable that runs on any modern Linux distribution without installation.

1. **Download the AppImage**:
   ```bash
   wget https://github.com/0xxc0mrade/turin-releases/releases/latest/download/Turin.AppImage
   ```
2. **Make it executable**:
   ```bash
   chmod +x Turin.AppImage
   ```
3. **Run the application**:
   ```bash
   ./Turin.AppImage
   ```

>  **FUSE Requirement**: If you encounter an error starting the AppImage due to missing FUSE support on newer distros (like Ubuntu 22.04+), install it via `sudo apt install libfuse2` or extract the bundle directly:
> ```bash
> ./Turin.AppImage --appimage-extract
> ./squashfs-root/AppRun
> ```

---

## Quick Start Guide

### 1. Choose Your Project Mode
When you open Turin, you can choose between two modes:
*   **Temporary Project Mode**: Memory-only session. No keys or tokens required. All local session logs and intercepted history are destroyed immediately upon exiting the app (ideal for quick, single-target assessments).
*   **Permanent Mode**: Persists database records locally and connects to the **xcomrade.tech** sync engine. Requires you to paste your session token from `https://xcomrade.tech/settings`.

### 2. Configure Your Browser
To intercept SSL/TLS traffic:
1. Open the **Proxy Settings** panel in Turin and click **Download CA Certificate**.
2. Import the certificate into your browser's Trust Store (e.g., Firefox ➔ Settings ➔ Certificates ➔ View Certificates ➔ Authorities ➔ Import).
3. Set your browser's proxy configurations to:
   * **Host**: `127.0.0.1`
   * **Port**: `8080` (or your configured proxy port)

---

##  System Requirements
*   **Operating System**: Linux x86_64 desktop env (Kali, Debian, Ubuntu, Mint, Fedora, Arch).
*   **GUI Libraries**: `libwebkit2gtk-4.0` or `libwebkit2gtk-4.1` (installed by default on desktop environments).
*   **Browser**: Chromium, Google Chrome, or Firefox.

---

##  Support & Feedback
*   To report bugs or security issues with the tool, please contact **security@xcomrade.tech**.
*   For documentation, manuals, and integrations, visit [XC0MRADE](https://xcomrade.tech/turin).
