# MetaMask Integrate (WalletConnect + ethers.js)

Minimal one-page dApp that:
- Connects a mobile wallet (WalletConnect v2)
- Ensures **Sepolia** is selected
- Sends a small **test transfer from JavaScript (ethers.js)** after the user approves

Live demo: https://willfx.github.io/MetaMask-integrate/

## What it does
Single-button flow:
1. Open wallet selector (WalletConnect)
2. Connect wallet + approve in the wallet app
3. Switch / confirm **Sepolia (11155111)**
4. Create an **ethers.js signer** from the connected wallet provider
5. Send a test transaction from JS

## Tech
- WalletConnect Ethereum Provider (v2)
- ethers.js (v6)
- Static HTML (works on GitHub Pages)

## Configure
Edit `index.html`:

- WalletConnect Project ID:
  ```js
  const projectId = "YOUR_WALLETCONNECT_PROJECT_ID";
   # MetaMask Integrate (WalletConnect + ethers.js
  Sepolia recipient address:

const TO_ADDRESS = "0x...";

Amount (in wei):

const TEST_VALUE_WEI = "600000000000000"; // 0.0006 ETH
Run locally

Just open with a local server (recommended):

VS Code Live Server, or

python -m http.server

Then visit:

http://localhost:8000

Deploy (GitHub Pages)

Push to GitHub

Repo Settings → Pages → set source branch (e.g. main)

Open the GitHub Pages URL

Notes (mobile)

The wallet app must be installed on the phone

On Android, switching between Chrome and the wallet app may still require user action depending on OS/wallet behavior
