# liquid-staked-gov

A protocol for governance tokens in DeFi, tentatively called Liquid Governance Tokens (LGTs). The goal of the protocol is to let tokenholders use their tokens in both DeFi AND governance at the same time.

## Motivation

The ‘governance’ part of governance tokens has to compete with other use cases. Governance tokens can’t govern from inside DeFi protocols, cold storage, or centralized exchanges. To participate in governance, tokens must be delegated – aka “activated” – but they can’t be activated unless the owner holds them directly.

The challenge will get harder because yield is coming. Restaking protocols like EigenLayer and Symbiotic will offer yield for ERC20s, including governance tokens. That will pull even more tokens out of governance.

Tally’s LGTs fix the problem. LGTs make it so that holders don’t have to choose between yield and governance.

## Solution

If held directly, LGTs can use their voting power like normal governance tokens. Also like normal governance tokens, the holder cannot activate LGT voting power if they don’t hold the LGTs directly. 

However, unlike governance tokens, the Tally protocol activates the voting power of unactivated LGTs. To prevent capture, the Tally protocol will let the underlying governance decide how that extra voting power is used.

