# PonsMCP contracts

This repository is reserved for future PonsMCP contracts.

## Current settlement model

PonsMCP **does not deploy or claim a custom settlement contract today**. The current agent-payment flow:

1. creates a server-side payment intent,
2. quotes USDG on Robinhood Chain (`4663`),
3. enforces a local agent policy before signing,
4. sends a direct USDG ERC-20 transfer from the configured agent wallet,
5. verifies the exact recipient and amount from the on-chain receipt,
6. unlocks the merchant resource only after verification.

Any future contract in this repository must have a deployed address, tests, security review, and deployment documentation before it is described as production infrastructure.
