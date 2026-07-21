# Liquidity guide

This guide summarizes the mechanics relevant to Robindator. The
[NOXA liquidity documentation](https://docs.noxa.fi/dex/liquidity/) is the
canonical source and takes precedence if the protocol changes.

## V2 pools

NOXA V2 pools use the classic automated-market-maker model:

- liquidity is deposited as a balanced pair by value;
- providers receive fungible LP tokens;
- the LP tokens represent a proportional share of the pool; and
- removing LP returns both assets according to that share.

V2 positions are simple and remain active across the full price curve, but they
are not protected from impermanent loss.

## V3 pools

NOXA V3 pools use concentrated liquidity:

- each position is represented by an NFT;
- the provider selects a price range;
- narrow ranges can be more capital-efficient but become inactive when price
  moves outside the range; and
- wide or full ranges behave more like V2 liquidity.

NOXA lists 0.05%, 0.3%, and 1% fee tiers. Its documentation identifies 1% as
the default tier for NOXA Fun tokens and as the tier intended for volatile or
new assets.

## Locked NOXA Fun liquidity

According to NOXA, the initial LP for a NOXA Fun launch is:

1. created automatically at launch;
2. deposited into the locker contract; and
3. locked permanently, including against removal by the token creator.

This creates permanent baseline liquidity. It does not guarantee liquidity
depth, trading volume, token value, or protection against contract failure.
Anyone may still create or add separate liquidity positions.

## Fees versus principal

In a V3 position, deposited liquidity and earned trading fees are accounted for
separately. NOXA documents that earned fees can be collected from a position.
For Robindator, any claim that a particular address controls a position or
received fees should be verified through the relevant block explorer and
locker contract.

## Risk checklist

Before adding liquidity:

- verify the token and pool addresses;
- understand the selected price range and fee tier;
- confirm whether the position is locked or removable;
- account for impermanent loss;
- review smart-contract and token risk; and
- use only funds you can afford to lose.

