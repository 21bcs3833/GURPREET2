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
