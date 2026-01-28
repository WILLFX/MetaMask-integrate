This project demonstrates how to integrate MetaMask with WalletConnect v2 in a bare HTML dapp. It allows users to connect their MetaMask wallet, switch to the Sepolia test network (if not already on it), and view their balance on the Sepolia network using WalletConnect.

The dapp is hosted and accessible on GitHub Pages at:

Dapp URL: https://willfx.github.io/MetaMask-integrate/

Features:

MetaMask connection via WalletConnect v2: Easily connect your MetaMask wallet using WalletConnect.

Auto-switch to Sepolia: The dapp automatically prompts the user to switch to the Sepolia test network if it’s not already active in MetaMask.

Display Balance: Once connected to Sepolia, the user's balance in ETH is shown.

Getting Started
1. Prerequisites

To use this dapp, you will need:

MetaMask app installed on your mobile device.

A WalletConnect-compatible wallet (like MetaMask).

Sepolia test network configured on MetaMask (this will be handled automatically if not already set up).

2. How to Connect to MetaMask:

Visit the hosted dapp URL: https://willfx.github.io/MetaMask-integrate/
.

Click the Connect button to initiate the connection to your MetaMask wallet using WalletConnect.

Once connected, MetaMask will ask you to approve the connection.

After approval, the dapp will automatically prompt for Sepolia network switching if necessary, and the Sepolia test network will be activated in MetaMask.

Your Sepolia ETH balance will be displayed on the dapp once the network switch is complete.

3. How to Switch to Sepolia:

After connection approval, if you're not already on the Sepolia test network, MetaMask will ask you to switch networks.

Once approved, the Sepolia network will be selected, and your Sepolia balance will be shown in the dapp.

4. Troubleshooting:

If MetaMask does not prompt you to switch networks, ensure that the Sepolia RPC URL is correctly set up in your MetaMask wallet.

If the network switch is not successful, check that you approved the request in MetaMask.

How the Code Works:
WalletConnect Integration:

The dapp uses WalletConnect v2 to interact with MetaMask. Here's a brief breakdown of how it works:

Connect Button: The "Connect" button triggers the WalletConnect connection via a deep link (metamask://wc?uri= or https://metamask.app.link/wc?uri=).

Display URI: WalletConnect generates a URI which MetaMask reads to establish a secure connection.

Network Switching: Once the connection is established, the dapp checks if the Sepolia network is active. If not, it triggers a network switch using the wallet_switchEthereumChain and wallet_addEthereumChain methods.

Balance Retrieval: After switching to Sepolia, the user's balance in ETH is fetched and displayed on the dapp.

Deep Link Implementation:

MetaMask Deep Link is used to handle the connection and chain-switching requests directly inside MetaMask:

Scheme link: metamask://wc?uri=<walletconnect_uri>

Universal link: https://metamask.app.link/wc?uri=<walletconnect_uri>

The code follows these steps:

Connect MetaMask using WalletConnect.

Switch to Sepolia if necessary.

Fetch and display the balance once connected to Sepolia.

License

This project is open-source and available under the MIT License.
