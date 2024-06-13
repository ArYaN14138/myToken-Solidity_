// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18; // This part specifies the Version and  compiled with Solidity version 0.8.18.



contract MyToken {
//This starts the definition of the MyToken contract.
    // Public variables to store the details about the token
    string public name = "MyToken";
    string public symbol = "MTK";
    uint256 public totalSupply;

    // This line creates a mapping called balances that maps addresses to their respective token balances
    mapping(address => uint256) public balances;

    // These lines define two events, Mint and Burn, which log the minting and burning of tokens.
// The indexed keyword allows these events to be searchable by address.

    event Mint(address indexed to, uint256 value);
    event Burn(address indexed from, uint256 value);

    // Mint function to increase total supply and balance of an address
    //This function mints new tokens.
    function mint(address to, uint256 value) public {
        totalSupply += value;
        balances[to] += value;
        emit Mint(to, value);
    }

    // Burn function to decrease total supply and balance of an address
    //This function burns  tokens. 
    function burn(address from, uint256 value) public {
        require(balances[from] >= value, "Insufficient balance to burn");
        totalSupply -= value;
        balances[from] -= value;
        emit Burn(from, value);
    }
}
