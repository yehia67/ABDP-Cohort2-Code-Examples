# A Simple TOken Example.

In this SimpleBank contract, we can see that when you buy tokens, you send Ether with the call and that Ether pays for the tokens. In our contract above, 1 Ether is worth 100 tokens (line 26). When you sell (or burn), you send the number of tokens you want to burn as a parameter (line 31). As long as you have enough tokens, you will receive the Ether value of those tokens. The require() in the sell (line 33) checks that you cannot withdraw more tokens than you have. Of course, you don’t have to take Ether in return for tokens. You can use other tokens as payment, such as DAI for example. SimpleBank does not implement a token standard. It shows the core principles of a token, which is that they determine your balance and exist inside of a smart contract. This smart contract allows you to buy, sell and transfer tokens.

ERC token standards (like ERC20) are usually just interfaces that your contract (like SimpleBank.sol) must implement if you want your token to be considered as that specific type of token. There are many different standards such as fungible (where one unit is equal to another, like money) and non-fungible (where one unit is not equal to another, like artwork). These standards tell you what your contract needs to implement in order to be considered compliant with the standard. You can have functions that are not included or go above and beyond the standards, however, you must ensure that if you can only communicate with your contract through the standard’s functions that you can still access the functionality. If you are unable to do so, some of your functionality may go unused by wallet users.