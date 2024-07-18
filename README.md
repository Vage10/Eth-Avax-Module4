# Eth-Avax-Module4
Overview

The DengenToken smart contract is an implementation of an ERC-20 token with additional functionality for token redemption. The contract is built using Solidity and leverages the OpenZeppelin library for standard token operations and ownership management. The token is named "Degen" and has the symbol "DGN".

Features

Minting: The owner can mint new tokens to a specified address.
Burning: Users can burn their tokens to reduce the total supply.
Redeeming: Users can redeem tokens for items, which burns a specified number of tokens from their balance.
Tracking Redeemed Items: The contract maintains a record of redeemed items for each user.
Balance Check: Users can check their token balance.
Token Transfer: Tokens can be transferred between addresses with support for allowance.

Contract Details

Variables
tokenCost: The cost of redeeming tokens, set to 1 by default.
redeemedItems: A mapping to track redeemed items for each user.

Events
TokensRedeemed: Emitted when tokens are redeemed by a user.

Functions
Constructor
constructor() ERC20("Degen", "DGN") Ownable(msg.sender)

Initializes the token with the name "Degen" and symbol "DGN". Sets the contract deployer as the owner.

Minting
function mint(address to, uint256 amount) public onlyOwner

Mints new tokens to the specified address. Only the owner can call this function.

Burning

function burn(uint256 amount) public

Burns the specified amount of tokens from the caller's balance.

Redeeming

function redeem(uint256 amount) public

Redeems the specified amount of tokens. The cost is calculated as amount * tokenCost and the tokens are burned from the caller's balance. The redeemed items are recorded.

Get Redeemed Items

function getRedeemedItems(address account) public view returns (RedeemedItem[] memory)

Returns the list of redeemed items for the specified account.

Print Redeemed Tokens

function printRedeemedTokens(address account) public view returns (string memory)

Returns a string representation of the redeemed tokens for the specified account.

Utility Functions

function uintToString(uint256 v) internal pure returns (string memory)

Converts a uint256 value to a string.

Balance Check

function checkBalance(address account) public view returns (uint256)

Returns the token balance of the specified account.

Token Transfer

function transferTokens(address from, address to, uint256 amount) public

Transfers tokens from one address to another. Supports transfers from an address by the owner of the tokens or via allowance.

Usage

Deployment: Deploy the contract to the Ethereum blockchain.
Minting Tokens: The owner can mint tokens to any address using the mint function.
Burning Tokens: Users can burn their tokens using the burn function.
Redeeming Tokens: Users can redeem their tokens using the redeem function. The cost is calculated based on the tokenCost variable.
Checking Balance: Users can check their token balance using the checkBalance function.
Transferring Tokens: Tokens can be transferred between addresses using the transferTokens function.
Prerequisites
Solidity ^0.8.0
OpenZeppelin Contracts
Installation
Install OpenZeppelin Contracts:

npm install @openzeppelin/contracts
Deploy the Contract: Use a tool like Truffle or Hardhat to deploy the contract to your desired network.

License

This project is licensed under the MIT License. See the LICENSE file for details.

Author

Vageshwari Chaudhary
