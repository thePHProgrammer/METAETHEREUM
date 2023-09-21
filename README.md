# BATSHEBA Token
This Solidity program is a simple ethereum token contract program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how ethereum works.
# DESCRIPTION
This Solidity program is a basic Ethereum token contract designed to create and manage a simple cryptocurrency named "Batsheba" with the symbol "BSBA." This contract includes essential functions for minting (creating) and burning (destroying) tokens.
# GETTING STARTED
## Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., BATSHEBA.sol). Copy and paste the following code into the file:
```solidity
contract MyToken {

    // public variables here
    string public tokenName = "Batsheba";
    string public tokenAbbrv = "BSBA";
    uint public totalSupply = 0;
    
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public{
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public{
        if(balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once you have successfully compiled and deployed your MyToken contract to the Ethereum blockchain, you can start using it for various purposes, such as creating and managing your own cryptocurrency. 

Before you can interact with the contract, you need to deploy it to the Ethereum blockchain. You can do this using Ethereum development tools like Remix, Truffle, or Hardhat. Deploying the contract will result in a transaction on the Ethereum network, and you'll receive a contract address.

After deployment, you can interact with the contract using Ethereum wallets or other smart contract interaction tools. Here's how you can interact with the provided contract:

To mint  new tokens, you can use the mint function. Provide the Ethereum address where you want to send the tokens and the number of tokens to create as arguments.

To burn  tokens held by a specific address, you can use the burn function. Provide the address from which you want to burn tokens and the number of tokens to burn as arguments.

To burn  tokens held by a specific address, you can use the burn function. Provide the address from which you want to burn token and the number of tokens to burn as arguments.

# AUTHORS
Noriel Joy S. Embudo
Email:
202010306@fit.edu.ph
# LICENSE
This project is licensed under the Noriel License - see the LICENSE.md file for details
