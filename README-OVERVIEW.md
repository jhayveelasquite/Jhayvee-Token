# Jhayvee-Token

Simple overview of use/purpose. Hello! The purpose of this code is to create a token on the etherum blokchain. It makes operations like minting the generation of new tokens and buring the destruction of old tokens much easier. This spacific token is called "Jhayve-Token" and its acronym is "JT". It keeps an eye on each address's balance as well as the overall supply.

## Description

An in-depth paragraph about your project and overview of use. Essential token functionality on the Etherum network are provided by the Mytoken contract named "Jhayvee-Token" (JT). It uses mappings to keep track of user balance and uses public variables to establish the token's name, abbreviation, and total supply.

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

In order to use this tool, you must comprehend and closely adhere to the given instructions.
• Make sure your smart contract is deployed on the blokchain network in the appropriate context.
• You will find the following steps in your contact:
  
  Step A: TokenName and tokenAbbrv variables can be updated to change the name and abbreviation of your token.

  Set B: Update the totalSupply variable to determine the token's initial supply.
  
  Set C: Use the mint function to add addresses and their respective amounts.
  
  Set D: Using the burn function, choose addresses and start the token reduction process.

```
code blocks for commands
 // SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleToken {
    string public name = "Jhayvee-token;
    string public symbol =" JT";
    uint256 public totalSupply;

    mapping(address => uint256) public balances;

    event Transfer(address indexed _from, address indexed _to, uint256 _value);

    constructor(string memory _name, string memory _symbol, uint256 _totalSupply) {
        name = _name;
        symbol = _symbol;
        totalSupply = _totalSupply;
        balances[msg.sender] = _totalSupply;
    }

    function transfer(address _to, uint256 _value) public {
        require(balances[msg.sender] >= _value, "Insufficient balance");
        require(_to != address(0), "Invalid recipient");
        
        balances[msg.sender] -= _value;
        balances[_to] += _value;
        
        emit Transfer(msg.sender, _to, _value);
    }
}
```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

Here are some pointers for dealing with typical issues.

Make sure your permissions are correct if you are having trouble accessing your token.

Verify your functions for potential misuse or minor details if there are mistakes occurring during the minting and burning of tokens.

To prevent compilation and runtime issues in your smart contract, make sure your variables and data types are accurate.

Be cautious in evaluating your conditions and assertions to avoid potential security and safety issues.

If you're having trouble getting your smart contract to execute and function, just use debugging tools like Ganache to examine and verify the code you wrote and spot any possible flaws.

## Authors

Contributors names and contact info

 [NTC-S] Jhayvee C. Lasquite 
  422001114@ntc.edu.ph


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
