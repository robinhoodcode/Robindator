# Flywheel policy

The Robindator flywheel is an experimental treasury policy intended to turn a
portion of eligible trading fees into publicly verifiable token buybacks.

## Treasury

`0xd42801b94ae6ead3d93a09b115d178c0ea1da3a3`

Community members should independently verify this address through official
project channels before relying on it.

## Intended flow

1. A supported pool generates trading fees.
2. Fees attributable to the project's eligible position are claimed.
3. Claimed assets are transferred to or retained by the flywheel treasury.
4. The treasury executes announced purchases through the supported market.
5. Transaction hashes are added to the deployment records or an equivalent
   public ledger.

## What the policy does not guarantee

- A fixed buyback schedule or amount
- A minimum token price
- Continuous trading volume or fee revenue
- Profit for token holders
- Protection from slippage, front-running, or smart-contract failure
- That every pool or position participates in the flywheel

Buybacks are treasury transactions, not dividends or guaranteed distributions.
The policy may be paused when execution would be unsafe, uneconomical, or
inconsistent with applicable requirements.

## Transparency standard

Each reported buyback should include:

- transaction hash;
- execution timestamp;
- input and output assets;
- amount spent;
- tokens received; and
- the pool or router used.

Statements that cannot be verified on-chain should be treated as unconfirmed.
