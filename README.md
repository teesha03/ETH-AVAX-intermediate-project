# ETH-AVAX-intermediate-project
## Overview

This contract allows a single owner to deposit, withdraw, and transfer Ether funds. It utilizes Solidity's require and revert statements to ensure that only the owner can perform these actions and that the contract's balance is always maintained correctly.

## Getting Started

### Functions

deposit(uint amount):
- Allows the owner to deposit Ether funds into the contract.
- Requires that the sender is the owner and that the deposit amount is greater than 0.
- Increments the contract's balance by the deposit amount.

withdraw(uint amount):
- Allows the owner to withdraw Ether funds from the contract.
- Requires that the sender is the owner, that the withdrawal amount is greater than 0, and that the contract's balance is sufficient to cover the withdrawal.
- Decrements the contract's balance by the withdrawal amount.
- Ensures that the contract's balance does not become negative.

transfer(address recipient, uint amount):
- Allows the owner to transfer Ether funds to a specified recipient.
- Requires that the sender is the owner, that the transfer amount is greater than 0, and that the contract's balance is sufficient to cover the transfer.
- Decrements the contract's balance by the transfer amount.
- Uses the call function to transfer the funds to the recipient and reverts if the transfer fails.

## Security Considerations
- The contract uses require statements to ensure that only the owner can perform actions and that the contract's balance is maintained correctly.
- The contract uses revert statements to undo any changes if an action fails or if the contract's balance becomes negative.

## License

This project is licensed under the MIT License.
