# 💊 MedLedger: An ICP-Based Medicine Authenticity Tracker

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Build: Passing](https://img.shields.io/badge/Build-Passing-brightgreen.svg)
![Powered by: ICP](https://img.shields.io/badge/Powered%20by-Internet%20Computer-blueviolet.svg)

> **Our Mission**: To restore trust in the pharmaceutical supply chain and save lives by providing a transparent, secure, and user-friendly system for verifying the authenticity of medicines.

MedLedger is a decentralized application designed to combat the global crisis of counterfeit medicines. By leveraging the unique capabilities of the **Internet Computer Protocol (ICP)**, we have built a fully on-chain solution that tracks medicine batches from manufacturer to consumer.

---

## 📺 Presentation

For a detailed explanation and a visual walkthrough of the project, please view our presentation slides:

[**MedLedger Pitch Deck**](https://docs.google.com/presentation/d/1X9amyUc08xmExICqfaDQ7CMYm-_P0ap6/edit?usp=sharing&ouid=100103825555716073583&rtpof=true&sd=true)

---

## 🚀 The Problem

The global supply chain for pharmaceuticals is plagued by counterfeit drugs, which pose significant health risks to consumers and damage the reputation of legitimate manufacturers. It's often impossible for a consumer or even a pharmacist to verify if a product is authentic, as traditional packaging can be easily replicated. This opacity creates a critical trust deficit in a system where lives are at stake.

---

## ✨ Our Solution

MedLedger solves this problem by creating an **immutable and decentralized ledger** for every single batch of medicine. Our solution provides:

* **Decentralized Trust**: By using the Internet Computer, no single entity can tamper with a product's record. All data is transparent and verifiable by anyone.
* **Verifiable Authenticity**: Every new medicine batch is registered on-chain, creating a unique, traceable digital identity that follows it through the supply chain.
* **Instant Verification**: A simple QR code scan with any smartphone camera allows consumers, pharmacists, and regulators to instantly verify a product's details against the secure blockchain record.

---

## 🏛️ Architecture Overview

Our application is built entirely on the **Internet Computer**, utilizing its full-stack decentralization capabilities. This means both our frontend and backend logic are hosted on-chain.

### Frontend Canister (`medledger_frontend`)
This canister serves our complete frontend user interface, including all HTML, CSS, and JavaScript assets. By hosting the UI directly on-chain, ICP provides unparalleled security and resistance to tampering, ensuring that the application users interact with is the genuine, untampered version.

### Backend Canister (`medledger_backend`)
This **Motoko** canister contains the core business logic and data management for our application.
* **Data Storage**: All medicine data (ID, name, batch ID, manufacturer, timestamp) is stored directly within the canister's **stable memory**. This showcases a key ICP advantage: the ability to store large amounts of data on-chain affordably and efficiently, eliminating the need for external storage solutions like IPFS.
* **Core Functions**: Includes `addMedicine` for authenticated manufacturers to add new batches and a public `getMedicine` query function that allows anyone to verify a product.

---

## 💡 Key ICP Features Used

* **On-Chain Website Hosting**: Our entire frontend is served directly from a canister, providing a seamless and highly secure user experience.
* **Canister Smart Contracts**: All backend logic and data are encapsulated within a powerful Motoko canister.
* **Stable Data Storage**: We leverage stable memory to ensure our medicine data persists across canister upgrades, providing essential long-term reliability.
* **Internet Identity (Planned)**: The system is designed for future integration with Internet Identity to provide secure, passwordless authentication for manufacturers.

---

## 🛠️ Tech Stack

* **Blockchain**: Internet Computer Protocol (ICP)
* **Backend Language**: Motoko
* **Frontend**: HTML, CSS, JavaScript
* **Development SDK**: DFINITY Canister SDK (`dfx`)

---

## 🚀 Getting Started (Local Development)

To build and deploy this project locally, you will need the DFINITY Canister SDK (`dfx`).

1.  **Clone the repository:**
    ```bash
    git clone [Your-GitHub-Repo-URL]
    cd medledger-project
    ```

2.  **Start the local replica:**
    This command starts a local instance of the Internet Computer running in the background.
    ```bash
    dfx start --background
    ```

3.  **Deploy the canisters:**
    This command builds and deploys both the frontend and backend canisters to your local replica.
    ```bash
    dfx deploy
    ```

---

## 🌱 Future Roadmap

* **Full Internet Identity Integration**: Implement a robust login system for manufacturers to ensure only authorized entities can add new medicines.
* **HTTP Outcalls**: Use HTTP outcalls to integrate with external government or regulatory APIs, allowing for real-time cross-referencing of manufacturer licenses.
* **On-Canister QR Generation**: Explore generating the QR code SVG data directly within the Motoko canister to further decentralize all application assets.
* **Mainnet Deployment**: After further testing and refinement, deploy the canisters to the ICP mainnet for public use.

---

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
