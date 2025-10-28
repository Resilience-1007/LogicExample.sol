
# LogicExample 🔍

This Solidity smart contract demonstrates **conditional logic** and **require statements**.

---

## 🧠 What This Contract Teaches
- How to use `if` / `else` for conditional logic
- How `require()` is used to restrict actions
- Boolean data type and logical flow
- How conditions affect gas usage and execution

---

## 🧩 Contract Example
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract LogicExample {
    uint public age;
    bool public isRegistered;

    function setAge(uint _age) public {
        age = _age;
    }

    function register() public {
        require(age >= 18, "You must be 18 or older to register");
        isRegistered = true;
    }

    function isAdult() public view returns (bool) {
        if (age >= 18) {
            return true;
        } else {
            return false;
        }
    }
}
