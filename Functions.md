---
share: true
---

Visibility to a function specifies how the function is visible to the caller internally or externally.

**Public**

- Visible from internal and external contracts
- Can be called inside a contract or outside a contract
- Default is public
- Visible to the public, so has security concerns

**Private**

- Private functions are visible inside the same contract
- Can be called inside a contract
- Not able to call from an outside contract

**Internal**

- Similar to private functions and visible to contract hierarchy
- Can be called inside a contract and contracts that inherit from it

**External**

- External functions are visible to public functions
- Can only be called outside the contract

### Function Types

There are four types of functions in Solidity:

1. **View**: The function only reads from the smart contract and will not perform any kind of writing operations. A 'view' function does not consume any amount of gas.
2. **Pure**: The function will neither read nor write anything on the smart contract. They are also called helper functions. For example, you can write any mathematical calculations for your smart contract that neither read data from the blockchain nor writes to the blockchain.
3. **Payable**: These functions have the capability to accept Ether as an input. If you are sending ethers to smart contracts, then you need to make sure that it is only to those functions that are defined as payable.
4. **Fallback**: If an incoming transaction call does not match any of the functions defined in a smart contract, then the call will be directed towards the Fallback function. In other words, if there is a call for a function that doesn't exist, then the call will fall to the Fallback function. The fallback function doesn’t have any arguments and they don’t return any values.
5. 