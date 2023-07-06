# ETH_2assessment_1
# Solidity Contract - Assessment

This contract implements a simple deposit function in Solidity. It showcases the usage of the `assert`, `revert`, and `require` statements for validation and error handling.

### SPDX-License-Identifier

The contract is licensed under the MIT License. The SPDX-License-Identifier is specified at the beginning of the file for clarity and legal compliance.

```
// SPDX-License-Identifier: MIT
```

### Pragma Directive

The `pragma solidity` directive specifies the version of the Solidity compiler required to compile the contract. In this case, the contract requires Solidity version 0.8.9.

```
pragma solidity ^0.8.9;
```

### Description
The "test" contract presented here is a Solidity smart contract that showcases error handling techniques using `revert`, `assert`,`require` and custom error messages. The contract enables users to deposit and withdraw funds while ensuring proper validation and error handling.

The contract features a `constructor` that initializes the contract by setting the contract owner and the initial balance. The `deposit` function allows the contract owner to deposit funds into the contract. It verifies that the caller is the owner and updates the balance accordingly. It also utilizes `assert` to assert that the updated balance is correct.

To handle a scenario where the contract does not have sufficient balance for withdrawal, the contract defines a custom error message using the `error` keyword. The `withdraw` function checks if the caller is the owner and if the contract has enough balance for the withdrawal amount. If the condition is not met, it reverts the transaction with the custom error message `InsufficientBalance`.

Overall, this contract provides a practical example of how to implement error handling techniques in Solidity smart contracts to ensure proper validation and handling of errors during deposit and withdrawal operations.


### Deployment and usage
The Solidity smart contract provided in this project demonstrates the implementation of error handling using `revert`, `assert`, and custom error messages. The contract, named `test`, allows users to deposit and withdraw funds while ensuring proper validation and error handling.

The contract features a constructor that initializes the contract's owner and initial balance. The `deposit` function enables the contract owner to deposit funds into the contract, updating the balance accordingly. It employs a `require` statement to verify that the sender is the owner, preventing unauthorized deposits. The `assert` statement is then used to ensure that the balance is updated correctly.

To handle the scenario of insufficient balance during a withdrawal, the contract includes a custom error called `InsufficientBalance`. The `withdraw` function allows the owner to withdraw funds from the contract. Before executing the withdrawal, it checks if the balance is sufficient using a `require` statement. If the balance is insufficient, it reverts the transaction with a custom error message, indicating the current balance and the requested withdrawal amount.

Throughout the contract, `assert` statements are utilized to validate internal contract state and ensure correctness. These statements verify that the changes made to the balance during deposit and withdrawal operations are as expected.

This project serves as a useful reference for implementing error handling mechanisms in Solidity contracts, providing insights into the proper usage of `revert`, `assert`, and custom error messages. Developers can learn how to validate conditions, revert transactions when necessary, and assert internal contract state to ensure the integrity of their smart contracts.


## License

This contract is licensed under the MIT License. Please see the `LICENSE` file for more information.

---

Please note that there was a typo in the function name "Deposite" which I corrected to "Deposit" assuming it was a typographical error. Feel free to modify it as per your requirements.
