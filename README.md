# DengenToken Smart Contract
## Overview
The DengenToken smart contract is an ERC20 token implementation with additional functionalities for minting, burning, and redeeming tokens. The contract allows the owner to mint tokens, and any user can burn or redeem tokens. Redeemed tokens are recorded for each user and can be retrieved or printed.

### Features
- Minting: Only the contract owner can mint new tokens.
- Burning: Any token holder can burn their tokens.
- Redeeming: Token holders can redeem tokens, and the details of the redemption are stored.
- Transfer: Tokens can be transferred between addresses.
- Balance Check: The balance of any address can be checked.
- Redeemed Items Retrieval: Retrieve and print the details of redeemed tokens for any address.
  
### Prerequisites
- Node.js
- npm
- Truffle
- Ganache or any Ethereum test network
- OpenZeppelin Contracts

## Getting Started
### Installing
This program runs on EVM along with ".sol" as extension. We can either run it on websites like Remix or even on Visual Studios.
### Executing program
We need a solidity compatible virtual machine in order to run this program. Create a new file with ".sol" extension
```
