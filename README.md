# inheritance
Contracts inherit other contracts by using the keyword 'is’.
Contracts can inherit from multiple parent contracts.
When a function is called that is defined multiple times in different contracts, parent contracts are searched from right to left, and in depth-first manner.
Inheritance must be ordered from “most base-like” to “most derived”.

# Multiple Inheritance

Solidity supports multiple inheritance, meaning that one contract can inherit several contracts. 
Multiple inheritance introduces ambiguity called Diamond Problem: if two or more base contracts define the same function, which one should be called in the child contract?
Solidity deals with this ambiguity by using reverse C3 Linearization, which sets a priority between base contracts.
That way, base contracts have different priorities, so the order of inheritance matters. 
Neglecting inheritance order can lead to unexpected behavior.

