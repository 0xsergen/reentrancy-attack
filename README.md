# Re-entrancy Attack

This project consists of two basic staking smart contracts (one of them is vulnerable to re-entrancy attack) and one attack smart contract. The test file is to show the the importance of safety.

<!---This project was developed for use in [this article](https://scdevstr.substack.com/p/re-entrancy-yeniden-giris-atag) (in Turkish).-->

## Run Locally
To get started with this project, clone this repo and follow these commands in your terminal:

Clone the project

```bash
  git clone git clone https://github.com/0xsergen/reentrancy-attack.git
```

Go to the directory of project

```bash
  cd reentrancy-attack 
```

Install dependencies

```bash
  yarn install
```

Run the test

```bash
  npx hardhat test test/Attack.js
```

You should see similar output. 
```bash
  Re-entrancy Attack
User1 deposited 5 ETH to VulnerableStaking.
User2 deposited 5 ETH to VulnerableStaking.
VulnerableStaking has 10 ETH now.
Attacker will attack to VulnerableStaking now.
ETH balance of Staking Contract is 0.0
    ✔ Should hack vulnerable staking contract
User1 deposited 5 ETH to SafeStaking.
User2 deposited 5 ETH to SafeStaking.
SafeStaking has 10 ETH now.
Attacker will attack to VulnerableStaking now.
ETH balance of Staking Contract is 10.0
    ✔ Should NOT hack safe staking contract

  2 passing
  ```

You can check and modify `test/Attack.js` to try different scenarios. 

