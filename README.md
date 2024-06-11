# ETH_Beginner_project

This Solidity program is a simple program that demonstrates the transactions and functionality of the functions in Solidity programming language. The purpose of this program is to serve as the final project for our Ethereum Beginner Course using Solidity and to get a feel for how it works.

## Description

This program is a simple contract named "MyToken" written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract have firstly variables named tokenName as string, tokenAbbvas string and tokenSupply as uint also we had a balances variable used here for mapping the address then there are two functions present named "mint" and "burn" , this "mint" have two parameteres add of type address and value of uint type which are used to add the value in the given address and update the balance. The other program "burn" also have two parameters add of address type and value of uint type which are used to burn the amount which we enter in value parameter from the balance address and show the updated balance in it. This program serves as a simple and straightforward introduction to Solidity programming and using of functions , and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Installing

* To run the program we can use Remix, an online Soledity IDE which is an online platform where we can create and deploy our smart contract in a easy and fast way.
* To get started, go to the Remix website at https://remix.ethereum.org/ 

### Executing program

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Eth_Project.sol). Copy and paste the following code into the file

```
contract MyToken {

    // public variables here
    string public tokenName="Dogecoin";
    string public tokenAbbv="DC";
    uint public totalSupply = 1000;


    // mapping variable here
    mapping(address=> uint) public  balances;

    // mint function
    function mint(address add ,uint _value) public {
        totalSupply += _value;
        balances[add] +=_value;
    }
    // burn function
    function burn (address add, uint _value)public {
        if(balances[add]>= _value){
            totalSupply -= _value;
            balances[add] -= _value;

        }
    }

}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Eth_Project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Eth_Project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the various function types. Click on the "Eth_Project" contract in the left-hand sidebar, and then click on the "mint" function after adding the req details in it. Finally, click on the "transact" button to execute the function and the values will be updated in balances.

In the same way we can use "burn" function by putting the values in the columns and by clicking on "transact" the required function will execute and provide the result for it.

## Authors

Contributors names and contact info

Mukesh Arya
22bcs50149@gmail.com
