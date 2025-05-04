# Decentralized Blockchain Voting System

A secure, transparent voting platform built on blockchain technology that enables tamper-proof elections with verifiable results.

## Features
- End-to-end encrypted voting
- Immutable vote recording on blockchain
- Voter identity verification
- Real-time results dashboard
- Transparent audit trail

## Technologies
- **Blockchain**: Ethereum/Solidity smart contracts
- **Frontend**: React.js with Web3.js/ethers.js
- **Backend**: Node.js/Express (if applicable)
- **Storage**: IPFS for decentralized document storage
- **Authentication**: Cryptographic signatures

## Getting Started
1. Clone this repository
2. Install dependencies:
   ```
   cd Client && npm install
   cd ../Blockchain && npm install
   ```
3. Start local blockchain:
   ```
   npx hardhat node
   ```
4. **Set up MetaMask:**
   - Install the [MetaMask browser extension](https://metamask.io/).
   - Create a new wallet or import one of the test accounts provided by Hardhat (private keys are shown in your terminal after running `npx hardhat node`).
   - Add a new network in MetaMask:
     - **Network Name:** Localhost 8545
     - **New RPC URL:** http://127.0.0.1:8545
     - **Chain ID:** 31337
     - **Currency Symbol:** ETH
   - Switch to this network in MetaMask.

5. Deploy contracts:
   ```
   npx hardhat run scripts/deploy.js --network localhost
   ```
6. Run frontend:
   ```
   cd Client && npm start
   ```

## Casting a Vote
1. Open the voting portal at [http://localhost:3000](http://localhost:3000).
2. Connect your MetaMask wallet when prompted.
3. Select the active election from the dropdown menu.
4. Choose your candidate and click "Vote".
5. MetaMask will prompt you to confirm the transaction. Review and confirm.
6. Wait for the transaction to be mined (a notification will appear).
7. Your vote is now recorded on the blockchain. Results update in real time.

**Note:**
- Each vote is a blockchain transaction and will require a small amount of ETH (provided by your local Hardhat node).
- Votes are immutable and cannot be changed once confirmed.
- If you encounter issues, ensure MetaMask is connected to the correct network and has sufficient test ETH.

## License
MIT
