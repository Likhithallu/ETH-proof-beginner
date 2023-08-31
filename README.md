#     Create A Token

This Solidity program is a simple Solidity program to create a Token and a contract to mint and burn.

## Description

This program is a simple contract written in Solidity, a programming language for developing smart contracts on the Ethereum blockchain. The contract Mytoken has a 3 variable token Name, token Abbr, Total Supply, and 2 functions mint which has 2 parameters address and value which adds total supply to that value and we have a bunt function which subtracts the total supply from the value passed if possible. This program serves as a simple and straightforward introduction to Solidity programming and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

You can use Remix, an online Solidity IDE to run this program. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

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

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "My Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "Mytoken" contract in the left-hand sidebar, and then click on the "mint" and "burn functions and pass the parameters to the function. Finally, click on the "transact" button to execute the function and retrieve the "total supply" to know the value.
