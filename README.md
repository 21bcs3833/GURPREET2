# Smart Contract Project

## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This is a smart contract that implements the require(), assert() and revert() statements.

## Getting Started

### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:


## License

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract ErrorHandlingContract {

    function requireExample(uint256 x, uint256 y) public pure returns (uint256) {
        require(y != 0, "Division by zero is not allowed");
        return x / y;
    }
    
    function assertExample(uint256 a, uint256 b) public pure returns (uint256) {
        uint256 result = a + b;
        assert(result >= a && result >= b);
        return result;
    }
    
    function revertExample(uint256 value) public pure returns (string memory) {
        if (value < 10) {
            revert("Value must be greater than or equal to 10");
        }
        return "Value is valid";
    }
}


## Authors
21bcs3833


license
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;
