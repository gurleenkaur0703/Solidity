# Solidity Contract for creating a Token
This Solidity contract shows the implementation of a basic token creation with minting and burning functionalities.

## Contract Description:

### Public Variables
#### •	token_name:
Name of the token.
#### •	token_abbrv:
Abbreviation or symbol of the token.
#### •	total_supply: 
Total supply of the token.

### Mapping
#### •	total_amt:
Mapping of addresses to balances of token holders).

### Functions
#### 1.	mint(address token_address, uint token_value):
#### •	Description:
Increases the total supply of the token and adds tokens to the balance of the specified address.
#### •	Parameters:
#### a)	token_address: 
Address to which tokens will be minted.
#### b)	token_value:
Amount of tokens to mint.

#### 2. burn(address token_address, uint token_value):
#### •	Description:
Decreases the total supply of the token and burns tokens from the balance of the specified address.
#### •	Parameters:
#### a)	token_address:
Address from which tokens will be burned.
#### b)	token_value:
Amount of tokens to burn.

## Getting Started

### Installing

•	Simply search for remix.ethereum.org in your web browser.	No installation is required.

### Executing program
• Open Remix IDE in your browser. Create a New File with .sol extention. Copy and paste the following code into the file:
```
contract Create_Token {
    // public variables here
            string public token_name  = "BITCOIN";
            string public token_abbrv = "BTC";
            uint public total_supply  = 0;
    // mapping variable here
            mapping(address => uint) public total_amt;  // total_amt here is balances
    // mint function
            function mint(address token_address, uint token_value) public 
               {
            total_supply += token_value;
            total_amt[token_address] += token_value;
               }
    // burn function
            function burn(address token_address, uint token_value) public 
              {
             if(total_amt[token_address] >= token_value)
               {
             total_supply -= token_value;
             total_amt[token_address] -= token_value;
               }
             }
    }
```
Compile and then deploy the Contract. Click on token_name, token_abbrv, and total_supply to see the initial values. 
Mint and burn tokens with your any address and value in the ‘mint’ and ‘burn’ function inputs. Click on mint button to see the increase in the total_supply and the balance of the 
specified address.

Similarly, click on burn button to see the decrease in the total_supply and the balance of the specified address if the balance is sufficient. Check total_supply 
and total_amt again to see the updated values after minting and burning.

## Authors

Gurleen Kaur
(@https://github.com/gurleenkaur0703)

## License

This project is licensed under the MIT License.
