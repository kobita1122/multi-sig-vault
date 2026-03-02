# Multi-Sig Vault

A decentralized treasury management solution that ensures no single point of failure. Transactions must be proposed and confirmed by a predefined threshold of owners before execution.

### Features
* **Threshold Logic:** Flexible "M-of-N" signing (e.g., 2-of-3, 3-of-5).
* **Transaction Queue:** Transparent list of pending, executed, and revoked transactions.
* **Security:** Prevents reentrancy and unauthorized access using OpenZeppelin standards.
* **Flat Layout:** All logic contained in `MultiSig.sol` for simplified deployment.

### How it Works
1.  **Propose:** Any owner submits a transaction (target, value, data).
2.  **Confirm:** Other owners call `confirmTransaction`.
3.  **Execute:** Once the threshold is met, anyone can call `executeTransaction` to trigger the call.
