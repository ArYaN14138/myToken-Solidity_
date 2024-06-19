# metacrafters_ETH_PROOF_Project
This report contains project assessment code for the ETH PROOF: Beginner EVM course under metacrafter.

# Code outline

- Public variables to store token details
- A mapping to track balances.
- A mint function to add tokens.
- A burn function to destroy tokens, with a check to ensure the sender has enough balance.

# MyToken Smart Contract

# Description
This smart contract implements a simple token system with mint and burn functionalities. It is built on the Ethereum blockchain using Solidity.

# Features
  - Public variables to store token details:
  - `MyToken`: The name of the token (e.g., "matic").
  - `MTK`: This variable holds the symbol of the token.
  - `totalSupply`: The total supply of the token.
- A mapping to store the balance of each address.
- `mint` function to create new tokens and assign them to an address.
- `burn` function to destroy tokens from an address, with a check to ensure sufficient balance.

# Functions

# mint
solidity
function mint(address to, uint256 value) public {
    totalSupply += value;
    balances[to] += value;
    emit Mint(to, value);
}


This function mints new tokens, increasing the totalSupply and the balance of the specified address. It also emits the Mint event.

# Burn
- function burn(address from, uint256 value) public {
    require(balances[from] >= value, "Insufficient balance to burn");
    totalSupply -= value;
    balances[from] -= value;
    emit Burn(from, value);
}

This function burns tokens, decreasing the totalSupply and the balance of the specified address, provided the address has enough tokens. It emits the Burn event to log the action.

# Deployment

- Ensure you have Solidity 0.8.18 installed.
- Compile the contract using a Solidity compiler.
- Deploy the contract to your preferred Ethereum network.

# Usage

- Use the mint function to create new tokens and assign them to a specific address.
- Use the burn function to destroy tokens from a specific address, ensuring the address has enough tokens to burn.

# Project by

- Aryan
