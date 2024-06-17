# liquid-staked-gov

Tally and Scopelift are building a protocol for governance tokens in DeFi. It's called Liquid Governance Tokens (tLSTs). The goal of tLSTs is to let tokenholders use their tokens in both DeFi AND governance at the same time.

## Motivation

The ‘governance’ part of governance tokens has to compete with other use cases. Tokens can’t govern from inside DeFi protocols, cold storage, or centralized exchanges. That's because tokens must be delegated, or “activated”, to vote. But, they can’t be activated unless the owner holds them directly.
The challenge will get harder, because yield is coming. Restaking protocols like EigenLayer and Symbiotic will offer yield for everything. That includes governance tokens. This yield will pull even more tokens out of governance.
tLSTs fix the problem. tLSTs make it so that holders don’t have to choose between yield and governance.

## Solution

tLSTs operate under the same constraints as regular governance tokens. If held directly, tLSTs can use their voting power like normal governance tokens. If not held directly, the holders cannot activate tLST voting power themselves.
Unlike governance tokens, Tally's tLST protocol activates the voting power of unactivated tLSTs. When an tLST isn't activated by the holder, the tLST's governance strategy activates it. To prevent capture, the underlying DAO determins the tLST's governance strategy.
tLSTs will be backwards compatible with existing `ERC20Votes` governance tokens.

### Staker support

Yield doesn’t just come from restaking. Some protocols also have native yield. tLST also wraps sources of yield like [UniStaker](https://github.com/uniswapfoundation/UniStaker).

## Implementation

### Smart contract

tLSTs will be ERC20 tokens. They will also implement [ERC20Votes](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/ERC20Votes.sol) and restaking collateral interfaces.

### User interface

Tally will provide an interface for tLSTs
