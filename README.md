# KentaToken Smart Contract - Functionalities Summary
The KentaToken smart contract is a specialized ERC20 token that incorporates a variety of unique features. Here's a comprehensive breakdown of its functionality:

Inheritance: The KentaToken contract inherits functionalities from OpenZeppelin's ERC20Pausable and Ownable contracts. This means it comes with standard ERC20 functionalities, pause controls, and ownership controls.

Token Supply: The TOTAL_SUPPLY is a constant set to 
120
×
1
0
27
120×10 
27
 , signifying the total number of tokens available.

Tax Fee: The TAX_FEE is a constant set to 2%. This indicates that each transfer is taxed at 2%, with the tax amount sent to a designated wallet.

Tax Wallet: The taxWallet state variable is the wallet address that receives the tax collected from each transfer. This address can be updated by the contract owner.

Events: The contract emits FunctionCalled and TransferWithTax events that log when specific functions are called and when transfers with taxation occur, respectively.

Constructor: Upon deployment, the contract mints the total supply of tokens and assigns them to the contract creator.

setTaxWallet Function: This function allows the contract owner to update the tax wallet address. It validates that the new address is not the zero address.

burn Function: This function lets the contract owner burn a specified amount of tokens from their balance.

renounceOwnership Function: This allows the contract owner to relinquish ownership of the contract. It emits an OwnershipTransferred event.

pause & unpause Functions: These functions enable the contract owner to pause and unpause token transfers.

getMaxPurchaseLimit Function: This function provides a way to check the maximum token purchase limit at any given time, which is set to 1% of the total supply.

_transfer Function (Overridden): This function handles token transfers while considering the tax fee and the maximum purchase limit. It first deducts the tax fee, transfers it to the tax wallet, and then transfers the remaining tokens to the recipient. It also checks that the transfer amount does not exceed the maximum purchase limit.

To summarize, the KentaToken smart contract offers a unique implementation of an ERC20 token. It includes features like a fixed tax fee on transfers, a maximum purchase limit, and owner-only functions such as token burning and pausing token transfers. The contract benefits from OpenZeppelin's widely used and security-audited contracts for robust and compliant functionality.
