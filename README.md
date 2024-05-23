
META Token Contract
Overview
The META Token Contract is a basic Ethereum smart contract designed for creating, minting, and burning a custom token called "META".

Contract Description
This Solidity contract allows users to create a custom token on the Ethereum blockchain. It includes functionalities to mint new tokens, thereby increasing the total supply, and to burn tokens, reducing the total supply. The contract also maintains a record of each address's token balance.

Contract Details
Public Variables
tokenName: Stores the name of the token. In this contract, it's set to "META".
tokenAbbrv: Stores the abbreviation of the token. In this contract, it's set to "MTA".
totalSupply: Stores the total supply of tokens. Initially set to 0.
Mapping
balances: Maps addresses to their respective token balances.
Functions
Mint Function
solidity
Copy code
function mint(address _address, uint256 _value) public {
    totalSupply += _value;
    balances[_address] += _value;
}
Increases the total supply of tokens by _value.
Increases the balance of _address by _value.
Burn Function
solidity
Copy code
function burn(address _address, uint256 _value) public {
    if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
Checks if the balance of _address is greater than or equal to _value.
Decreases the total supply of tokens by _value.
Decreases the balance of _address by _value.
