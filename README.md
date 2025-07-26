<div align="center">

# 💊 MedLedger

**An immutable, on-chain ledger for verifying medicine authenticity on the Internet Computer.**

</div>

---

### Core Concept

| The Problem | Our Solution |
| :--- | :--- |
| The pharmaceutical market is flooded with **counterfeit drugs**, endangering lives and eroding trust. Traditional packaging is easy to fake, leaving consumers with no reliable way to verify authenticity. | We provide a **decentralized, tamper-proof record** for every medicine batch. By scanning a simple QR code, anyone can instantly verify a product's origin and details against a secure on-chain ledger. |

---

### How It Works

1.  **Registration**: A manufacturer authenticates and registers a new medicine batch via the MedLedger dApp.
2.  **On-Chain Record**: A new, immutable record is created in a backend **Motoko canister** running on the Internet Computer.
3.  **QR Code Generation**: A unique QR code, pointing to the verification record, is generated for the product's packaging.
4.  **Instant Verification**: A consumer scans the QR code with their phone, which calls a query function on the canister and instantly displays the authentic product details from the blockchain.

---

### Architecture & Tech Stack

This entire application is hosted on the **Internet Computer**, leveraging its ability to serve web assets and run backend logic from a unified, decentralized environment. We use a two-canister architecture: a **frontend canister** serves the UI directly to users, while a **backend canister** manages all data and business logic.

| Category | Technology Used |
| :--- | :--- |
| **Blockchain** | Internet Computer Protocol (ICP) |
| **Backend Language** | Motoko |
| **Frontend** | HTML, CSS, JavaScript (Served On-Chain) |
| **Development Tools** | `dfx` (DFINITY Canister SDK) |

---

### 🚀 Local Quick-Start

To run this project locally, you will need the `dfx` SDK.

1.  **Clone the repo:**
    ```bash
    git clone [Your-GitHub-Repo-URL] && cd [project-folder]
    ```
2.  **Start the local replica:**
    ```bash
    dfx start --background
    ```
3.  **Deploy the dApp:**
    ```bash
    dfx deploy
    ```
---

### 🌱 Project Roadmap

- [ ] **Phase 1: Secure Authentication**
    - Implement full Internet Identity integration for manufacturers.
- [ ] **Phase 2: External Integration**
    - Use HTTP outcalls to cross-reference manufacturer licenses with regulatory APIs.
- [ ] **Phase 3: Optimization**
    - Explore generating QR code SVG data directly inside the Motoko canister.
- [ ] **Phase 4: Mainnet Launch**
    - After rigorous testing, deploy the canisters to the ICP mainnet for public use.

---

<p align="center">Licensed under the MIT License.</p>
