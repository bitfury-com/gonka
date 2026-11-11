# Bitfury buys another tranche of GNK for 1.75M USDT as part of previously approved 12M USDT smart contract: 1.14M to Community Pool, 0.6M reimbursement of expenditures paid by Bitfury directly to vendors for bug bounty program and security audit

## Summary

Bitfury intends to purchase GNK for 1.75M USDT from the previously approved 12M USDT Community Sale contract at $0.60 per GNK. Of this amount, 607,250 USDT is returned to Bitfury as reimbursement for security audit contracts with HackerOne and Trail of Bits, which Bitfury paid in fiat directly to vendors, because Gonka had no legal entity at the time which both providers needed. The remaining part of 1,142,750 USDT stays on the Community Pool. If the proposal is not approved, none of these transactions will take place

## Background

This proposal combines two things: a purchase of GNK by Bitfury that brings new USDT into the Community Pool as part of previously approved 12M USDT smart contract, and the reimbursement of costs that Bitfury paid earlier directly to vendors on behalf of the network.

The Gonka protocol required independent security work, including security audits, a bug bounty program and related work to improve the security of the network. HackerOne and Trail of Bits contract only with legal entities and invoice in fiat. At the time this work had to begin, Gonka had no legal entity able to act as the contracting party. The Gonka Foundation in Zug was registered in October 2026.

Recognizing that the security of the protocol was a critical priority, Bitfury entered into contracts with both vendors and paid them in advance from its own funds: HackerOne in April 2026 and Trail of Bits in August 2026. The total amount paid was 607,250 USD.

## Rationale

The reimbursement is funded entirely from the new capital Bitfury contributes through this purchase. Existing Community Pool funds are not used. Upon execution, the Community Pool balance will increase by 1,142,750 USDT.

Governance has approved comparable proposals before. Proposal #103 reimbursed costs already paid on behalf of the network, and proposal #102 ratified a third party as the legal counterparty for work required by the network.

## Execution

1. `MsgExec`: under an authz grant from Bitfury, the governance module sends 1,750,000 USDT (CW20 bridged from Ethereum, `gonka15ggwj9un6qrmu4nj5ev6l7kpdcr00td03ff2mmj4cyhl8u8vjd2qnl3hgk`) from `gonka1as7g7ansh8wurv22gqqa9kq7592eclt8tkyycg` to the Community Sale contract `gonka18pkq9mwxxlmyq7kr5txhm060wemg2s4u94wvsfd9w2kdc0u99d6spk8pz2`, which delivers about 2,916,667 GNK to Bitfury.
2. `withdraw_cw20`: the governance module returns 607,250 USDT from the contract to the Bitfury wallet.

Both messages execute together. If the purchase fails, no funds are withdrawn. Bitfury will set up the authz grant and hold at least 1,750,000 USDT in the wallet before voting ends.
