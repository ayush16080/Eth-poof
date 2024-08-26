# myToken Contract

## Overview

The `myToken` contract is a basic Solidity implementation of a token with functionality for minting and burning. It tracks the total supply and individual balances of the tokens.

## License

This contract is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Prerequisites

- Solidity version 0.8.18 or higher

## Contract Details

### Variables

- `string public tokenName`: The name of the token, initialized to `"Ayush"`.
- `string public tokenAbbrevation`: The abbreviation of the token, initialized to `"AY"`.
- `uint public totalSupply`: The total supply of tokens, initialized to `0`.
- `mapping(address => uint) public balances`: A mapping that stores the balance of each address.

### Functions

#### `minting(address _address, uint _value) public`

- **Description**: Mints `_value` tokens to the specified `_address`.
- **Parameters**:
  - `_address`: The address to which tokens will be minted.
  - `_value`: The number of tokens to mint.
- **Functionality**:
  - Increases `totalSupply` by `_value`.
  - Adds `_value` to the balance of `_address`.

#### `burning(address _address, uint _value) public`

- **Description**: Burns `_value` tokens from the specified `_address`.
- **Parameters**:
  - `_address`: The address from which tokens will be burned.
  - `_value`: The number of tokens to burn.
- **Functionality**:
  - Checks if the balance of `_address` is greater than `_value`.
  - If true:
    - Decreases `totalSupply` by `_value`.
    - Subtracts `_value` from the balance of `_address`.

# Author
Ayush Guleria
