#     Create A Token

This Solidity program creates a token and a contract to mint and burn. It is a straightforward Solidity program.
## Description

Solidity, a programming language for creating smart contracts on the Ethereum blockchain, was used to create this straightforward contract. The contract Mytoken includes three variables for the token Name, Token Abbreviation, and Total Supply, as well as two functions: mint, which takes two arguments for address and value and adds the Total Supply to that value, and bunt, which, where possible, takes the Total Supply out of the value passed. This software acts as an easy-to-understand primer on Solidity programming and can be used as a launching pad for more difficult projects in the future.

## Getting Started
To run this program, use Remix, an online Solidity IDE. Visit the Remix website at https://remix.ethereum.org to get started.
we have to create a new file 'Create a token' and write the below code to the GitHub

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

string public tokenName = "Likhith";
string public tokenAbbr = "MVR";
uint public totalSupply = 0;

mapping (address => uint) public balances;


function mint(address Address, uint Value) public {
    totalSupply += Value;
    balances[Address] += Value;
}

function burn(address Address, uint Value) public {
    if(balances[Address] >= Value){
    totalSupply -= Value;
    balances[Address] -= Value;
    }
}
}

```
### Executing program
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "My Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "My token" contract in the left-hand sidebar, and then click on the token name, token abbr, total Supply, and then click on the "mint" and "burn functions and pass the parameters to the function. Finally, click on the "transact" button to execute the function and retrieve the "total supply" to know the value.
