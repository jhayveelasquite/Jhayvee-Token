# Jhayvee-Token
Simple overview of use/purpose. Hello! The purpose of this code is to create a token on the etherum blokchain. It makes operations like minting the generation of new tokens and buring the destruction of old tokens much easier. This spacific token is called "Jhayve-Token" and its acronym is " MTJ". It keeps an eye on each address's balance as well as the overall supply.

# Description
An in-depth paragraph about your project and overview of use. Essential token functionality on the Etherum network are provided by the Mytoken contract named "jhayvee-Token" (MTJ). It uses mappings to keep track of user balance and uses public variables to establish the token's name, abbreviation, and total supply.

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

### Executing program

* How to run the program
* Step-by-step bullets
  ```
  code blocks for command
  contract SimpleToken {
    string public name;
    string public symbol;
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
command to run if program contains helper info


## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)
  [NTC-S] Jhayvee C. Lasquite 
  422001114@ntc.edu.ph

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
