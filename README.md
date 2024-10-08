# Intermediate-Mod-1
### DESCRIPTION

Here in this code snippet we are going to understand how to work with Solidity to do the Error Handelling part using Assert, Revert, Require.

### GETTING STARTED
- Remix Editor

### Assert, Revert and Require Functions

```
// Function to withdraw tokens using require
    function withdrawWithRequire(uint amount) public {
        require(balances[msg.sender] >= amount, "Insufficient balance");
        balances[msg.sender] -= amount;
    }

    // Function to withdraw tokens using revert
    function withdrawWithRevert(uint amount) public {
        if (balances[msg.sender] < amount) {
            revert("Insufficient balance to withdraw");
        }
        balances[msg.sender] -= amount;
    }

    // Function to withdraw tokens using assert
    function withdrawWithAssert(uint amount) public {
        uint initialBalance = balances[msg.sender];
        balances[msg.sender] -= amount;
        assert(balances[msg.sender] == initialBalance - amount);
    }
```

### Authors
- Sabhye Gulati
