# MedLedger
# 💊 MediLedger - Blockchain Medicine Authenticity Tracker

MediLedger is a hackathon project that creates a transparent and trustworthy medicine supply chain powered by blockchain technology. Our mission is to fight counterfeit medicines and ensure every drug is authentic, traceable, and safe through instant QR-based verification.

## 🚀 The Problem

The global supply chain for pharmaceuticals is plagued by counterfeit drugs, which pose significant health risks to consumers and damage the reputation of legitimate manufacturers. It's often impossible for a consumer or even a pharmacist to verify if a product is authentic, as traditional packaging can be easily replicated.

## ✨ Our Solution

MediLedger solves this problem by creating an immutable, decentralized ledger for every batch of medicine.

* **Decentralized Trust**: By using a public blockchain (Polygon), no single entity can tamper with a product's record.
* **Verifiable Authenticity**: Every new medicine batch is registered on-chain, creating a unique, traceable digital identity.
* **Instant Verification**: A simple QR code scan with any smartphone camera allows anyone to instantly verify a product's details against the secure blockchain record.

## 🛠️ Tech Stack

* **Smart Contract**: Solidity
* **Blockchain**: Polygon Mumbai Testnet
* **Frontend**: HTML, Tailwind CSS, Vanilla JavaScript
* **Blockchain Interaction**: Ethers.js
* **QR Code Functionality**: `qrcode.js`, `html5-qrcode`

## 🏃‍♀️ How to Run the Project

To run this project, you will need the [MetaMask](https://metamask.io/) browser extension.

1.  **Clone the Repository**
    ```bash
    git clone [Your-GitHub-Repo-URL]
    ```

2.  **Configure MetaMask**
    * Add and switch to the **Polygon Mumbai** test network.
    * Get free test MATIC from a public faucet like [mumbaifaucet.com](https://mumbaifaucet.com/) to pay for transaction fees.

3.  **Run the Application**
    * Simply open the `index.html` file in a web browser (like Chrome or Firefox).

## 🎬 How to Use the App

1.  **Connect Wallet**: Click the "Connect MetaMask" button to link your wallet.
2.  **Add a Medicine Batch**:
    * In the "Add Medicine" tab, enter the medicine's name and its batch ID.
    * Click "Add to Blockchain" and confirm the transaction in MetaMask.
    * Once the transaction is complete, a unique QR code will be displayed.
3.  **Verify a Medicine Batch**:
    * Navigate to the "Verify Medicine" tab.
    * Click "Start Scan" and point your camera at the generated QR code.
    * The app will instantly retrieve the product's details from the blockchain and display them, confirming its authenticity.
