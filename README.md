# Lottery Smart Contract

This repository contains a simple Ethereum smart contract written in Solidity for a lottery game.

## Directory Structure

- Lottery_Smart_Contract
  - contracts
    - Lottery.sol
  - test
    - Lottery.test.js
  - compile.js
  - deploy.js


## Contract Details

- **Solidity Version**: ^0.4.17
- **Contract Name**: Lottery

### Features

- **Manager**: The contract creator is designated as the manager.
- **Players**: Anyone can enter the lottery by sending a minimum of 0.01 ether.
- **Random Winner Selection**: A random player is selected to win the total pot.
- **Reset Players List**: After selecting a winner, the list of players is reset.

### Functions

- `enter()`: Allows a player to enter the lottery by sending the required amount of ether.
- `pickWinner()`: Randomly selects a winner and sends the total pot to the winner's address.
- `getPlayers()`: Returns the list of players who have entered the lottery.

## Compilation

To compile the Solidity smart contract, use the `compile.js` script provided in the repository.

### Steps to Compile

1. **Navigate to the Repository**
    ```bash
    cd Lottery_Smart_Contract
    ```

2. **Run the Compilation Script**
    ```bash
    node compile.js
    ```

This will compile the `Lottery.sol` contract and produce the ABI and bytecode required for deployment.

## Deployment

To deploy the compiled smart contract to an Ethereum network, use the `deploy.js` script provided in the repository.

### Steps to Deploy

1. **Update the Mnemonic and Infura API Key**
   
   Replace `"your 12-word mnemonic"` and `"https://mainnet.infura.io/v3/YOUR_INFURA_API_KEY"` with your actual mnemonic and Infura API key in the `deploy.js` file.

   ```javascript
   const provider = new HDWalletProvider(
     "your 12-word mnemonic",
     "https://mainnet.infura.io/v3/YOUR_INFURA_API_KEY"
   ); ```
   
2. **Navigate to the Repository**
       ```bash
    cd Lottery_Smart_Contract
    ```
3. **Run the Deployment Script**
    ```bash
    node deploy.js
    ```
