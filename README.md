* Incorrect use of tx.origin could lead to security vulnerabilities in smart contracts. You should use ```msg.sender``` instead of ```tx.origin``` to not let this happen
* The attack will happen as follows, initially ```addr1``` will deploy Good.sol and will be the ```owner``` but we can fool the user who has the private key of ```addr1``` to call the ```attack``` function with Attack.sol. And finally we will be able to change the ```owner``` of Good.sol.
* Users lost millions in $RUNE due to an attacker being able to get approvals on $RUNE token by sending a fake token to user's wallets, and approving that token for sale on Uniswap would transfer $RUNE from the user's wallet to the attacker's wallet because THORChain used ```tx.origin``` for transfer checks instead of ```msg.sender```.


# Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a script that deploys that contract.

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test
GAS_REPORT=true npx hardhat test
npx hardhat node
npx hardhat run scripts/deploy.js
```
