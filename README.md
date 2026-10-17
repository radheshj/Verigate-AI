# VERIGATE AI — Serverless Identity Screening Platform


![Architecture](https://img.shields.io/badge/Architecture-100%25%20Serverless-emerald?style=for-the-badge)
![AI Engine](https://img.shields.io/badge/OCR%20Engine-Grok%20Qwen%203.8-blue?style=for-the-badge)
![Forensics](https://img.shields.io/badge/Forensics-PyScript%20%2F%20WASM-orange?style=for-the-badge)
![Biometrics](https://img.shields.io/badge/Biometrics-face--api.js%20(WebGL)-purple?style=for-the-badge)

Verigate AI is a privacy-first, zero-infrastructure identity verification and border defense engine. Built to operate **100% client-side** directly inside the browser, it combines multimodal vision AI, WebAssembly-powered Python forensics, WebGL biometrics, and algorithmic rule checking to deliver sub-second document authentication without requiring a dedicated backend server or database.

---

## 🚀 Key Features

* **Multimodal Vision OCR:** Powered by the Grok's Qwen API (`qwen-3.8`), extracting identity fields (Passport Number, Name, DOB, Expiry, Sex, MRZ strings) into structured JSON payloads in under 1s.
* **ICAO 9303 Checksum Engine:** Pure JavaScript implementation of official ICAO 9303 modulo 10 checksum algorithms using 7, 3, 1 weighting multipliers to catch altered text and expired credentials.
* **Browser-Native ELA Image Forensics:** Executes Error Level Analysis (ELA) inside the browser via PyScript (WebAssembly) running `forensics.py` and Pillow (PIL) to isolate compression discrepancies and detect tampered details.
* **WebGL 1:1 Facial Matching:** Captures live traveler feeds via WebRTC and compares 128-dimensional facial landmark embeddings against cropped ID photos using `face-api.js`.
* **Composite Threat Scoring & Audit Trail:** Calculates a composite risk score (0–100) based on checksum integrity, document expiry, ELA variance, and facial similarity, saving logs locally via `localStorage` with full JSON report export.

---

## 🛠️ Tech Stack

| Component | Technology / Library |
| :--- | :--- |
| **Frontend UI** | Vanilla JavaScript (ES6 Modules), HTML5, Tailwind CSS |
| **Design & Icons** | Lucide Icons, Custom Light/Dark CSS Variable Engine |
| **Vision OCR Engine** | Grok's Qwen API (`qwen-3.8`) via Client-Side REST Fetch |
| **Browser Python Runtime** | PyScript (WebAssembly) running `forensics.py` & Pillow (PIL) |
| **Client Biometrics** | `face-api.js` (WebGL, SSD MobileNet v1) |
| **State & Persistence** | Browser Web Storage API (`localStorage`) |

---

## ⚡ Quick Start  
1. Clone the Repository.
2. Run the Application.  
   VS Code: Right-click index.html and click Open with Live Server.
3. Configure Grok API Key.
   Paste your API key into the Grok Key... input field in the top navigation bar and click Save.

The key will be stored securely inside your browser's localStorage and never sent to external server backends.
   
