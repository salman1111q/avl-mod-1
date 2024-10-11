# ERC20 Token and Vault Contract

This repository contains two Solidity contracts:

1. **ERC20**: A standard ERC20 token contract called "Solidity by Example" with the symbol "SOLBYEX". It implements basic token functionalities such as transfer, approve, transferFrom, mint, and burn.

2. **Vault**: A contract named Vault that facilitates the deposit and withdrawal of ERC20 tokens. It calculates the shares of deposited tokens based on the total supply and the amount of tokens deposited. Similarly, it calculates the amount of tokens to be withdrawn based on the shares redeemed and the current total supply.

## ERC20 Contract

### Functions
- `transfer`: Transfer tokens from the sender's account to another account.
- `approve`: Approve another address to spend tokens on behalf of the sender.
- `transferFrom`: Transfer tokens from one account to another if allowed by the sender.
- `mint`: Mint new tokens and assign them to the caller's account.
- `burn`: Burn tokens from the caller's account.

### Events
- `Transfer`: Triggered when tokens are transferred from one account to another.
- `Approval`: Triggered when the allowance of a spender is approved by the token owner.

## Vault Contract

### Constructor
- `constructor`: Initializes the Vault contract with the address of the ERC20 token.

### Functions
- `deposit`: Allows users to deposit ERC20 tokens into the Vault and receive shares in return.
- `withdraw`: Allows users to withdraw ERC20 tokens from the Vault by redeeming their shares.

### Internal Functions
- `_mint`: Mints shares for the user based on the amount deposited.
- `_burn`: Burns shares when a user withdraws tokens.

### State Variables
- `token`: Immutable variable storing the address of the ERC20 token.
- `totalSupply`: Total shares issued by the Vault.
- `balanceOf`: Mapping storing the balance of shares for each user.

## Usage
1. Deploy the ERC20 contract and mint initial tokens if needed.
2. Deploy the Vault contract, passing the address of the ERC20 contract to its constructor.
3. Users can deposit ERC20 tokens into the Vault using the `deposit` function and receive shares in return.
4. Users can withdraw ERC20 tokens from the Vault by redeeming their shares using the `withdraw` function.

## License
Both contracts are provided under the MIT License.

