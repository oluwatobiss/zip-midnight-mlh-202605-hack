# ZIP — Zero-Exposure Identity Proof

**"Prove you're human. Reveal nothing else."**

ZIP is a privacy-first Proof-of-Humanity application built for the Midnight Hackathon. It demonstrates a powerful idea: users should be able to prove they are real humans to external applications without exposing any sensitive identity data (like passports, biometrics, or real names).

This project strongly aligns with the **Midnight Network's** privacy-first philosophy, utilizing the principles of Zero-Knowledge (ZK) cryptography.

---

## 🌟 The MVP Experience

This MVP focuses on emotional clarity and a seamless, premium user experience to communicate the power of zero-exposure proofs. 

It consists of three core flows:

1. **User Onboarding (Local Vault)**
   - Users create a secure local identity vault using a public alias.
   - Raw credentials never leave the browser. A local ZK key is derived and encrypted exclusively in the device's secure storage.
   - *Visualizes: Privacy-first design and local-only data retention.*

2. **Generate Human Proof (Selective Disclosure)**
   - Users can selectively disclose specific rules (e.g., "Proof of Humanity").
   - The application simulates compiling a ZK circuit and synthesizing a ZK-SNARK proof.
   - *Visualizes: Mathematical proof generation without exposing underlying data.*

3. **Connect to Demo App (Nova Social)**
   - "Nova Social" is a mocked, futuristic community platform experiencing bot attacks.
   - Users authenticate with their ZIP proof via a secure handshake.
   - *Visualizes: An external application definitively verifying humanity without ever learning the user's real identity.*

---

## 🏗️ Architecture & Tech Stack

To prioritize a highly polished, demo-ready experience, this MVP isolates the application logic in the browser while maintaining the foundation for future Midnight smart contract integration.

### Frontend (`/frontend`)
- **React 19 & TypeScript**: Component-driven architecture.
- **Vite**: Ultra-fast build tooling and hot-module replacement.
- **TailwindCSS v4**: Premium "Obsidian Dark" aesthetics, custom glassmorphism panels, and neon accents.
- **Framer Motion**: Fluid animations simulating cryptographic latency for an immersive experience.

### Backend & Midnight Infrastructure
This repository was originally scaffolded using `create-mn-app`. 
- **Simulated MVP Backend**: For the scope of this hackathon, real blockchain transactions are bypassed to ensure presentation speed and reliability. All cryptographic operations (vault generation, encryption, ZK-SNARK synthesis) are **simulated locally** in the browser via `frontend/src/services/zipCryptoService.ts`.
- **Future Integration**: The `contracts/` directory contains a sample Compact smart contract (`hello-world.compact`). Moving forward, this structure allows developers to easily swap the mocked `zipCryptoService` with the actual Midnight Compact SDK and live blockchain deployment scripts found in the `src/` and `scripts/` directories.

---

## 🚀 How to Run Locally

You can spin up the full ZIP MVP frontend in just a few seconds.

### Prerequisites
- Node.js (v18 or higher)
- npm

### Quick Start

1. **Navigate to the frontend directory:**
   ```bash
   cd frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```

4. **View the Application:**
   Open your browser and navigate to **[http://localhost:5173](http://localhost:5173)** to start the demo!

---

## 🛡️ ZIP Threat Guard (AI Feature)

The application includes a lightweight, simulated AI feature called the **Threat Guard**. Located on the Dashboard, it demonstrates how anomaly detection can monitor proof request velocity and prevent bot-like reuse of proofs—all executed entirely on the client side without inspecting raw identity data.

---
*Built for the Midnight MLH Hackathon 2026.*
