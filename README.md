# MyToken 🌟

This Solidity contract defines a simple token with basic minting and burning functionalities. The purpose of this contract is to demonstrate the fundamental principles of creating a token, managing its supply, and modifying account balances in the Solidity programming language.

## Description 📜

The `MyToken` contract is a straightforward implementation of a token on the Ethereum blockchain. It includes:

1. **Public Variables**: 
   - `tokenName` - The name of the token.
   - `tokenAbbrv` - The abbreviation of the token.
   - `totalSupply` - The total supply of the token.

2. **Mapping**:
   - `balances` - A mapping of addresses to their respective token balances.

3. **Mint Function**: 
   - Increases the total supply and the balance of the specified address.

4. **Burn Function**: 
   - Decreases the total supply and the balance of the specified address, ensuring that the balance is sufficient before burning.

## Getting Started 🚀

### Prerequisites 🛠️

To compile and deploy this contract, you will need:

- An Ethereum development environment such as [Remix](https://remix.ethereum.org/), [Truffle](https://www.trufflesuite.com/truffle), or [Hardhat](https://hardhat.org/).
- MetaMask or any other Ethereum wallet to interact with the contract.

### Executing the Program 🏃‍♂️

#### Using Remix 🖥️

1. **Open Remix**: Go to [Remix IDE](https://remix.ethereum.org/).

2. **Create a New File**: 
   - Click on the "+" icon in the left-hand sidebar.
   - Name the file `MyToken.sol`.

3. **Copy and Paste the Code**:
   ```solidity
   // SPDX-License-Identifier: MIT
   pragma solidity >=0.6.12 <0.9.0;

   contract MyToken {
       // public variables here
       string public tokenName = "META";
       string public tokenAbbrv = "MTA";
       uint256 public totalSupply = 0;

       // mapping variable here
       mapping(address => uint256) public balances;

       // mint function
       function mint(address _address, uint256 _value) public {
           totalSupply += _value;
           balances[_address] += _value;
       }

       // burn function
       function burn(address _address, uint256 _value) public {
           if (balances[_address] >= _value) {
               totalSupply -= _value;
               balances[_address] -= _value;
           }
       }
   }

Authors ✍️

[Mohan-duhan](https://github.com/Mohan-duhan)

License 📄

This project is licensed under the MIT License - see the LICENSE.md file for details.




