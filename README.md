# MyToken


This Solidity program is a simple "MyToken" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to create our own token of whatever name we want  and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a mainly Two function that are "Mint" and "Burn" function, which is used to mint and burn the values. there are public variables like string, uint, etc, and even has the mapping of addressses to balances. This program is a simple and straightforward to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {
        // public variables here
     string public tokenName = "DAINIK-META";
     string public tokenAbbrv = "MTA";
     uint public totalSupply = 0;
     
    // mapping variable here
    mapping(address => uint) public balances;  

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it. After, that to check whether the contract is running successfully we can check by performing the minting and the burning function. We can check the TotalCount, TotalAbrrevation, Balance, too. After, the Deployment of Contract copy the initial address above and then paste down to the left-most side where u can see the TotalCount, TotalAbbrv, Balances, Mint, Burn, etc and then You can perform the basic task that the contract has. So, atlast we can see all the things are performed well and as said.

## Authors

Metacrafter Dainik  
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License.
