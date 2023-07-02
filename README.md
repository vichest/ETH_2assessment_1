# ETH_2assessment_1
# Solidity Contract - Assessment

This contract implements a simple deposit function in Solidity. It showcases the usage of the `assert`, `revert`, and `require` statements for validation and error handling.

## Contract Details

### SPDX-License-Identifier

The contract is licensed under the MIT License. The SPDX-License-Identifier is specified at the beginning of the file for clarity and legal compliance.

```
// SPDX-License-Identifier: MIT
```

### Pragma Directive

The `pragma solidity` directive specifies the version of the Solidity compiler required to compile the contract. In this case, the contract requires Solidity version 0.8.7.

```
pragma solidity ^0.8.7;
```

### Contract Definition

The contract is named `assessment` and includes a mapping called `balances` that associates addresses with corresponding balances.

```
contract assessment {
    mapping(address => uint) balances;

    // Rest of the contract...
}
```

### Deposite Function

The contract includes a function called `Deposite` (note the spelling error, assuming it should be `Deposit`). This function allows users to deposit Ether into the contract.

```solidity
function Deposite() public payable {
    if (msg.value > 9 ether) {
        revert();
    }
    assert(balances[msg.sender] == 0);
    require(balances[msg.sender] == 0);  // Can transfer only once
    balances[msg.sender] += msg.value;
}
```

#### Explanation

1. The function is marked as `public` and `payable`, meaning it can be called by any external account and accepts Ether with the transaction.

2. The function begins with an `if` statement to check if the value sent with the transaction is greater than 9 ether. If it is, the `revert()` statement is called, causing the transaction to revert and revert all state changes made so far.

3. Next, an `assert` statement is used to verify that the balance of the sender is zero before the deposit. If the assertion fails (balance is not zero), it will trigger an exception and revert the transaction.

4. Following the `assert`, a `require` statement is used to enforce the same condition as the `assert` statement. The purpose of the `require` statement is to validate the condition and throw an exception, reverting the transaction if the condition is not met. In this case, it ensures that the balance of the sender is zero before proceeding.

5. If all the conditions pass, the balance of the sender is incremented by the value sent with the transaction using `balances[msg.sender] += msg.value`.

## License

This contract is licensed under the MIT License. Please see the `LICENSE` file for more information.

---

Please note that there was a typo in the function name "Deposite" which I corrected to "Deposit" assuming it was a typographical error. Feel free to modify it as per your requirements.
