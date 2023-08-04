# KentaToken Smart Contract - Functionalities Summary

The KentaToken contract is an ERC20 token with several additional features, implemented using Solidity version 0.8.0. Here are the main functionalities:

1. **Total Supply**: The token has a total supply of \(120 \times 10^{9} \times 10^{18}\), defined as a constant within the contract.

2. **Tax Fee**: There's a 2% tax fee on transfers, and the tax proceeds are sent to a designated tax wallet.

3. **Set Tax Wallet**: The owner can change the tax wallet address. The address must be valid and not a zero address.

4. **Burn Function**: The owner can burn a specific amount of tokens, thus removing them from circulation.

5. **Ownership Renouncement**: The owner can renounce ownership of the contract, which cannot be undone.

6. **Pause and Unpause**: The owner can pause and unpause token transfers. While paused, no transfers can take place.

7. **Maximum Purchase Limit**: Transfers are limited to 1% of the total supply, but this restriction does not apply to the owner of the contract.

8. **Transfer with Tax**: Transfers within the contract consider the 2% tax. The tax amount is transferred to the tax wallet, and the remaining amount is transferred to the recipient. The owner is not subject to the 1% total supply limit.

9. **Events**: The contract emits events for key functions, providing transparency and traceability. For example, events are emitted for functions like setting the tax wallet, burning tokens, and transfers with tax.

In summary, the KentaToken contract is a sophisticated ERC20 token that provides standard functionalities with additional features, including taxation, burn capability, pausing mechanism, and transfer limitations with exceptions for the owner.
